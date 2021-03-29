---
description: Para descifrar un mensaje con doble cifrado, el destinatario coincide con un certificado del almacén My que tiene una clave privada disponible con un certificado en el mensaje con doble cifrado.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Recibir un mensaje de datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912821"
---
# <a name="receiving-an-enveloped-data-message"></a>Recibir un mensaje de datos con doble cifrado

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

Para descifrar un mensaje con doble cifrado, el destinatario coincide con un [*certificado*](../secgloss/c-gly.md) del almacén My que tiene una clave privada disponible con un certificado en el mensaje con doble cifrado. Si se encuentra una coincidencia, se descifra la clave cifrada asociada a ese certificado y la clave descifrada se usa para descifrar el mensaje con doble cifrado. Un destinatario del mensaje que no tenga un certificado coincidente con una clave privada disponible no podrá descifrar el mensaje.

En el ejemplo siguiente, se pasa un nombre de archivo a la subrutina, se abre ese archivo y se lee un mensaje con doble cifrado. A continuación, se descifra el mensaje con doble cifrado. Los pasos para hacer coincidir un certificado de usuario con un certificado en el mensaje con doble cifrado, descifrar la clave de cifrado y, por último, descifrar el mensaje se realizan en segundo plano. Se produce un error si no se encuentra una coincidencia de certificado o si se produce un error en el descifrado.

En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** . Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md). Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.


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



 

 
