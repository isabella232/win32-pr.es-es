---
description: La interfaz IXpsOMPackageWriter crea un archivo de documento XPS en el que las aplicaciones pueden escribir el contenido de las interfaces IXpsOMPage de un OM XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Uso de la interfaz IXpsOMPackageWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8a34a0538ff09cc050ac287d5314be93f0da8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707007"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Uso de la interfaz IXpsOMPackageWriter

La interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un archivo de documento XPS en el que las aplicaciones pueden escribir el contenido de las interfaces [**IXPSOMPAGE**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) de un OM XPS. La interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) es muy útil cuando el contenido del documento se está procesando o creando secuencialmente. A diferencia de los métodos [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) y [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) de la interfaz [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , para que se use la interfaz **IXpsOMPackageWriter** no se debe finalizar el FixedDocument completo ni la FixedDocumentSequence.

## <a name="overview"></a>Información general

La interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) escribe una página a la vez, desde la primera página de un documento XPS hasta el último. La interfaz se puede utilizar para crear archivos de documento XPS sencillos y también archivos de documento XPS complejos que contienen más de un FixedDocument en la FixedDocumentSequence. En los archivos de documento XPS complejos, los FixedDocuments también se crean secuencialmente, empezando por el primer FixedDocument de la FixedDocumentSequence. La interfaz **IXpsOMPackageWriter** no admite la creación de contenido de documento en orden aleatorio. Úselo, por ejemplo, para crear un informe secuencial o para realizar el procesamiento en un filtro de controlador de dispositivo en el que el contenido del documento se introduce en la secuencia.

## <a name="terminology-review"></a>Revisión de la terminología

Un *archivo de documento XPS* es un paquete de convenciones de empaquetado abierto (OPC) que se ajusta a la especificación de papel XML. Por lo tanto, técnicamente, la interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un *paquete OPC*, pero es un paquete OPC que se ajusta a la especificación de papel XML. Por esta razón, en las discusiones sobre los documentos XPS, los términos documento y *Paquete* de *XPS* suelen usarse indistintamente.

El *paquete* creado por la interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) contendrá los componentes de documento XPS necesarios: una FixedDocumentSequence, al menos un FixedDocument, y al menos un FixedPage. La FixedDocumentSequence se crea cuando se crea una instancia de la interfaz **IXpsOMPackageWriter** . Se crea un FixedDocument cada vez que se llama a [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) y se crea un FixedPage cada vez que se llama a [**IXpsOMPackageWriter:: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) . Dado que la interfaz escribe el contenido del documento secuencialmente, el método **addPage** agrega la página al FixedDocument creado más recientemente.

## <a name="using-the-ixpsompackagewriter-interface"></a>Uso de la interfaz IXpsOMPackageWriter

En el procedimiento siguiente se describe cómo crear un archivo de documento XPS mediante la interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) . En el procedimiento no se describe cómo crear una instancia de una interfaz [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) y su contenido. Para obtener más información sobre **IXpsOMPage** y la adición de contenido a una página, vea [interfaces de página de XPS OM](xps-object-model-page-interfaces.md) y los temas que se enumeran en la sección Vea también.

 **Crear un documento**

1.  Cree una instancia de una interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) .

    Esto crea una FixedDocumentSequence vacía en el paquete.

    -   Para crear un documento XPS en un archivo, llame a [**IXpsOMObjectFactory:: CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Para crear un documento XPS en una secuencia, llame a [**IXpsOMObjectFactory:: CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Inicie un nuevo documento en el paquete mediante una llamada a [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Antes de agregar una página, llame a [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) para agregar un FixedDocument a la FixedDocumentSequence que se creó en el paso 1.

3.  Agregar contenido.
    -   Para agregar un nuevo FixedPage al documento, llame a [**IXpsOMPackageWriter:: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), pasándole un puntero a la interfaz [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que tenga el contenido de la FixedPage que desea agregar.
    -   Para crear un nuevo FixedDocument en la FixedDocumentSequence, llame a [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Cierre el paquete y su contenido mediante una llamada a [**IXpsOMPackageWriter:: Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Características avanzadas

Los métodos de la interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) también admiten la adición de recursos, miniaturas e impresión de incidencias. Estos componentes de documento se pueden agregar en los niveles package, FixedDocumentSequence, FixedDocument y FixedPage. Para obtener más información acerca del uso de esta interfaz para imprimir, consulte [imprimir un OM de XPS](print-an-xps-om.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de firma digital XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Interfaces de página de XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Navegar por el OM de XPS](navigate-the-xps-om.md)
</dt> <dt>

[Trabajar con las interfaces visual y canvas de XPS OM](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Trabajar con las interfaces de ruta de acceso XPS OM](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Trabajar con interfaces de texto, gráficos e imágenes de XPS OM](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Interfaces de vales de impresión de XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Referencia de la API de documentos XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



