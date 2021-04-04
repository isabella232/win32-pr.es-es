---
description: Las interfaces de paquete representan el nivel superior del OM de XPS, que corresponde a un archivo de documento XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfaces de paquetes de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908624"
---
# <a name="xps-om-package-interfaces"></a>Interfaces de paquetes de XPS OM

Las interfaces de paquete representan el nivel superior del OM de XPS, que corresponde a un archivo de documento XPS. Estas interfaces contienen métodos que serializan un OM XPS en un documento o secuencia XPS y deserializan un paquete XPS para crear un OM XPS que permite a un programa tener acceso al contenido de un documento.



| Nombre de interfaz                                                  | Interfaces secundarias lógicas                                                                                                            | Descripción                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | El OM XPS completo que corresponde al paquete que contiene el documento XPS.<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | None<br/>                                                                                                                     | Habilita la serialización incremental de las páginas del documento en un paquete.<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | None<br/>                                                                                                                     | Obtiene acceso a los metadatos del documento. <br/>                                                    |



 

## <a name="code-examples"></a>Ejemplos de código

En los ejemplos de código siguientes se muestra cómo se usan algunas de las interfaces de paquetes en un programa. A menos que se indique lo contrario, todos los elementos en cursiva son nombres de parámetro.

-   [Leer un documento XPS en un OM XPS](#read-an-xps-document-into-an-xps-om)
-   [Escribir un OM XPS en un archivo de documento XPS](#write-an-xps-om-to-an-xps-document-file)
-   [Obtener acceso a la secuencia de documentos del OM de XPS](#access-the-document-sequence-of-the-xps-om)
-   [Acceder al CoreProperties del documento](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Leer un documento XPS en un OM XPS

A partir de un documento XPS existente cuyo nombre de archivo está almacenado en *xpsDocumentFilename*, en este ejemplo de código se crea un OM XPS al que hace referencia *xpsPackage*.


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



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Escribir un OM XPS en un archivo de documento XPS

En el ejemplo de código siguiente se escribe el OM XPS al que hace referencia *xpsPackage*. En el ejemplo se crea un documento XPS en el archivo cuyo nombre se almacena en *filename*.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Obtener acceso a la secuencia de documentos del OM de XPS

En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , que contiene la secuencia de documento del OM XPS que se representa mediante *xpsPackage*.


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



### <a name="access-the-documents-coreproperties"></a>Acceder al CoreProperties del documento

En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , lo que permite que el programa tenga acceso al contenido del elemento CoreProperties. En el ejemplo, se supone que se ha leído el documento en un OM XPS representado por *xpsPackage*.


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

[Navegar por el OM de XPS](navigate-the-xps-om.md)
</dt> <dt>

[**Interfaz IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Interfaz IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Interfaz IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




