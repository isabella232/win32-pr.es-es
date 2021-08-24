---
description: En este tema se describe cómo usar las interfaces que proporcionan acceso a las partes del documento XPS en un OM xps.
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: Interfaces de elemento DE OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc93023f251d96f557dfc351949b58f7b9a0b67d308903d83b182de8f710e110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823905"
---
# <a name="xps-om-part-interfaces"></a>Interfaces de elemento DE OM XPS

En este tema se describe cómo usar las interfaces que proporcionan acceso a las partes del documento XPS en un OM xps.



| Nombre de interfaz                                                                                                    | Interfaces secundarias lógicas                                                                                                                                                                                                                                                                                     | Descripción                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPart**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | Componentes de documento que son la estructura del documento.<br/>                                          |
| [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | IXpsOMFontResource<br/> IXpsOMImageResource<br/> IXpsOMColorProfileResource<br/> IXpsOMPrintTicketResource<br/> IXpsOMRemoteDictionaryResource<br/> IXpsOMDocumentStructureResource<br/> IXpsOMStoryFragmentsResource<br/> IXpsOMSignatureBlockResource<br/> | Componentes de documento que contienen elementos que se usan en una página o un documento o a los que hace referencia.<br/> |
| [**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | Ninguno<br/>                                                                                                                                                                                                                                                                                              | Colección de URI de partes.<br/>                                                                        |



 

## <a name="code-examples"></a>Ejemplos de código

Los ejemplos de código siguientes muestran dos ejemplos de cómo usar las interfaces de elemento para acceder al contenido de XPS OM.

### <a name="get-the-name-of-a-document-part"></a>Obtener el nombre de un elemento de documento

En el ejemplo de código siguiente se navega a un elemento de documento y se obtiene el nombre de la parte.


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Obtener los recursos de elemento asociados a esta página

En el ejemplo de código siguiente se obtienen las listas de los distintos recursos que usa esta página.


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



 

