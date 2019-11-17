# Pangram-checking
Check a sentence whether it is a pangram or not
    Sub Main()
        Dim str1 As String
        Dim counter As Integer
        Dim nextalpha As String
        Dim ispangram As Boolean

        Console.WriteLine("enter pangram : ")
        str1 = Console.ReadLine

        ispangram = False

        If Len(str1) >= 26 Then
            ispangram = True

            str1 = vbUpperCase

            For counter = 65 To 90
                nextalpha = Chr(counter)

                If Loc(str1, nextalpha) = 0 Then
                    ispangram = False


                    Exit For

                End If

            Next

        End If

        If ispangram = True Then
            Console.WriteLine("Sentence is pangram")

        End If

        If ispangram = False Then
            Console.WriteLine("Sentence is not a pangram")
        End If

        Console.ReadKey()

    End Sub

 

End Module
