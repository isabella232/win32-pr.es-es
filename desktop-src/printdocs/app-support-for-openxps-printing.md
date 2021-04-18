---
description: OpenXPS es el formato de especificación de papel XML abierto para los documentos, y se basa en la especificación estándar de la Asociación Europea de los responsables de cartón (ECMA).
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: Compatibilidad de aplicaciones para la impresión en OpenXPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706297"
---
# <a name="app-support-for-openxps-printing"></a>Compatibilidad de aplicaciones para la impresión en OpenXPS

OpenXPS es el formato de especificación de papel XML abierto para los documentos y se basa en la especificación estándar de la Asociación Europea de fabricantes de informática (ECMA).

Windows 8 proporciona compatibilidad total con la impresión de OpenXPS a través del modelo de controlador de impresión V4, en paralelo con la compatibilidad continua con el formato XPS de Microsoft. Y este tema se centra en la parte de este soporte que es relevante para los desarrolladores de aplicaciones de Windows. Para obtener información sobre los requisitos de controladores para la compatibilidad con OpenXPS, consulte [compatibilidad de controladores con OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).

## <a name="sending-xps-data-to-the-print-system"></a>Envío de datos XPS al sistema de impresión

Se recomienda usar [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para enviar todos los trabajos de impresión XPS al sistema de impresión. **IPrintDocumentPackageTarget** acepta el modelo de objetos XPS (OM) sin serialización y ayuda a mejorar el rendimiento general.

A continuación se muestra un breve resumen de la interfaz **IPrintDocumentPackageTarget** :

-   Esta interfaz admite la impresión desde soluciones personalizadas, así como aplicaciones de escritorio.

-   En el caso de las aplicaciones de escritorio, se puede usar en lugar de [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).

-   Disponible en Windows 7 con Service Pack 1 (SP1) + actualización de la plataforma y Windows 8.

-   Incluya *DocumentTarget. h* en los proyectos para usar estas API.

Las aplicaciones que consumen documentos OpenXPS deben tener en cuenta que el tipo MIME para OpenXPS es el siguiente:

<dl> oxps de aplicación \\  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>Envío de datos de OpenXPS a la API de impresión XPS

Específico de OpenXPS, XPS OM acepta MSXPS y OpenXPS, y proporciona métodos para la conversión y serialización en cualquier formato. Esto permite a los desarrolladores de aplicaciones ser independientes del controlador de destino, si así lo desean. Esto también significa que los desarrolladores de aplicaciones siempre pueden enviar trabajos de impresión como OM de XPS a StartXpsPrintJob1 o IDocumentPackageTarget, sabiendo que el sistema de impresión administrará cualquier conversión necesaria.

Por supuesto, si se impide la conversión entre formatos XPS, se mejorará el rendimiento de un extremo a otro. Desde la aplicación, el desarrollador puede comprobar la siguiente clave del registro para determinar el formato XPS preferido del controlador de impresión de destino:

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

Una vez que se haya determinado el formato XPS preferido, la aplicación puede proporcionar objetos XPS OM que no requieran conversión. Una nota concreta es el uso de la foto HD en MSXPS y JPEGXR en OpenXPS. La conversión de JPEGXR en HD Photo es relativamente ligera, ya que la principal diferencia en esta conversión es que HD Photo omite 4 bits de control que requiere JPEGXR. Sin embargo, la conversión de la foto de HD a JPEGXR requiere que se vuelva a codificar la imagen completa para generar los bits de control necesarios. Por lo tanto, proporcionar imágenes de JPEGXR para imágenes de alta resolución garantizará la compatibilidad con OpenXPS y minimizará el costo de conversión de la imagen de MSXPS.

El encabezado *Xpsobjectmodel \_ 1. h* define las API y los objetos adicionales para OpenXPS. Y la interfaz IXpsOMObjectFactory1 proporciona métodos adicionales para la conversión de imágenes. Esta es la sintaxis:


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



Windows 8 proporciona las siguientes enumeraciones nuevas y actualizadas.

Nueva enumeración:

<dl>

[**\_tipo de documento XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

Enumeración actualizada

<dl>

[**\_tipo de imagen XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

Los nuevos métodos de Getdocumenttype (permiten que una aplicación determine el formato XPS de los documentos. Están disponibles en [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)y [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1). Esta es una lista de los métodos.

<dl>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1:: Getdocumenttype (**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1:: Getdocumenttype (**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

Windows 8 proporciona los siguientes códigos de error nuevos en compatibilidad con OpenXPS:

<dl> espacio de nombres de XPS \_ E no \_ coincidente \_ . <dl> Se devuelve este error si hay un espacio de nombres no coincidente.  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> Este error se devuelve si MSXPS usa URI absolutos en referencias internas o intenta usar referencias internas para serializar en la secuencia. Esto se debe a que el modelo de objetos de XPS genera identificadores URI relativos. Aunque MSXPS admite los URI relativos y absolutos, OpenXPS requiere URI relativos.  
</dl> </dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad de controladores para OpenXPS](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1:: Getdocumenttype (**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1:: Getdocumenttype (**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**\_tipo de documento XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**\_tipo de imagen XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
