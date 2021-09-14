---
description: Esta sección de temas proporciona a los desarrolladores instrucciones sobre cómo implementar códecs de formato de archivo de imagen que funcionarán dentro del marco Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Cómo escribir un códec de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359612"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>Cómo escribir un códec de WIC-Enabled

Esta sección de temas proporciona a los desarrolladores instrucciones sobre cómo implementar códecs de formato de archivo de imagen que funcionarán dentro del marco Windows Imaging Component (WIC).

<dl>

[Introducción](-wic-howtowriteacodec-intro.md)  
[Funcionamiento del Windows de creación de imágenes (WIC)](-wic-howwicworks.md)  
<dl>

[Detección y arbitraje](-wic-howwicworks.md)  
[Descodificación](-wic-howwicworks.md)  
[Encoding](-wic-howwicworks.md)  
[Duración de un códec](-wic-howwicworks.md)  
[Habilitación de un códec en WIC](-wic-howwicworks.md)  
[Compatibilidad con el apartamento multiproceso en WIC](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementación de un descodificador WIC-Enabled de datos</a><dl>

[Interfaces de descodificador](-wic-decoderinterfaces.md)<dl>

[IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[IWICBitmapSource](-wic-imp-iwicbitmapsource.md)  
[IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)  
[IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementación de un WIC-Enabled Encoder</a>  
<dl>

[Interfaces de codificador](-wic-encoderinterfaces.md)  
<dl>

[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Instalación y registro de códecs</a>  
<dl>

[Registro de un códec](-wic-codecinstallandreg.md)  
<dl>

[Entradas de registro generales](-wic-generalregentries.md)  
[Entradas del Registro específicas del codificador](-wic-encoderregentries.md)  
<dl>

[Registro de un formato de contenedor con escritores de metadatos](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">Entradas del Registro específicas del codificador</a>  
<dl>

[Registrar un nuevo formato de contenedor con lectores de metadatos](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">Integración con Windows Vista PhotoGallery y Explorer</a>  
<dl>

[Windows Almacén de propiedades](-wic-integrationregentries.md)  
[Windows Vista Galería de fotos](-wic-integrationregentries.md)  
[Windows Caché de miniaturas de Vista](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Actualización de la caché de miniaturas al instalar un códec</a> que hace que el códec WIC-Enabled esté disponible para los [usuarios.](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Introducción (Cómo escribir un códec de WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



