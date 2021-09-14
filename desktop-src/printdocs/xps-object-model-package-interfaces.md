---
description: Las interfaces de paquete representan el nivel superior de XPS OM, que corresponde a un archivo de documento XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfaces de paquete DE OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168021"
---
# <a name="xps-om-package-interfaces"></a>Interfaces de paquete DE OM XPS

Las interfaces de paquete representan el nivel superior de XPS OM, que corresponde a un archivo de documento XPS. Estas interfaces contienen métodos que serializan una OM XPS en un documento XPS o una secuencia, y deserializan un paquete XPS para crear una OM XPS que permite que un programa acceda al contenido de un documento.



| Nombre de interfaz                                                  | Interfaces secundarias lógicas                                                                                                            | Descripción                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | La OM XPS completa que corresponde al paquete que contiene el documento XPS.<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | None<br/>                                                                                                                     | Habilita la serialización incremental de páginas de documento en un paquete.<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | None<br/>                                                                                                                     | Accede a los metadatos del documento. <br/>                                                    |



 

## <a name="code-examples"></a>Ejemplos de código

Los ejemplos de código siguientes muestran cómo un programa usa algunas de las interfaces de paquete. A menos que se indique lo contrario, todos los elementos en cursiva son nombres de parámetro.

-   [Lectura de un documento XPS en una om xps](#read-an-xps-document-into-an-xps-om)
-   [Escritura de una OM xps en un archivo de documento XPS](#write-an-xps-om-to-an-xps-document-file)
-   [Acceso a la secuencia de documentos de XPS OM](#access-the-document-sequence-of-the-xps-om)
-   [Acceso a CoreProperties del documento](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Lectura de un documento XPS en una om xps

A partir de un documento XPS existente cuyo nombre de archivo se almacena en *xpsDocumentFilename*, en este ejemplo de código se crea un OM XPS al que hace referencia *xpsPackage*.


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Escritura de una OM xps en un archivo de documento XPS

En el ejemplo de código siguiente se escribe la OM xpS a la que hace referencia *xpsPackage*. En el ejemplo se crea un documento XPS en el archivo cuyo nombre se almacena en *fileName*.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Acceso a la secuencia de documentos de XPS OM

En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMDocumentSequence,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contiene la secuencia de documento del OM xpS representado por *xpsPackage*.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a>Acceso a CoreProperties del documento

El ejemplo de código siguiente obtiene un puntero a la interfaz [**IXpsOMCoreProperties,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) lo que permite al programa acceder al contenido de la parte CoreProperties. En el ejemplo, se supone que el documento se ha leído en una OM XPS representada por *xpsPackage*.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la interfaz IXpsOMPackageWriter](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[Navegar por XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[**IXpsOMDocumentSequence (Interfaz)**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPackage (interfaz)**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter (Interfaz)**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Interfaz IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




