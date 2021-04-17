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
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>Trabajar con interfaces IXpsOMDocumentSequence

En este tema se describe cómo usar las interfaces que proporcionan acceso a la FixedDocumentSequence, que es el nivel superior de la jerarquía de documentos en un OM XPS.



| Nombre de interfaz                                                          | Interfaces secundarias lógicas                            | Descripción                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | Agrupa un conjunto de FixedDocuments en una lista ordenada.<br/>          |
| [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | None<br/>                                     | Colección de FixedDocuments en una secuencia de documentos XPS.<br/> |



 

## <a name="code-example"></a>Ejemplo de código

En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contiene la secuencia de documento del OM XPS que se representa mediante *xpsPackage*. A continuación, en el ejemplo se enumeran los documentos de la colección.


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



 

 




