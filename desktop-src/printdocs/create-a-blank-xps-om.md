---
description: En este tema se describe cómo crear un OM XPS en blanco.
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: Crear un OM XPS en blanco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0588fc11deb4b3d980e978dfe8a5370bc170d506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706309"
---
# <a name="create-a-blank-xps-om"></a><span data-ttu-id="797c7-103">Crear un OM XPS en blanco</span><span class="sxs-lookup"><span data-stu-id="797c7-103">Create a Blank XPS OM</span></span>

<span data-ttu-id="797c7-104">En este tema se describe cómo crear un OM XPS en blanco.</span><span class="sxs-lookup"><span data-stu-id="797c7-104">This topic describes how to create a blank XPS OM.</span></span> <span data-ttu-id="797c7-105">Presenta los ejemplos de código que muestran cómo usar un OM XPS para crear la estructura de documento de un documento XPS con una página en blanco.</span><span class="sxs-lookup"><span data-stu-id="797c7-105">It presents the code examples that illustrate how to use an XPS OM to build the document structure of an XPS document that has one blank page.</span></span>

<span data-ttu-id="797c7-106">Para que se guarde como un documento XPS, el OM de XPS requiere al menos los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="797c7-106">To be saved as an XPS document, the XPS OM requires at least the following components:</span></span>

