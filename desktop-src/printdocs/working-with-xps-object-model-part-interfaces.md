---
description: En este tema se describe cómo usar las interfaces que proporcionan acceso a los elementos de documento XPS en un OM XPS.
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: Interfaces de elementos de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81cbf17c26e4ba6c80199ee787b1ee11b28d260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001836"
---
# <a name="xps-om-part-interfaces"></a><span data-ttu-id="205a6-103">Interfaces de elementos de XPS OM</span><span class="sxs-lookup"><span data-stu-id="205a6-103">XPS OM Part Interfaces</span></span>

<span data-ttu-id="205a6-104">En este tema se describe cómo usar las interfaces que proporcionan acceso a los elementos de documento XPS en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="205a6-104">This topic describes how to use the interfaces that provide access to XPS document parts in an XPS OM.</span></span>



| <span data-ttu-id="205a6-105">Nombre de interfaz</span><span class="sxs-lookup"><span data-stu-id="205a6-105">Interface name</span></span>                                                                                                    | <span data-ttu-id="205a6-106">Interfaces secundarias lógicas</span><span class="sxs-lookup"><span data-stu-id="205a6-106">Logical child interfaces</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="205a6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="205a6-107">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="205a6-108">**IXpsOMPart**</span><span class="sxs-lookup"><span data-stu-id="205a6-108">**IXpsOMPart**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [<span data-ttu-id="205a6-109">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="205a6-109">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="205a6-110">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="205a6-110">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [<span data-ttu-id="205a6-111">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="205a6-111">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [<span data-ttu-id="205a6-112">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="205a6-112">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [<span data-ttu-id="205a6-113">**IXpsOMResource**</span><span class="sxs-lookup"><span data-stu-id="205a6-113">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | <span data-ttu-id="205a6-114">Componentes de documento que componen la estructura del documento.</span><span class="sxs-lookup"><span data-stu-id="205a6-114">Document components that make up the document structure.</span></span><br/>                                          |
| [<span data-ttu-id="205a6-115">**IXpsOMResource**</span><span class="sxs-lookup"><span data-stu-id="205a6-115">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [<span data-ttu-id="205a6-116">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="205a6-116">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | <span data-ttu-id="205a6-117">IXpsOMFontResource</span><span class="sxs-lookup"><span data-stu-id="205a6-117">IXpsOMFontResource</span></span><br/> <span data-ttu-id="205a6-118">IXpsOMImageResource</span><span class="sxs-lookup"><span data-stu-id="205a6-118">IXpsOMImageResource</span></span><br/> <span data-ttu-id="205a6-119">IXpsOMColorProfileResource</span><span class="sxs-lookup"><span data-stu-id="205a6-119">IXpsOMColorProfileResource</span></span><br/> <span data-ttu-id="205a6-120">IXpsOMPrintTicketResource</span><span class="sxs-lookup"><span data-stu-id="205a6-120">IXpsOMPrintTicketResource</span></span><br/> <span data-ttu-id="205a6-121">IXpsOMRemoteDictionaryResource</span><span class="sxs-lookup"><span data-stu-id="205a6-121">IXpsOMRemoteDictionaryResource</span></span><br/> <span data-ttu-id="205a6-122">IXpsOMDocumentStructureResource</span><span class="sxs-lookup"><span data-stu-id="205a6-122">IXpsOMDocumentStructureResource</span></span><br/> <span data-ttu-id="205a6-123">IXpsOMStoryFragmentsResource</span><span class="sxs-lookup"><span data-stu-id="205a6-123">IXpsOMStoryFragmentsResource</span></span><br/> <span data-ttu-id="205a6-124">IXpsOMSignatureBlockResource</span><span class="sxs-lookup"><span data-stu-id="205a6-124">IXpsOMSignatureBlockResource</span></span><br/> | <span data-ttu-id="205a6-125">Componentes de documento que contienen elementos que se usan en una página o un documento o a los que se hace referencia en ella.</span><span class="sxs-lookup"><span data-stu-id="205a6-125">Document components that contain elements that are used in or referenced by a page or a document.</span></span><br/> |
| [<span data-ttu-id="205a6-126">**IXpsOMPartUriCollection**</span><span class="sxs-lookup"><span data-stu-id="205a6-126">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | <span data-ttu-id="205a6-127">None</span><span class="sxs-lookup"><span data-stu-id="205a6-127">None</span></span><br/>                                                                                                                                                                                                                                                                                              | <span data-ttu-id="205a6-128">Colección de identificadores URI de partes.</span><span class="sxs-lookup"><span data-stu-id="205a6-128">A collection of part URIs.</span></span><br/>                                                                        |



 

## <a name="code-examples"></a><span data-ttu-id="205a6-129">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="205a6-129">Code Examples</span></span>

<span data-ttu-id="205a6-130">En los ejemplos de código siguientes se muestran dos ejemplos de cómo usar las interfaces de elementos para tener acceso al contenido XPS OM.</span><span class="sxs-lookup"><span data-stu-id="205a6-130">The code examples that follow show two examples of how to use the part interfaces to access XPS OM content.</span></span>

### <a name="get-the-name-of-a-document-part"></a><span data-ttu-id="205a6-131">Obtener el nombre de un elemento de documento</span><span class="sxs-lookup"><span data-stu-id="205a6-131">Get the name of a document part</span></span>

<span data-ttu-id="205a6-132">En el ejemplo de código siguiente se navega a una parte del documento y se obtiene el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="205a6-132">The following code example navigates to a document part and gets the part's name.</span></span>


```C++
    HRESULT                         hr = S_OK;
    
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;
    IXpsOMPageReferenceCollection   *pages;
    IXpsOMPageReference             *pageRef;
    IXpsOMPage                      *page;

    IOpcPartUri                     *thisDocPartUri;
    IOpcPartUri                     *thisPagePartUri;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // package points to the IXpsOMPackage interface to walk.

    // get the fixed document sequence of the package
    hr = package->GetDocumentSequence(&docSeq);

    // get the fixed documents in the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // get the part name (URI) of this document
        hr = doc->GetPartName ( &thisDocPartUri );

        // get the doc contents
        hr = doc->GetPageReferences(&pages);
        
        // walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // get this page reference
            hr = pages->GetAt(thisPageRef, &pageRef );

            // get the part name (URI) of this page
            hr = pageRef->GetPage (&page);
            hr = page->GetPartName ( &thisPagePartUri );

            // do something with the part name
 
            thisPagePartUri->Release();
            page->Release();
            pageRef->Release();

            thisPageRef++;
        }
        pages->Release();
        thisDocPartUri->Release();
        doc->Release();
        thisDoc++;
    }

    docs->Release();
    docSeq->Release();

```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="205a6-133">Obtener los recursos del elemento que están asociados a esta página</span><span class="sxs-lookup"><span data-stu-id="205a6-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="205a6-134">En el ejemplo de código siguiente se obtienen las listas de los distintos recursos utilizados por esta página.</span><span class="sxs-lookup"><span data-stu-id="205a6-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );

    // use resources

    dictionaryResources->Release();
    imageResources->Release();
    fontResources->Release();
    colorProfileResources->Release();
    resources->Release();
```



 

