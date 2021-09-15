---
description: Para descifrar un mensaje con sobres, el destinatario coincide con un certificado del almacén Mi que tiene una clave privada disponible con un certificado en el mensaje sobres.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Recepción de un mensaje de datos con sobres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476392"
---
# <a name="receiving-an-enveloped-data-message"></a>Recepción de un mensaje de datos con sobres

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Para descifrar un mensaje con sobres, el destinatario coincide con un certificado del almacén Mi que tiene una clave privada disponible con un certificado en el mensaje sobres. [](../secgloss/c-gly.md) Si se encuentra una coincidencia, se descifra la clave cifrada asociada a ese certificado y esa clave descifrada se usa para descifrar el mensaje envoltorio. Un destinatario del mensaje que no tenga un certificado correspondiente con una clave privada disponible no puede descifrar el mensaje.

En el ejemplo siguiente, se pasa un nombre de archivo a la subrutina, ese archivo se abre y se lee un mensaje sobre. A continuación, se descifra el mensaje con sobres. Los pasos para hacer coincidir un certificado de usuario con un certificado en el mensaje sobre, descifrar la clave de cifrado y, por último, descifrar el mensaje se realizan en segundo plano. Se produce un error si no se encuentra una coincidencia de certificado o si se produce un error en el descifrado.

En cualquier error CAPICOM, se devuelve un valor decimal negativo **de Err.Number.** Para obtener más información, vea [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obtener información sobre los valores decimales positivos **de Err.Number,** vea Winerror.h.


```VB
Sub ReceiveMessage(ByVal InFile As String)
On Error GoTo ErrorHandler

'Declare an EnvelopedData object

Dim Envmessage As New EnvelopedData

'Declare a string variable to hold the encrypted message.

Dim Encrypted As String

' Open an input file and read in the encrypted message
Open InFile For Input As #1
Input #1, Encrypted
Close #1

' If the length of the input string is greater than 0, 
' an encrypted message string is available. Decrypt the message.
' Note: to decrypt the message, a certificate with access to
' a user's private key must be available, and that certificate must
' match one of the certificates in the Recipients collection of 
' certificates.
If Len(Encrypted) > 0 Then
    ' Receive and decrypt the message
    Envmessage.Decrypt encrypted
    
    ' Display the decrypted message.
    MsgBox Envmessage.Content
Else
    MsgBox "No enveloped message was read in."
End If
' Release the EncryptedData object.
Set Envmessage = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 