-   <span data-ttu-id="797c7-107">Un [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) que describe el paquete de documento XPS</span><span class="sxs-lookup"><span data-stu-id="797c7-107">An [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) that describes the XPS document package</span></span>
-   <span data-ttu-id="797c7-108">Un [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contiene el marco del contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="797c7-108">An [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) that contains the framework of the package contents</span></span>
-   <span data-ttu-id="797c7-109">Un [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) que contiene el marco de un documento dentro del paquete.</span><span class="sxs-lookup"><span data-stu-id="797c7-109">An [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) that contains the framework of a document within the package</span></span>
-   <span data-ttu-id="797c7-110">[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) que contiene la colección de páginas del documento.</span><span class="sxs-lookup"><span data-stu-id="797c7-110">An [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) that contains the collection of pages in the document</span></span>
-   <span data-ttu-id="797c7-111">Un [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que contiene una página en blanco</span><span class="sxs-lookup"><span data-stu-id="797c7-111">An [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) that contains a blank page</span></span>

<span data-ttu-id="797c7-112">Cuando se usan estas interfaces, el OM de XPS contendrá un documento con una página en blanco.</span><span class="sxs-lookup"><span data-stu-id="797c7-112">When these interfaces are used, the XPS OM will contain a document that has one blank page.</span></span> <span data-ttu-id="797c7-113">Para crear este documento en un OM XPS, el programa primero debe crear los componentes individuales y vincularlos juntos.</span><span class="sxs-lookup"><span data-stu-id="797c7-113">To create this document in an XPS OM, the program must first create the individual components and then link them together.</span></span>

<span data-ttu-id="797c7-114">Antes de usar los ejemplos de código siguientes, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="797c7-114">Before using the following code examples, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-examples"></a><span data-ttu-id="797c7-115">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="797c7-115">Code Examples</span></span>

<span data-ttu-id="797c7-116">En el ejemplo de código siguiente se da por supuesto que la inicialización, descrita en [inicializar un OM XPS](xps-object-model-initialization.md), se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="797c7-116">The following code example assumes that the initialization, described in [Initialize an XPS OM](xps-object-model-initialization.md), has succeeded.</span></span>


```C++
    // Declare the variables used in this section.
    HRESULT                       hr = S_OK;
    IOpcPartUri                   *opcPartUri = NULL;
    IXpsOMPackage                 *xpsPackage = NULL;
    IXpsOMDocumentSequence        *xpsFDS = NULL;
    IXpsOMDocumentCollection      *fixedDocuments = NULL;
    IXpsOMDocument                *xpsFD = NULL;
    IXpsOMPage                    *xpsPage = NULL;
    IXpsOMPageReferenceCollection *pageRefs = NULL;
    IXpsOMPageReference           *xpsPageRef = NULL;
    // These values are set outside of this code example.
    XPS_SIZE pageSize = {width, height}; 
    
    // Create the package.
    hr = xpsFactory->CreatePackage( &xpsPackage );

    // Create the URI for the fixed document sequence part and then  
    //  create the fixed document sequence
    hr = xpsFactory->CreatePartUri( 
        L"/FixedDocumentSequence.fdseq", &opcPartUri );
    hr = xpsFactory->CreateDocumentSequence( opcPartUri, &xpsFDS );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create the URI for the document part and then create the document.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/FixedDocument.fdoc", &opcPartUri );
    hr = xpsFactory->CreateDocument( opcPartUri, &xpsFD );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a blank page.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/Pages/1.fpage", &opcPartUri );
    hr = xpsFactory->CreatePage(
        &pageSize,                  // Page size
        L"en-US",                   // Page language
        opcPartUri,                 // Page part name
        &xpsPage);                
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a page reference for the page.
    hr = xpsFactory->CreatePageReference( &pageSize, &xpsPageRef );

    // Add the fixed document sequence to the package.
    hr = xpsPackage->SetDocumentSequence( xpsFDS );

    // Get the document collection of the fixed document sequence
    //  and then add the document to the collection.
    hr = xpsFDS->GetDocuments( &fixedDocuments );
    hr = fixedDocuments->Append( xpsFD );

    // Get the page reference collection from the document
    //  and add the page reference and blank page.
    hr = xpsFD->GetPageReferences( &pageRefs );
    hr = pageRefs->Append( xpsPageRef );
    hr = xpsPageRef->SetPage( xpsPage );

    // Release interface pointer
    if (NULL != xpsPage) xpsPage->Release();
    if (NULL != pageRefs) pageRefs->Release();
    if (NULL != fixedDocuments) fixedDocuments->Release();
    if (NULL != xpsPageRef) xpsPageRef->Release();
    if (NULL != xpsFD) xpsFD->Release();
    if (NULL != xpsFDS) xpsFDS->Release();
    if (NULL != xpsPackage) xpsPackage->Release();

```



## <a name="best-practices"></a><span data-ttu-id="797c7-117">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="797c7-117">Best Practices</span></span>

<span data-ttu-id="797c7-118">Después de usar una interfaz [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) para crear un componente (por ejemplo, después de llamar al método **CreateDocument** en el ejemplo de código), libere el puntero a esa interfaz, a menos que lo necesite para otra llamada.</span><span class="sxs-lookup"><span data-stu-id="797c7-118">After you have used an [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) interface to create a component (such as after calling the **CreateDocument** method in the code example), release the pointer to that interface—unless you need it for another call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="797c7-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="797c7-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="797c7-120">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="797c7-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="797c7-121">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="797c7-121">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="797c7-122">Escribir texto en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="797c7-122">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="797c7-123">Dibujar gráficos en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="797c7-123">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="797c7-124">Colocar imágenes en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="797c7-124">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="797c7-125">**Se usa en esta página**</span><span class="sxs-lookup"><span data-stu-id="797c7-125">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="797c7-126">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="797c7-126">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="797c7-127">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="797c7-127">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="797c7-128">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="797c7-128">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="797c7-129">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="797c7-129">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="797c7-130">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="797c7-130">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="797c7-131">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="797c7-131">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="797c7-132">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="797c7-132">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="797c7-133">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="797c7-133">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="797c7-134">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="797c7-134">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="797c7-135">**tamaño de XPS \_**</span><span class="sxs-lookup"><span data-stu-id="797c7-135">**XPS\_SIZE**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

<span data-ttu-id="797c7-136">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="797c7-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="797c7-137">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="797c7-137">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="797c7-138">API de empaquetado</span><span class="sxs-lookup"><span data-stu-id="797c7-138">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="797c7-139">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="797c7-139">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="797c7-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="797c7-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
