---
description: Cuando se recibe un documento firmado, se puede comprobar la validez de la firma o las firmas.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Comprobar la firma de un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910069"
---
# <a name="verifying-the-signature-on-a-document"></a><span data-ttu-id="e4f1f-103">Comprobar la firma de un documento</span><span class="sxs-lookup"><span data-stu-id="e4f1f-103">Verifying the Signature on a Document</span></span>

<span data-ttu-id="e4f1f-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e4f1f-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="e4f1f-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="e4f1f-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="e4f1f-107">Cuando se recibe un documento firmado, se puede comprobar la validez de la firma o las firmas.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-107">When a signed document is received, the validity of the signature or signatures can be checked.</span></span> <span data-ttu-id="e4f1f-108">Se puede comprobar una firma para:</span><span class="sxs-lookup"><span data-stu-id="e4f1f-108">A signature can be checked for:</span></span>

-   <span data-ttu-id="e4f1f-109">Validez del hash de firma</span><span class="sxs-lookup"><span data-stu-id="e4f1f-109">Validity of the signature hash</span></span>
-   <span data-ttu-id="e4f1f-110">Validez del certificado del firmante</span><span class="sxs-lookup"><span data-stu-id="e4f1f-110">Validity of the signer's certificate</span></span>

<span data-ttu-id="e4f1f-111">El [*hash*](../secgloss/h-gly.md) de firma se descifra mediante la [*clave pública*](../secgloss/p-gly.md) del firmante que se encuentra en el [*certificado*](../secgloss/c-gly.md)del firmante, incluido como parte de la firma.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-111">The signature [*hash*](../secgloss/h-gly.md) is decrypted using the [*public key*](../secgloss/p-gly.md) of the signer found on the signer's [*certificate*](../secgloss/c-gly.md), included as part of the signature.</span></span> <span data-ttu-id="e4f1f-112">Si la firma descifrada coincide con un nuevo hash del documento original, la firma la creó el propietario de la clave privada asociada a la clave pública utilizada para descifrar el hash.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-112">If the decrypted signature matches a new hash of the original document, the signature was created by the owner of the private key associated with the public key used to decrypt the hash.</span></span> <span data-ttu-id="e4f1f-113">Además, se garantiza que el documento en el que se basa la firma no se ha cambiado después de crear la firma.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-113">In addition, the document that the signature is based on is guaranteed not to have been changed after the signature was created.</span></span>

<span data-ttu-id="e4f1f-114">También se puede comprobar la validez del certificado que proporcionó la clave pública y la identidad del firmante, como por ejemplo, si el certificado se ha revocado, si el certificado no está actualizado o si el certificado lo ha emitido un emisor de certificados de confianza.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-114">The certificate that provided the public key and the identity of the signer can also be checked for validity including such issues as whether the certificate has been revoked, whether the certificate is out of date, or whether the certificate was issued by a trusted certificate issuer.</span></span>

<span data-ttu-id="e4f1f-115">En el ejemplo siguiente, el contenido firmado y el objeto **SignedData** se leen desde un archivo, y se comprueba la firma y la validez del certificado utilizado para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-115">In the following example, the content signed and the **SignedData** object are read in from a file and the signature and the validity of the certificate used to create the signature are checked.</span></span>

> [!Note]  
> <span data-ttu-id="e4f1f-116">Si la firma no es válida criptográficamente o el certificado del firmante no es válido, se produce una excepción y el programa que comprueba debe controlar la excepción.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-116">If the signature is not cryptographically valid or the certificate of the signer is not valid, an exception is raised and the verifying program must handle the exception.</span></span> <span data-ttu-id="e4f1f-117">En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="e4f1f-117">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="e4f1f-118">Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="e4f1f-118">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="e4f1f-119">Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="e4f1f-119">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
