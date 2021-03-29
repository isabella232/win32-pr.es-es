---
description: Esta subrutina toma una cadena de contraseña que se utilizará para generar una clave de cifrado de sesión y el nombre de un archivo desde el que se leerá un mensaje cifrado. Todos los parámetros se pasan a la subrutina por valores.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Descifrado de un mensaje en CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba984bad7d9289eaf89725e9598a4330f16b49ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648379"
---
# <a name="decrypting-a-message-in-capicom"></a>Descifrado de un mensaje en CAPICOM

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

Esta subrutina toma una cadena de contraseña que se utilizará para generar una clave de cifrado de sesión y el nombre de un archivo desde el que se leerá un mensaje cifrado. Todos los parámetros se pasan a la subrutina por valores.

> [!Note]  
> CAPICOM no admite el tipo de \# contenido de PKCS 7 EncryptedData, pero usa una estructura ASN no estándar para EncryptedData. Por lo tanto, solo CAPICOM puede descifrar un objeto EncryptedData de CAPICOM.

 

Si se produce un error en el descifrado, se comprueba el valor de **Err. Number** para determinar si el error se debe al uso de una contraseña que no coincidía con la contraseña usada para cifrar el mensaje. En este caso, \_ se devuelve el error de datos incorrectos de NTE \_ .

En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** . Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md). Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.


```VB
Sub DecryptMessage(ByVal hidden As String, ByVal filename As String)
On Error goto ErrorHandler

'Declare an EncryptedData object

Dim message As New EncryptedData

'Declare a string variable to hold the encrypted message.
Dim encrypted As String

' Open an input file and read in the encrypted message
Open filename For Input As #1
Input #1, encrypted
Close #1

' If a message was read in (the length of the input string is 
' greater than 0), set the password and decrypt the message.
If Len(encrypted) > 0 then
    ' Set the password used to generate the key
    ' used to decrypt the message. If the password
    ' not the same as the password used when the message
    ' was encrypted, decryption will fail.
    ' The algorithm name and key length set in the encrypting
    ' process are automatically used to decrypt the message. 
    message.SetSecret hidden
    message.Decrypt encrypted
    ' Display the decrypted message.
    MsgBox message.Content
else
    msgbox "No encrypted message was read in.
endif

' Release the EncryptedData object and exit the subroutine.
Set message = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
'    Check for a bad password error.
    If Err.Number = -2146893819 Then
        MsgBox "Error. The password may not be correct."
    Else
        MsgBox "CAPICOM error found : " & Err.Number
    End If
End If
End Sub
```



 

 



