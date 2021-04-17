---
description: En este tema se describe cómo usar las interfaces que proporcionan acceso a la FixedDocumentSequence, que es el nivel superior de la jerarquía de documentos en un OM XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Trabajar con interfaces IXpsOMDocumentSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f108cbadf735b334f758102915abbda239a4e974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697270"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a><span data-ttu-id="ad1d7-103">Trabajar con interfaces IXpsOMDocumentSequence</span><span class="sxs-lookup"><span data-stu-id="ad1d7-103">Working with IXpsOMDocumentSequence Interfaces</span></span>

<span data-ttu-id="ad1d7-104">En este tema se describe cómo usar las interfaces que proporcionan acceso a la FixedDocumentSequence, que es el nivel superior de la jerarquía de documentos en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="ad1d7-104">This topic describes how to use the interfaces that provide access to the FixedDocumentSequence, which is the top level of the document hierarchy in an XPS OM.</span></span>



| <span data-ttu-id="ad1d7-105">Nombre de interfaz</span><span class="sxs-lookup"><span data-stu-id="ad1d7-105">Interface name</span></span>                                                          | <span data-ttu-id="ad1d7-106">Interfaces secundarias lógicas</span><span class="sxs-lookup"><span data-stu-id="ad1d7-106">Logical child interfaces</span></span>                            | <span data-ttu-id="ad1d7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad1d7-107">Description</span></span>                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="ad1d7-108">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="ad1d7-108">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [<span data-ttu-id="ad1d7-109">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="ad1d7-109">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | <span data-ttu-id="ad1d7-110">Agrupa un conjunto de FixedDocuments en una lista ordenada.</span><span class="sxs-lookup"><span data-stu-id="ad1d7-110">Groups a set of FixedDocuments into an ordered list.</span></span><br/>          |
| [<span data-ttu-id="ad1d7-111">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="ad1d7-111">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | <span data-ttu-id="ad1d7-112">None</span><span class="sxs-lookup"><span data-stu-id="ad1d7-112">None</span></span><br/>                                     | <span data-ttu-id="ad1d7-113">Colección de FixedDocuments en una secuencia de documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="ad1d7-113">The collection of FixedDocuments in an XPS document sequence.</span></span><br/> |



 

## <a name="code-example"></a><span data-ttu-id="ad1d7-114">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="ad1d7-114">Code Example</span></span>

<span data-ttu-id="ad1d7-115">En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contiene la secuencia de documento del OM XPS que se representa mediante *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="ad1d7-115">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface that contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span> <span data-ttu-id="ad1d7-116">A continuación, en el ejemplo se enumeran los documentos de la colección.</span><span class="sxs-lookup"><span data-stu-id="ad1d7-116">The example then enumerates the documents in the collection.</span></span>


```C++
    HRESULT                         hr = S_OK;

    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
 
        // use this doc for something

        // release this doc and then go to the next one
        doc->Release();
        thisDoc++;
    }
    // release the document collection and
    // the document sequence
    docs->Release();
    docSeq->Release();
```



 

 




