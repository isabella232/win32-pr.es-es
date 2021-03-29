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
# <a name="receiving-an-enveloped-data-message"></a><span data-ttu-id="b920d-103">Recibir un mensaje de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="b920d-103">Receiving an Enveloped Data Message</span></span>

<span data-ttu-id="b920d-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b920d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b920d-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b920d-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="b920d-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="b920d-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="b920d-107">Para descifrar un mensaje con doble cifrado, el destinatario coincide con un [*certificado*](../secgloss/c-gly.md) del almacén My que tiene una clave privada disponible con un certificado en el mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="b920d-107">To decrypt an enveloped message, the recipient matches a [*certificate*](../secgloss/c-gly.md) from the My store that has an available private key with a certificate in the enveloped message.</span></span> <span data-ttu-id="b920d-108">Si se encuentra una coincidencia, se descifra la clave cifrada asociada a ese certificado y la clave descifrada se usa para descifrar el mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="b920d-108">If a match is found, the encrypted key associated with that certificate is decrypted and that decrypted key is used to decrypt the enveloped message.</span></span> <span data-ttu-id="b920d-109">Un destinatario del mensaje que no tenga un certificado coincidente con una clave privada disponible no podrá descifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b920d-109">A message recipient that does not have a matching certificate with an available private key cannot decrypt the message.</span></span>

<span data-ttu-id="b920d-110">En el ejemplo siguiente, se pasa un nombre de archivo a la subrutina, se abre ese archivo y se lee un mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="b920d-110">In the example that follows, a file name is passed into the subroutine, that file is opened and an enveloped message is read in.</span></span> <span data-ttu-id="b920d-111">A continuación, se descifra el mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="b920d-111">The enveloped message is then decrypted.</span></span> <span data-ttu-id="b920d-112">Los pasos para hacer coincidir un certificado de usuario con un certificado en el mensaje con doble cifrado, descifrar la clave de cifrado y, por último, descifrar el mensaje se realizan en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b920d-112">The steps of matching a user certificate with a certificate in the enveloped message, of decrypting the encryption key, and finally of decrypting the message are all done behind the scenes.</span></span> <span data-ttu-id="b920d-113">Se produce un error si no se encuentra una coincidencia de certificado o si se produce un error en el descifrado.</span><span class="sxs-lookup"><span data-stu-id="b920d-113">An error is raised if a certificate match is not found or if the decryption fails.</span></span>

<span data-ttu-id="b920d-114">En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="b920d-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="b920d-115">Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="b920d-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="b920d-116">Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b920d-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 
