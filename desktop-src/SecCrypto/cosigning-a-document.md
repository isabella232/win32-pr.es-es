---
description: Un documento puede estar firmado por más de un firmante.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Firmar un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689698"
---
# <a name="cosigning-a-document"></a><span data-ttu-id="328c3-103">Firmar un documento</span><span class="sxs-lookup"><span data-stu-id="328c3-103">Cosigning a Document</span></span>

<span data-ttu-id="328c3-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="328c3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="328c3-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="328c3-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="328c3-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="328c3-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="328c3-107">Un documento puede estar firmado por más de un firmante.</span><span class="sxs-lookup"><span data-stu-id="328c3-107">A document can be signed by more than one signer.</span></span> <span data-ttu-id="328c3-108">Esto sucede cuando, por ejemplo, dos o más entidades firman un contrato o un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="328c3-108">This happens when, for instance, two or more parties sign a contract or an expense report.</span></span> <span data-ttu-id="328c3-109">En el siguiente ejemplo, un documento ya firmado lo recibe un segundo firmante.</span><span class="sxs-lookup"><span data-stu-id="328c3-109">In the following example, a document already signed is received by a second signer.</span></span> <span data-ttu-id="328c3-110">Este firmante usa el método de [**cofirma**](signeddata-cosign.md) para adjuntar una firma adicional al documento.</span><span class="sxs-lookup"><span data-stu-id="328c3-110">This signer uses the [**CoSign**](signeddata-cosign.md) method to attach an additional signature to the document.</span></span>

<span data-ttu-id="328c3-111">Si se produce algún error de CAPICOM, se devuelve un valor negativo en la propiedad **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="328c3-111">If any CAPICOM error occurs, a negative value is returned in the **Err.Number** property.</span></span> <span data-ttu-id="328c3-112">Para obtener más información sobre los códigos de error de CAPICOM, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="328c3-112">For more information about CAPICOM error codes, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="328c3-113">Si el código de error de la propiedad **Err. Number** es un valor positivo, el error es un error de Windows.</span><span class="sxs-lookup"><span data-stu-id="328c3-113">If the error code in the **Err.Number** property is a positive value, then the error is a Windows error.</span></span> <span data-ttu-id="328c3-114">Para obtener información acerca de los códigos de error de Windows, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="328c3-114">For information about Windows error codes, see Winerror.h.</span></span>

> [!Note]
> <span data-ttu-id="328c3-115">Para firmar un documento también es necesario que el cofirmador tenga un [*certificado*](../secgloss/c-gly.md) disponible con una [*clave privada*](../secgloss/p-gly.md) para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="328c3-115">Cosigning a document also requires that the cosigner have an available [*certificate*](../secgloss/c-gly.md) with a [*private key*](../secgloss/p-gly.md) to create the signature.</span></span> <span data-ttu-id="328c3-116">Si no se especifica un firmante en la llamada del método [**Sign**](signeddata-sign.md) y no hay ningún certificado en CAPICOM \_ My \_ Store con una clave privada asociada, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="328c3-116">If a signer is not specified in the call of the [**Sign**](signeddata-sign.md) method and there is no certificate in CAPICOM\_MY\_STORE with an associated private key, the method fails.</span></span> <span data-ttu-id="328c3-117">Si solo hay un certificado en CAPICOM \_ My \_ Store con una clave privada asociada, se usan esa clave y el certificado.</span><span class="sxs-lookup"><span data-stu-id="328c3-117">If there is one and only one certificate in CAPICOM\_MY\_STORE with an associated private key, that key and certificate are used.</span></span> <span data-ttu-id="328c3-118">Si hay más de un certificado que se puede usar, se muestra un mensaje para permitir que el usuario elija el certificado deseado.</span><span class="sxs-lookup"><span data-stu-id="328c3-118">If there is more than one usable certificate, a prompt is displayed to allow the user to choose the desired certificate.</span></span>
> 
> <span data-ttu-id="328c3-119">Si se usa el método de [**cofirmación**](signeddata-cosign.md) en una aplicación basada en Web, siempre se muestra un símbolo del sistema para obtener el permiso del usuario antes de crear una firma mediante la clave privada de dicho firmante.</span><span class="sxs-lookup"><span data-stu-id="328c3-119">If the [**CoSign**](signeddata-cosign.md) method is used in a web-based application, a prompt is always displayed to get the user's permission before a signature is created by using that signer's private key.</span></span>

 

<span data-ttu-id="328c3-120">En el ejemplo siguiente, se leen los archivos que contienen el documento que se va a firmar y las firmas actuales de dicho documento, la firma es cofirmada y la nueva firma se escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="328c3-120">In the following example, files that contain the document to be signed and the current signatures on that document are read, the signature is cosigned, and the new signature is written to a file.</span></span> <span data-ttu-id="328c3-121">En el ejemplo se utiliza una firma desasociada con los datos firmados y la firma en archivos independientes.</span><span class="sxs-lookup"><span data-stu-id="328c3-121">The example uses a detached signature with the data signed and the signature in separate files.</span></span>


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
