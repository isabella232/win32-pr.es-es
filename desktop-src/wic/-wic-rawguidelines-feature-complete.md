---
description: 'Integridad de las características: interfaces recomendadas'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Integridad de las características: interfaces recomendadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c819f56b9343eab8326eb755d86280bde242a01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473831"
---
# <a name="feature-completeness-recommended-interfaces"></a>Integridad de las características: interfaces recomendadas

En la tabla siguiente se enumeran los códecs RAW Windows interfaces raw del componente de creación de imágenes (WIC).




| Interfaz | Requerido para | Descripción | 
|-----------|--------------|-------------|
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a> | Decodificadores | Representa el punto inicial para lacoding de un archivo de imagen. Proporciona acceso a propiedades de nivel de contenedor, como miniaturas, marcos y paleta.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a> | Decodificadores | Representa un marco de imagen específico dentro del contenedor que proporciona acceso a las propiedades de nivel de fotograma. Esta es la interfaz que descodifica los bits de imagen reales.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> | Decodificadores | Necesario para enumerar e iterar bloques de metadatos e invocar a los lectores de metadatos adecuados al leer desde un archivo de imagen. <br /><blockquote>[!Note]<br />Si el formato de contenedor RAW es compatible con TIFF o usa IFD o IRB estándar para almacenar metadatos EXIF o XMP, los autores de códecs pueden optar por invocar los lectores de metadatos integrados en lugar de escribir los suyos propios.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a> | Decodificadores | Permite al autor de la llamada especificar el formato de escalado, recorte, rotación o píxel deseado para la imagen descodificada, lo que puede mejorar significativamente el rendimiento del descodificador. Por ejemplo, los descodificadores JPEG y protocolo de datagramas inalámbricos (WDP) de Microsoft usan un esquema de optimización piramidal para lograr una descodificación más rápida cuando el mapa de bits de destino es menor que el mapa de bits de origen. Windows Vista (y versiones posteriores) intentará usar esta interfaz para extraer una vista previa "rápida" de una imagen RAW siempre que falte la vista previa incrustada o menos de 1024 píxeles en su dimensión más grande.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a> | Decodificadores | Necesario para los formatos RAW. Expone parámetros específicos del procesamiento de imágenes RAW. Los códecs RAW deben admitir tantos parámetros como se apliquen al códec.<br /> | 
| <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a> | Codificadores | Representa el punto inicial para codificar un archivo de imagen. Esta interfaz se usa para establecer propiedades de nivel de contenedor, como miniaturas, marcos y paleta. También es necesario invocar un escritor de metadatos para habilitar la persistencia de metadatos en el archivo de imagen. Por estos motivos, esta interfaz es necesaria incluso si no se admite la codificación del mapa de bits principal al formato RAW.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a> | Codificadores | Representa un marco de imagen específico dentro del contenedor. Esta interfaz se usa para codificar los bits de imagen reales y para establecer propiedades y metadatos por fotograma.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> | Codificadores | Necesario para iterar por bloques de metadatos e invocar los escritores de metadatos adecuados al serializar un archivo de imagen.<br /><blockquote>[!Note]<br />Si el formato de contenedor RAW es compatible con TIFF, los autores de códecs pueden optar por invocar los escritores de metadatos integrados en lugar de escribir los suyos propios.</blockquote><br /><br /> | 




 

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

 

 




