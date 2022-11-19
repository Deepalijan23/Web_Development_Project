# Master_Trail_Project

JavaScript Form Validation
Many websites utilize form validation for client-side validation of user details, card details, address details, and other information. If a mandatory input field name exists, the user can type a number, leave the field blank, type only one letter, and so on. All of these validations are simple to implement using JavaScript. Implement the following validations

<html>
    <head>
        <title>Registration form.com</title>
        <style>
          body{
              background-color: rgba(247, 239, 239, 0.884);
          }
              </style>
      </head>
    <body>
        <div class="container">
            <h1><b>REGISTRATION FORM</b></h1>
            <form name="registration" class="registartion-form" onsubmit="return formValidation()">
              <table>
                <tr>
                    <td><label for="userid">USER ID</label></td>
                    <td><input type="userid" name="userid" id="userid" placeholder="userid"></td>
                </tr>
                <tr>
                  <td><label for="name">NAME:</label></td>
                  <td><input type="text" name="name" id="name" placeholder="name"></td>
                </tr>
                <tr>
                  <td><label for="email">EMAIL:</label></td>
                  <td><input type="text" name="email" id="email" placeholder="email"></td>
                </tr>
                <tr>
                  <td><label for="password">PASSWORD:</label></td>
                  <td><input type="password" name="password" id="password" placeholder="password"></td>
                </tr>
                <tr>
                  <td><label for="phoneNumber">PHONE NUMBER:</label></td>
                  <td><input type="number" name="phoneNumber" id="phoneNumber"></td>
                </tr>
                <tr>
                  <td><label for="gender">GENDER:</label></td>
                  <td>Male <input type="radio" name="gender" value="male">
                    Female <input type="radio" name="gender" value="female">
                    Other <input type="radio" name="gender" value="other"></td>
                </tr>
                <tr>
                  <td><label for="Country">COUNTRY</label></td>
                  <td>
                    <select name="Country" id="country">
                      <option value="">Select Country</option>
                      <option value="Africa">Africa</option>
                      <option value="America">America</option>
                      <option value="Bangalore">Bangalore</option>
                      <option value="China">China</option>
                      <option value="Dubai">Dubai</option>
                      <option value="Germany">Germany</option>
                      <option value="India">India</option>
                      <option value="Japan">Japan</option>
                      <option value="Russia">Russia</option>
                    </select>
                  </td>
                </tr>
                <tr>
                  <td><label for="zipcode">ZIP CODE:</label></td>
                  <td><input type="number" name="zipcode" id="zipcode"></td>
                </tr>
                <tr>
                    <td><label for="language">LANGUAGE:</label></td>
                    <td>English <input type="checkbox" name="English" value="English">
                      Hindi <input type="checkbox" name="Non English" value="non english">
                </tr>
                <tr>
                  <td><label for="about">ABOUT:</label></td>
                  <td><textarea name="about" id="about" placeholder="Write about yourself..."></textarea></td>
                </tr>
                <tr>
                  <td colspan="2"><input type="submit" class="submit" value="SUBMIT" /></td>
                </tr>
              </table>
            </form>
          </div>
          <style>
            * {
          margin: 0
        }
        
        .container {
          display: flex;
          justify-content: center;
          align-items: center;
          flex-direction: column;
          height: 100vh;
          
        }
        
        .container h1 {
          color: rgb(0, 0, 0);
          font-family: sans-serif;
          margin: 20px;
        }
        
        .registartion-form {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 600px;
          color: rgb(15, 6, 6);
          font-size: 120px;
          font-family: sans-serif;
          background-color: hsla(0, 91%, 87%, 0.742);
          padding: 1px;
        }
        
        .registartion-form input,
        .registartion-form select,
        .registartion-form textarea {
          border: none;
          padding: 5px;
          margin-top: 10px;
          font-family: sans-serif;
        }
        
        .registartion-form input:focus,
        .registartion-form textarea:focus {
          box-shadow: 10px 10px 10px rgb(228, 228, 228), -3px -3px 10px rgb(224, 224, 224);
        }
        
        .registartion-form .submit {
          width: 100%;
          padding: 8px 0;
          font-size: 20px;
          color: rgb(12, 4, 4);
          background-color: #746363;
          border-radius: 5px;
        }
        
        .registartion-form .submit:hover {
          box-shadow: 3px 3px 6px rgb(255, 214, 176);
        }
          </style>
          <script>
            // Select all input elements for varification
        const name = document.getElementById("name");
        const email = document.getElementById("email");
        const password = document.getElementById("password");
        const phoneNumber = document.getElementById("phoneNumber");
        const gender = document.registration;
        const language = document.getElementById("language");
        const zipcode = document.getElementById("zipcode");
        
        // function for form validation
        function formValidation() {
          
        // checking name length
        if (name.value.length < 2 || name.value.length > 20) {
            alert("Name length should be more than 2 and less than 21");
            name.focus();
            return false;
        }
        // checking email
        if (email.value.match(/^\w+([\.-]?\w+)w+([\.-]?\w+)*(\.\w{2,3})+$/)) {
            alert("Please enter a valid email!");
            email.focus();
            return false;
        }
        // checking password
        if (!password.value.match(/^.{5,15}$/)) {
            alert("Password length must be between 5-15 characters!");
            password.focus();
            return false;
        }
        // checking phone number
        if (!phoneNumber.value.match(/^[1-9][0-9]{9}$/)) {
            alert("Phone number must be 10 characters long number and first digit can't be 0!");
            phoneNumber.focus();
            return false;
        }
        // checking gender
        if (gender.gender.value === "") {
            alert("Please select your gender!");
            return false;
        }
        // checking language
        if (language.value === "") {
            alert("Please select your language!")
            return false;
        }
        // checking zip code
        if (!zipcode.value.match(/^[0-9]{6}$/)) {
            alert("Zip code must be 6 characters long number!");
            zipcode.focus();
            return false;
        }
        return true;
        }
          </script>
        
    </body>
</html>

