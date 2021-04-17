---
description: En este tema se describe cómo agregar una solicitud de firma a un documento XPS.
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: Agregar una solicitud de firma a un documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697515"
---
# <a name="add-a-signature-request-to-an-xps-document"></a><span data-ttu-id="67909-103">Agregar una solicitud de firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="67909-103">Add a Signature Request to an XPS Document</span></span>

<span data-ttu-id="67909-104">En este tema se describe cómo agregar una solicitud de firma a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="67909-104">This topic describes how to add a signature request to an XPS document.</span></span> <span data-ttu-id="67909-105">Una solicitud de firma solicita a un usuario que firme un documento si está de acuerdo con el intento de firma.</span><span class="sxs-lookup"><span data-stu-id="67909-105">A signature request prompts a user to sign a document if he or she agrees with the signature intent.</span></span>

<span data-ttu-id="67909-106">Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="67909-106">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="67909-107">Para agregar una solicitud de firma a un documento XPS:</span><span class="sxs-lookup"><span data-stu-id="67909-107">To add a signature request to an XPS Document:</span></span>

1.  <span data-ttu-id="67909-108">Cargue el documento XPS en un administrador de firmas, tal como se describe en [inicializar el administrador de firmas](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="67909-108">Load the XPS document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="67909-109">Agregue un bloque de firma al administrador de firmas.</span><span class="sxs-lookup"><span data-stu-id="67909-109">Add a signature block to the signature manager.</span></span>
3.  <span data-ttu-id="67909-110">Cree una solicitud de firma en el nuevo bloque de firma.</span><span class="sxs-lookup"><span data-stu-id="67909-110">Create a signature request in the new signature block.</span></span>
4.  <span data-ttu-id="67909-111">Establezca las propiedades de la solicitud de firma:</span><span class="sxs-lookup"><span data-stu-id="67909-111">Set the properties of the signature request:</span></span>
    1.  <span data-ttu-id="67909-112">Establezca la intención de la firma.</span><span class="sxs-lookup"><span data-stu-id="67909-112">Set the signature intent.</span></span>
    2.  <span data-ttu-id="67909-113">Establezca el nombre de la persona cuya firma se solicita (el firmante solicitado).</span><span class="sxs-lookup"><span data-stu-id="67909-113">Set the name of the person whose signature is requested (the requested signer).</span></span>
    3.  <span data-ttu-id="67909-114">Establece la fecha en la que se requiere la firma.</span><span class="sxs-lookup"><span data-stu-id="67909-114">Set the date the signature is required.</span></span>
    4.  <span data-ttu-id="67909-115">Establezca otras propiedades de la firma según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="67909-115">Set other signature properties as required.</span></span>

<span data-ttu-id="67909-116">En el ejemplo de código siguiente se muestra cómo agregar una solicitud de firma a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="67909-116">The following code example illustrates how to add a signature request to an XPS document.</span></span>


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="67909-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67909-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67909-118">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="67909-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="67909-119">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="67909-119">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[<span data-ttu-id="67909-120">**IXpsSignatureBlock::CreateRequest**</span><span class="sxs-lookup"><span data-stu-id="67909-120">**IXpsSignatureBlock::CreateRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[<span data-ttu-id="67909-121">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="67909-121">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="67909-122">**IXpsSignatureManager::AddSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="67909-122">**IXpsSignatureManager::AddSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[<span data-ttu-id="67909-123">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="67909-123">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[<span data-ttu-id="67909-124">**IXpsSignatureRequest::SetIntent**</span><span class="sxs-lookup"><span data-stu-id="67909-124">**IXpsSignatureRequest::SetIntent**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[<span data-ttu-id="67909-125">**IXpsSignatureRequest::SetRequestedSigner**</span><span class="sxs-lookup"><span data-stu-id="67909-125">**IXpsSignatureRequest::SetRequestedSigner**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[<span data-ttu-id="67909-126">**IXpsSignatureRequest::SetRequestSignByDate**</span><span class="sxs-lookup"><span data-stu-id="67909-126">**IXpsSignatureRequest::SetRequestSignByDate**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

<span data-ttu-id="67909-127">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="67909-127">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="67909-128">Errores de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="67909-128">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="67909-129">Errores de documento XPS</span><span class="sxs-lookup"><span data-stu-id="67909-129">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="67909-130">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="67909-130">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



