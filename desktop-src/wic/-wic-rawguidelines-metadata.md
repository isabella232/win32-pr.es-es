---
description: Compatibilidad con metadatos
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Compatibilidad con metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa706c3529a6c5efa0e453f7f3e181a6d6a82e0523d9ea3610dc992434856c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667342"
---
# <a name="metadata-support"></a>Compatibilidad con metadatos

Los formatos RAW también deben admitir los escenarios comunes de lectura y escritura de metadatos para las imágenes Windows. Microsoft ha desarrollado un conjunto de proveedores de metadatos nativos para archivos de imagen intercambiables (EXIF), International Press Telecommunications Council (IPTC) y metadatos de Extensible Metadata Platform (XMP) que actualmente solo se invocan para contenedores TIFF y JPEG. Si la imagen RAW se almacena en uno de estos formatos de contenedor, se recomienda usar el Windows de metadatos integrados. Sin embargo, el autor del códec es responsable de configurarlo correctamente. En el caso de los archivos RAW que no se basan en un contenedor TIFF, puede ser necesario implementar escritores EXIF, IPTC o XMP porque los lectores y escritores integrados esperan que los datos se ajusten a las especificaciones de diseño en disco exif, IPTC y XMP. Los autores de códecs también pueden implementar sus propios proveedores para cualquier metadato personalizado.

Debido a la arquitectura de Windows Imaging Component (WIC), los escritores de metadatos solo se pueden invocar a través de una instancia de un codificador de imágenes. Por lo tanto, los propietarios de formato RAW deben crear al menos un codificador [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) de "código auxiliar", incluso si no se implementa la codificación real de píxeles en un formato RAW. El autor del códec debe invocar los controladores de metadatos adecuados:

-   [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en el descodificador y el descodificador de marco según corresponda.
-   [**IWICMetadataBlockWriter en**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) el codificador y el codificador de fotogramas según corresponda.

Para admitir todos los escenarios previstos en aplicaciones de creación de imágenes en Windows Vista, se recomienda que los proveedores de códecs admitan lo siguiente como mínimo:

-   Exif read
-   Escritura exif parcial (para permitir que las actualizaciones capturen fecha y hora)
-   Lectura y escritura de XMP (incluido opcionalmente IPTC Core para XMP)
-   Lectura y escritura de IPTC IIMv4

La mayor parte del acceso a metadatos (tanto de lectura como de escritura) en Windows Vista se produce a través de la interfaz [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) o [**IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) Por lo tanto, para participar en las experiencias de metadatos de Windows Vista, los autores de códecs RAW deben implementar los métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Directrices de WIC para formatos de imagen raw de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



