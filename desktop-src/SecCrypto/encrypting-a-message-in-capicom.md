---
description: Esta subrutina toma una cadena que se va a cifrar, una cadena de contraseña que se usará para generar una clave de cifrado y el nombre de un archivo donde se escribirá el mensaje cifrado.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Cifrado de un mensaje en CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8039586736c09673644cacc90759e8d5f25b6e1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476427"
---
# <a name="encrypting-a-message-in-capicom"></a>Cifrado de un mensaje en CAPICOM

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Esta subrutina toma una cadena que se va a cifrar, una cadena de contraseña que se usará para generar una clave de cifrado y el nombre de un archivo donde se escribirá el mensaje cifrado. Todos los parámetros se pasan a la subrutina por valores. Para descifrar el mensaje, se debe usar la misma cadena de contraseña. Si se pierde la contraseña, el texto no se puede descifrar. La privacidad del mensaje se pierde si un destinatario no deseado obtiene acceso a la contraseña.

> [!Note]  
> CAPICOM no admite el tipo de contenido PkCS 7 EncryptedData, pero usa una estructura ASN no estándar \# para EncryptedData. Como resultado, solo CAPICOM puede descifrar un objeto CAPICOM EncryptedData.

 

En cualquier error CAPICOM, se devuelve un valor decimal negativo de la **propiedad Err.Number.** Para obtener más información, [**vea CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obtener información sobre los valores decimales positivos de **Err.Number,** vea Winerror.h.


```VB
Sub EncryptMessage(ByVal TobeEncrypted As String, ByVal hidden _
    As String, ByVal filename As String)

    On Error GoTo ErrorHandler

    ' Declare and initialize an EncryptedData object.
    ' Algorithm.Name and KeyLength do not need to be set.

    Dim message As New EncryptedData
    message.Content = Tobeencrypted
    message.SetSecret(hidden)
    ' Optionally, the encryption algorithm and key length can be set.
    ' If these properties are not set, the default algorithm and key 
    ' length are used.
    ' Information about the algorithm and key length is saved with 
    ' the encrypted string and the individual decrypting the message
    ' does not need to set these properties.

    message.Algorithm.Name = CAPICOM_ENCRYPTION_ALGORITHM_DES

    ' Declare the string that will hold the encrypted message.

    Dim encryptedmessage As String

    ' Encrypt the message storing the result in the encryptedmessage
    ' string.
    encryptedmessage = message.Encrypt

    ' Optionally, check the length of the encrypted string to 
    ' make sure that the encrypt method worked. 

    If Len(encryptedmessage) < 1 Then
        MsgBox("no message encrypted. ")
    Else
        MsgBox(" Message is " & Len(encryptedmessage) & " characters")

        ' Open an output file and write the encrypted message to the
        ' file. The file is not opened if there is no message
        ' to write.
    Open filename For Output As #1
    Write #1, encryptedmessage
    Close #1
        MsgBox("Encrypted message written to file ")
    End If

    ' Release the EncryptedData object.
    message = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 



