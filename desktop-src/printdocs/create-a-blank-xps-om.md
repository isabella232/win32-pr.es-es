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
# <a name="create-a-blank-xps-om"></a>Crear un OM XPS en blanco

En este tema se describe cómo crear un OM XPS en blanco. Presenta los ejemplos de código que muestran cómo usar un OM XPS para crear la estructura de documento de un documento XPS con una página en blanco.

Para que se guarde como un documento XPS, el OM de XPS requiere al menos los siguientes componentes:

-   Un [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) que describe el paquete de documento XPS
-   Un [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contiene el marco del contenido del paquete.
-   Un [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) que contiene el marco de un documento dentro del paquete.
-   [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) que contiene la colección de páginas del documento.
-   Un [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que contiene una página en blanco

Cuando se usan estas interfaces, el OM de XPS contendrá un documento con una página en blanco. Para crear este documento en un OM XPS, el programa primero debe crear los componentes individuales y vincularlos juntos.

Antes de usar los ejemplos de código siguientes, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).

## <a name="code-examples"></a>Ejemplos de código

En el ejemplo de código siguiente se da por supuesto que la inicialización, descrita en [inicializar un OM XPS](xps-object-model-initialization.md), se ha realizado correctamente.


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



## <a name="best-practices"></a>Prácticas recomendadas

Después de usar una interfaz [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) para crear un componente (por ejemplo, después de llamar al método **CreateDocument** en el ejemplo de código), libere el puntero a esa interfaz, a menos que lo necesite para otra llamada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Navegar por el OM de XPS](navigate-the-xps-om.md)
</dt> <dt>

[Escribir texto en un OM XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Dibujar gráficos en un OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Colocar imágenes en un OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Se usa en esta página**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**tamaño de XPS \_**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Inicializar un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[API de empaquetado](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Referencia de la API de documentos XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
