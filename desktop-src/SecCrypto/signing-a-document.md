---
description: Un uso estándar de una firma es firmar un texto y guardar ese texto firmado en un archivo. También se puede enviar el texto firmado a través de Internet. El mensaje firmado está en \# formato PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Firmar un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666210"
---
# <a name="signing-a-document"></a><span data-ttu-id="b5ead-105">Firmar un documento</span><span class="sxs-lookup"><span data-stu-id="b5ead-105">Signing a Document</span></span>

<span data-ttu-id="b5ead-106">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b5ead-106">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b5ead-107">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b5ead-107">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="b5ead-108">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="b5ead-108">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="b5ead-109">Un uso estándar de una firma es firmar un texto y guardar ese texto firmado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="b5ead-109">A standard use of a signature is to sign a text and save that signed text to a file.</span></span> <span data-ttu-id="b5ead-110">También se puede enviar el texto firmado a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="b5ead-110">The signed text could also be sent over the Internet.</span></span> <span data-ttu-id="b5ead-111">El mensaje firmado está en \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="b5ead-111">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="b5ead-112">En este ejemplo, la firma se crea para el contenido separado (cuando el contenido no se incluye con la firma).</span><span class="sxs-lookup"><span data-stu-id="b5ead-112">In this example, the signature is created for detached content (when the content is not included with the signature).</span></span> <span data-ttu-id="b5ead-113">Una firma desasociada se utilizaría normalmente si el destinatario de la firma tiene una copia del texto con firma exacto.</span><span class="sxs-lookup"><span data-stu-id="b5ead-113">A detached signature would most often be used if the recipient of the signature has a copy of the exact signed text.</span></span> <span data-ttu-id="b5ead-114">En el ejemplo siguiente, el mensaje original y la firma desasociada se escriben en archivos independientes.</span><span class="sxs-lookup"><span data-stu-id="b5ead-114">In the example below, the original message and the detached signature are written to separate files.</span></span>

<span data-ttu-id="b5ead-115">En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="b5ead-115">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="b5ead-116">Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="b5ead-116">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="b5ead-117">Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b5ead-117">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="b5ead-118">Al crear una firma se usa la [*clave privada*](../secgloss/p-gly.md)del firmante.</span><span class="sxs-lookup"><span data-stu-id="b5ead-118">Creating a signature uses the signer's [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="b5ead-119">Solo se puede crear una firma si está disponible el certificado del firmante con una clave privada asociada.</span><span class="sxs-lookup"><span data-stu-id="b5ead-119">A signature can only be created if the signer's certificate with an associated private key is available.</span></span> <span data-ttu-id="b5ead-120">Este ejemplo del método **Sign** no especifica un firmante.</span><span class="sxs-lookup"><span data-stu-id="b5ead-120">This example of the **Sign** method does not specify a signer.</span></span> <span data-ttu-id="b5ead-121">Si no se especifica un firmante y ningún certificado de **CAPICOM \_ My \_ Store** tiene una clave privada asociada, se produce un error en el método **Sign** .</span><span class="sxs-lookup"><span data-stu-id="b5ead-121">If a signer is not specified and no certificate in **CAPICOM\_MY\_STORE** has an associated private key, the **Sign** method fails.</span></span> <span data-ttu-id="b5ead-122">Si un solo certificado de **CAPICOM \_ My \_ Store** tiene una clave privada asociada, el certificado y su clave privada se usan para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="b5ead-122">If one and only one certificate in **CAPICOM\_MY\_STORE** has an associated private key, that certificate and its private key is used to create the signature.</span></span> <span data-ttu-id="b5ead-123">Si hay más de un certificado en la tienda **CAPICOM \_ My \_ Store** que tiene una clave privada asociada, aparece un cuadro de diálogo y el usuario puede elegir el certificado que se usará para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="b5ead-123">If more than one certificate in the **CAPICOM\_MY\_STORE** store has an associated private key, a dialog box appears and the user can choose the certificate to be used to create the signature.</span></span>

<span data-ttu-id="b5ead-124">Cuando una aplicación basada en Web usa el método **Sign** , siempre se muestra un mensaje y se requiere el permiso del usuario antes de crear una firma que use la clave privada de dicho firmante.</span><span class="sxs-lookup"><span data-stu-id="b5ead-124">When a web-based application uses the **Sign** method, a prompt is always displayed and the user's permission is required before a signature that uses that signer's private key is created.</span></span>


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="b5ead-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5ead-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5ead-126">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="b5ead-126">**Store.Open**</span></span>](store-open.md)
</dt> <dt>

[<span data-ttu-id="b5ead-127">**Certificado de firmante**</span><span class="sxs-lookup"><span data-stu-id="b5ead-127">**Signer.Certificate**</span></span>](signer-certificate.md)
</dt> <dt>

[<span data-ttu-id="b5ead-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b5ead-128">**Attribute**</span></span>](attribute.md)
</dt> <dt>

[<span data-ttu-id="b5ead-129">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="b5ead-129">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
