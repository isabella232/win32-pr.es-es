---
description: Describe cómo escribir el contenido de una OM XPS en un programa en un archivo de documento XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Escribir una OM xps en un documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f6ef79f592ad241e54e9a01fb5e4fe72cc41573e75c78f347109cdfb1c6f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098562"
---
# <a name="write-an-xps-om-to-an-xps-document"></a>Escribir una OM xps en un documento XPS

Describe cómo escribir el contenido de una OM XPS en un programa en un archivo de documento XPS.

Si un programa tiene un XPS OM que contiene un documento completo, el programa puede escribir la OM XPS en un archivo como un documento XPS, llamando al método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de la [**interfaz IXpsOMPackage.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)

Antes de usar estos ejemplos de código en un programa, lea la declinación de responsabilidades en [Tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>Escritura de una om XPS completa en un documento XPS

Después de establecer el contenido de una OM XPS, puede guardar la OM xps en un archivo como un documento XPS, llamando al método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de la interfaz [**IXpsOMPackage.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> La escritura de una OM xps en un archivo o secuencia no crea automáticamente una miniatura para el documento XPS. Para crear una miniatura del documento XPS, use la [**interfaz IXpsOMThumbnailGenerator.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)

 

## <a name="incrementally-writing-an-xps-document"></a>Escritura incremental de un documento XPS

La [**interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) se puede usar para escribir las partes de un documento XPS de forma incremental; por ejemplo, cuando los elementos del documento se crean o procesan en secuencia.

> [!Note]  
> La escritura de una OM xps en un archivo o secuencia no crea automáticamente una miniatura para el documento XPS. Para crear una miniatura del documento XPS, use la [**interfaz IXpsOMThumbnailGenerator.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Imprimir una OM XPS](print-an-xps-om.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Inicialización de una om xps](xps-object-model-initialization.md)
</dt> <dt>

[Referencia de document API de XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
