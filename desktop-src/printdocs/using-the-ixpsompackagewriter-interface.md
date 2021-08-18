---
description: La interfaz IXpsOMPackageWriter crea un archivo de documento XPS en el que las aplicaciones pueden escribir el contenido de las interfaces IXpsOMPage de un OM XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Uso de la interfaz IXpsOMPackageWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a4437f939821b826fa0d5c30407777b7d44c5d03c236f4ef850d52145b4f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098707"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Uso de la interfaz IXpsOMPackageWriter

La [**interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un archivo de documento XPS en el que las aplicaciones pueden escribir el contenido de las [**interfaces IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) de un OM XPS. La [**interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) es más útil cuando el contenido del documento se procesa o se crea secuencialmente. A diferencia de los métodos [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) y [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) de la interfaz [**IXpsOMPackage,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) para que la interfaz **IXpsOMPackageWriter** no se utilice, no es posible que se haya terminado ni el fixeddocument ni fixeddocumentsequence completos.

## <a name="overview"></a>Información general

La [**interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) escribe una página a la vez, desde la primera página de un documento XPS hasta la última. La interfaz se puede usar para crear archivos de documento XPS simples y también archivos de documento XPS complejos que contienen más de un fixeddocument en FixedDocumentSequence. En archivos de documento XPS complejos, los fixeddocuments también se crean en secuencia, empezando por el primer objeto FixedDocument en FixedDocumentSequence. La **interfaz IXpsOMPackageWriter** no admite la creación de contenido del documento en orden aleatorio. Úselo, por ejemplo, para crear un informe secuencial o para realizar el procesamiento en un filtro de controlador de dispositivo donde el contenido del documento se proporciona al controlador en secuencia.

## <a name="terminology-review"></a>Revisión de terminología

Un *archivo de documento XPS* es un paquete Convenciones de empaquetado abierto (OPC) que se ajusta al XML Paper Specification. Por lo tanto, técnicamente, la [**interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un paquete *OPC,* pero es un paquete OPC que se ajusta al XML Paper Specification. Por esta razón, en las discusiones sobre los documentos XPS, los términos *documento XPS* y *paquete* se suelen usar indistintamente.

El *paquete* creado por la [**interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) contendrá los componentes de documento XPS necesarios: FixedDocumentSequence, al menos un FixedDocument y al menos un FixedPage. FixedDocumentSequence se crea cuando se crea una instancia de **la interfaz IXpsOMPackageWriter.** Se crea fixeddocument cada vez que se llama a [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) y se crea un elemento FixedPage cada vez que se llama a [**IXpsOMPackageWriter::AddPage.**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) Dado que la interfaz escribe el contenido del documento secuencialmente, el **método AddPage** agrega la página al elemento FixedDocument creado más recientemente.

## <a name="using-the-ixpsompackagewriter-interface"></a>Uso de la interfaz IXpsOMPackageWriter

En el procedimiento siguiente se describe cómo crear un archivo de documento XPS mediante la [**interfaz IXpsOMPackageWriter.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) El procedimiento no describe cómo crear instancias de una [**interfaz IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) y su contenido. Para obtener más información sobre **IXpsOMPage** y agregar contenido a una página, vea [XpS OM Page Interfaces (Interfaces](xps-object-model-page-interfaces.md) de página de XPS OM) y los temas enumerados en la sección Vea también.

 **Creación de un documento**

1.  Cree una instancia de [**una interfaz IXpsOMPackageWriter.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)

    Esto crea una clase FixedDocumentSequence vacía en el paquete.

    -   Para crear un documento XPS en un archivo, llame a [**IXpsOMObjectFactory::CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Para crear un documento XPS en una secuencia, llame a [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Inicie un nuevo documento en el paquete mediante una llamada [**a IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Antes de agregar una página, llame a [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) para agregar un elemento FixedDocument a la clase FixedDocumentSequence que se creó en el paso 1.

3.  Agregar contenido.
    -   Para agregar una nueva clase FixedPage al documento, llame a [**IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage)y pase un puntero a la interfaz [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que tenga el contenido de FixedPage que desea agregar.
    -   Para crear un nuevo elemento FixedDocument en FixedDocumentSequence, llame a [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Cierre el paquete y su contenido mediante una llamada [**a IXpsOMPackageWriter::Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Características avanzadas

Los métodos de [**la interfaz IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) también admiten la adición de recursos, miniaturas y vales de impresión. Estos componentes de documento se pueden agregar en los niveles package, FixedDocumentSequence, FixedDocument y FixedPage. Para obtener más información sobre el uso de esta interfaz para imprimir, vea [Imprimir un XPS OM](print-an-xps-om.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de firma digital XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Interfaces de página de XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Navegar por xps om](navigate-the-xps-om.md)
</dt> <dt>

[Trabajar con xps om canvas e interfaces visuales](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Trabajar con interfaces de ruta de acceso de OM xps](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Trabajar con interfaces de texto, gráficos e imágenes de XPS OM](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Interfaces de vales de impresión de XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Referencia de LA API del documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



