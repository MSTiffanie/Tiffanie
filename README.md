# Tiffanie
 HW
Code

Public Class Form1
    Private Sub btnSubmit_Click(sender As Object, e As EventArgs) Handles btnSubmit.Click

        'Club Fees for age range
        Dim childFee As Double = 0   'index 0
        Dim minorFee As Double = 5    'index 1
        Dim adultFee As Double = 10   'index 2
        Dim seniorFee As Double = 7  'index 3
        Dim clubFee As Double = 0

        'Read input from listbox
        Dim index As Integer = ListBox1.SelectedIndex

        If (index = 0) Then
            clubFee = childFee
        ElseIf (index = 1) Then
            clubFee = minorFee
        ElseIf (index = 2) Then
            clubFee = adultFee
        ElseIf (index = 3) Then
            clubFee = seniorFee
        Else
            clubFee = 0
        End If

        Select Case index
            Case 0
                clubFee = childFee
            Case 1
                clubFee = minorFee
            Case 2
                clubFee = adultFee
            Case 3
                clubFee = seniorFee
            Case Else
                clubFee = 0
        End Select

        Dim memberClass As String      'Minor, 'Adult, 'Senior, 'Child,

        memberClass = ListBox1.Text

        If (memberClass = "Chlid") Then
            clubFee = childFee
        ElseIf (memberClass = "Adult") Then
            clubFee = adultFee
        ElseIf (memberClass = "Minor") Then

            clubFee = minorFee
        ElseIf (memberClass = "Senior") Then
            clubFee = seniorFee
        Else childFee = 0

        End If

        If (radChild.Checked = True) Then
            clubFee = childFee
        ElseIf (radMinor.Checked = True) Then
            clubFee = minorFee
        ElseIf (radAdult.Checked = True) Then
            clubFee = adultFee
        ElseIf (radSenior.Checked = True) Then
            clubFee = seniorFee
        Else
            clubFee = 0
        End If

        Dim pepsi, coke, sprite As Double
        If (chkPepsi.Checked) Then
            pepsi = 1.5
        End If

        If (chkCoke.Checked) Then
            coke = 2

        End If
        If (chkSprite.Checked) Then
            sprite = 2

        End If
        clubFee = clubFee + (pepsi + coke + sprite)



        txtFee.Text = clubFee.ToString("C2")



    End Sub
End Class
