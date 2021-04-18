---
description: Compatibilidad con metadatos
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Compatibilidad con metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706831"
---
# <a name="metadata-support"></a>Compatibilidad con metadatos

Los formatos sin formato también deben admitir los escenarios comunes de lectura y escritura de metadatos para las imágenes de Windows. Microsoft ha desarrollado un conjunto de proveedores de metadatos nativos para el archivo de imagen intercambiable (EXIF), el Consejo Internacional de telecomunicaciones (IPTC) y los metadatos de la plataforma de metadatos extensible (XMP) que actualmente se invocan solo para contenedores TIFF y JPEG. Si la imagen sin procesar se almacena en uno de estos formatos de contenedor, se recomienda usar los proveedores de metadatos integrados de Windows. Sin embargo, el autor del códec es responsable de configurarlo correctamente. En el caso de los archivos sin formato que no se basan en un contenedor TIFF, podría ser necesario implementar escritores EXIF, IPTC o XMP porque los lectores y escritores integrados esperan que los datos se ajusten a las especificaciones de diseño en disco de EXIF, IPTC y XMP. Los creadores de códecs también pueden implementar sus propios proveedores para los metadatos personalizados.

Debido a la arquitectura de Windows Imaging Component (WIC), los escritores de metadatos solo se pueden invocar a través de una instancia de un codificador de imágenes. Por lo tanto, los propietarios de formato sin formato deben crear al menos un codificador de "stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , incluso si no se implementa la codificación real de píxeles en formato sin procesar. El autor del códec debe invocar los controladores de metadatos adecuados:

-   [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) tanto en el descodificador como en el descodificador de fotogramas según corresponda.
-   [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) en el codificador y el codificador de tramas según corresponda.

Para admitir todos los escenarios previstos en aplicaciones de creación de imágenes en Windows Vista, se recomienda que los proveedores de códecs admitan lo siguiente como mínimo:

-   Lectura EXIF
-   Escritura EXIF parcial (para permitir que las actualizaciones capturen la fecha y la hora)
-   XMP Read y Write (incluido opcionalmente IPTC Core para XMP)
-   IIMv4 de lectura y escritura de IPTC

La mayor parte del acceso a los metadatos (lectura y escritura) en Windows Vista se produce a través de la interfaz [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) o [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Por lo tanto, para participar en las experiencias de metadatos de Windows Vista, los autores de códecs sin formato deben implementar los métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Instrucciones de WIC para formatos de imagen RAW de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



