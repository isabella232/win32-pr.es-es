---
description: En este tema se describen las interfaces que proporcionan acceso a los componentes de nivel de documento de una OM XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Trabajar con interfaces IXpsOMDocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241143"
---
# <a name="working-with-ixpsomdocument-interfaces"></a>Trabajar con interfaces IXpsOMDocument

En este tema se describen las interfaces que proporcionan acceso a los componentes de nivel de documento de una OM XPS.



| Nombre de interfaz                                                                        | Interfaces secundarias lógicas                                      | Descripción                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Representa un único elemento FixedDocument y enlaza una colección de referencias de página.<br/> [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) es la interfaz de colección que se usa para recorrer en iteración las [**interfaces IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) de un documento.<br/> |
| [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | None<br/>                                               | Representa la parte DocumentStructure.<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a>Ejemplos de código

Los ejemplos de código de esta sección muestran cómo se usan algunas de las interfaces de documento en un programa.

### <a name="get-the-page-references-of-a-document"></a>Obtener las referencias de página de un documento

En el ejemplo de código siguiente se obtiene un puntero a [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) que contiene la lista de interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) para el documento al que hace referencia el parámetro *doc.*


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



### <a name="get-the-document-structure-of-a-document"></a>Obtener la estructura del documento de un documento

En el ejemplo de código siguiente se obtiene el recurso que contiene la estructura del documento.


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



 

 




