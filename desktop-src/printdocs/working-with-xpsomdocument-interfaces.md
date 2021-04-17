---
description: En este tema se describen las interfaces que proporcionan acceso a los componentes de nivel de documento de un OM XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Trabajar con interfaces IXpsOMDocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697126"
---
# <a name="working-with-ixpsomdocument-interfaces"></a><span data-ttu-id="44e8c-103">Trabajar con interfaces IXpsOMDocument</span><span class="sxs-lookup"><span data-stu-id="44e8c-103">Working with IXpsOMDocument Interfaces</span></span>

<span data-ttu-id="44e8c-104">En este tema se describen las interfaces que proporcionan acceso a los componentes de nivel de documento de un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="44e8c-104">This topic describes the interfaces that provide access to the document-level components of an XPS OM.</span></span>



| <span data-ttu-id="44e8c-105">Nombre de interfaz</span><span class="sxs-lookup"><span data-stu-id="44e8c-105">Interface name</span></span>                                                                        | <span data-ttu-id="44e8c-106">Interfaces secundarias lógicas</span><span class="sxs-lookup"><span data-stu-id="44e8c-106">Logical child interfaces</span></span>                                      | <span data-ttu-id="44e8c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="44e8c-107">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44e8c-108">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="44e8c-108">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [<span data-ttu-id="44e8c-109">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="44e8c-109">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | <span data-ttu-id="44e8c-110">Representa una única parte de FixedDocument y enlaza una colección de referencias de página.</span><span class="sxs-lookup"><span data-stu-id="44e8c-110">Represents a single FixedDocument part and binds a collection of page references.</span></span><br/> <span data-ttu-id="44e8c-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) es la interfaz de colección que se usa para recorrer en iteración las interfaces de [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) en un documento.</span><span class="sxs-lookup"><span data-stu-id="44e8c-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) is the collection interface that is used to iterate through the [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces in a document.</span></span><br/> |
| [<span data-ttu-id="44e8c-112">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="44e8c-112">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | <span data-ttu-id="44e8c-113">None</span><span class="sxs-lookup"><span data-stu-id="44e8c-113">None</span></span><br/>                                               | <span data-ttu-id="44e8c-114">Representa la parte DocumentStructure.</span><span class="sxs-lookup"><span data-stu-id="44e8c-114">Represents the DocumentStructure part.</span></span><br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a><span data-ttu-id="44e8c-115">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="44e8c-115">Code Examples</span></span>

<span data-ttu-id="44e8c-116">Los ejemplos de código de esta sección muestran cómo se usan algunas de las interfaces de documento en un programa.</span><span class="sxs-lookup"><span data-stu-id="44e8c-116">The code examples in this section illustrate how some of the document interfaces are used in a program.</span></span>

### <a name="get-the-page-references-of-a-document"></a><span data-ttu-id="44e8c-117">Obtener las referencias de página de un documento</span><span class="sxs-lookup"><span data-stu-id="44e8c-117">Get the page references of a document</span></span>

<span data-ttu-id="44e8c-118">En el ejemplo de código siguiente se obtiene un puntero al [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) que contiene la lista de interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) para el documento al que hace referencia el parámetro de *documento* .</span><span class="sxs-lookup"><span data-stu-id="44e8c-118">The following code example gets a pointer to the [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) that contains the list of [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces for the document that is referenced by *doc* parameter.</span></span>


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a><span data-ttu-id="44e8c-119">Obtener la estructura de un documento</span><span class="sxs-lookup"><span data-stu-id="44e8c-119">Get the document structure of a document</span></span>

<span data-ttu-id="44e8c-120">En el ejemplo de código siguiente se obtiene el recurso que contiene la estructura del documento.</span><span class="sxs-lookup"><span data-stu-id="44e8c-120">The following code example gets the resource that contains the document structure.</span></span>


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 




