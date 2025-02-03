# HotelBookingSystem
Public Class Form1

    Private Sub btnSignUp_Click(sender As Object, e As EventArgs) Handles btnSignUp.Click
        ' Retrieve the input values
        Dim username As String = txtUsername.Text
        Dim password As String = txtPassword.Text
        Dim confirmPassword As String = txtConfirmPassword.Text

        ' Basic validation checks
        If String.IsNullOrEmpty(username) Or String.IsNullOrEmpty(password) Or String.IsNullOrEmpty(confirmPassword) Then
            lblMessage.Text = "All fields are required."
            lblMessage.ForeColor = Color.Red
            Return
        End If

        If password <> confirmPassword Then
            lblMessage.Text = "Passwords do not match."
            lblMessage.ForeColor = Color.Red
            Return
        End If

        ' If all validations pass, display success message
        lblMessage.Text = "Sign-Up Successful!"
        lblMessage.ForeColor = Color.Green

        ' You can add code here to save the user credentials to a database or file
    End Sub

End Class
