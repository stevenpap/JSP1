# JSP1


<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
	pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>Insert title here</title>
<link rel="stylesheet" type="text/css" href="DataEntry.css">
</head>
<body>
	<p>Are you a student or a Teacher.Please check the corresponding
		box.</p>

	<form method="GET" action="DataEntry.jsp">
		<p>
			<input type="checkbox" name="Person" value="Teacher" />Teacher
		</p>
		<p>
			<input type="checkbox" name="Person" value="Student" />Student
		</p>
		<p>
			<input type="submit" value="submit" />
	</form>
	<%
		String Person[] = request.getParameterValues("Person");
	%>
	<%
		String t = request.getParameter("Person");
	%>
	<%
		if (Person != null && t.equals("Teacher")) {
	%>
	<%
		for (int i = 0; i < Person.length; i++) {
	%>
	<%=Person[i] + "s enter information in the following forms:"%>
	<form method="get" action="DataView.jsp">
		<label> First name: <input type="text" name="first_name" />
		</label> <br> <br> <label> Last name: <input type="text"
			name="last_name" />
		</label> <br> <br> <label> Phone number: <input type="text"
			name="phone_number" />
		</label> <br> <br> <label> Mobile phone number: <input
			type="text" name="mobile_phone_number" />
		</label> <br> <br> <label> Social security number:<input
			type="text" name="social_security_number" />
		</label> <br> <br> <label> Bank account number:<input
			type="text" name="bank_account_number" />
		</label> <br> <br> <label> Employee ID:<input type="text"
			name="employee_ID" />
		</label> <br> <br> <label> Date of Birth:<input type="text"
			name="birthdate" />
		</label> <br> <br> <label> Enter Sex: <select
			name="dropdown">
				<option value="" disabled selected>Select Sex</option>
				<option value="0-Male">0-Male</option>
				<option value="1-Female">1-Female</option>
		</select>
		</label> <br> <br> <label> Enter ID Card Type: <select
			name="dropdown">
				<option value="" disabled selected>Select ID Card</option>
				<option value="1-ID Card">1-ID Card</option>
				<option value="2-Passport">2-Passport</option>
				<option value="3-Driver's licence">3-Driver's licence</option>
		</select>
		</label> <br> <br> <label> ID Card Number:<input type="text"
			name="card_number" />
		</label> <br> <br> <label> Residence Address:<input
			type="text" name="card_number" />
		</label> <br> <br>
		<p>
			<input type="submit" value="submit" />
	</form>
	<%
		}
		} else if (Person != null && t.equals("Student")) {
	%>

	<%
		for (int i = 0; i < Person.length; i++) {
	%>
	<%=Person[i] + "s enter information in the following forms:"%>
	<form method="get" action="DataView.jsp">
		<label> First name: <input type="text" name="first_name" />
		</label> <br> <br> <label> Last name: <input type="text"
			name="last_name" />
		</label> <br> <br>
		<p>
			<input type="submit" value="submit" />
	</form>
	<%
		}
		}
	%>

</body>
</html>
