---
description: En esta sección de temas se proporciona a los desarrolladores instrucciones sobre cómo implementar códecs de formato de archivo de imagen que funcionarán dentro del marco de trabajo de Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Cómo escribir un códec de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910169"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>Cómo escribir un códec de WIC-Enabled

En esta sección de temas se proporciona a los desarrolladores instrucciones sobre cómo implementar códecs de formato de archivo de imagen que funcionarán dentro del marco de trabajo de Windows Imaging Component (WIC).

<dl>

[Introducción](-wic-howtowriteacodec-intro.md)  
[Cómo funciona el componente de creación de imágenes de Windows (WIC)](-wic-howwicworks.md)  
<dl>

[Detección y arbitraje](-wic-howwicworks.md)  
[Descodificación](-wic-howwicworks.md)  
[Encoding](-wic-howwicworks.md)  
[La duración de un códec](-wic-howwicworks.md)  
[Cómo habilitar WIC](-wic-howwicworks.md)  
[Compatibilidad con apartamento multiproceso en WIC](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementar un descodificador de WIC-Enabled</a><dl>

[Interfaces del descodificador](-wic-decoderinterfaces.md)<dl>

[IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[IWICBitmapSource](-wic-imp-iwicbitmapsource.md)  
[IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)  
[IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementación de un codificador WIC-Enabled</a>  
<dl>

[Interfaces del codificador](-wic-encoderinterfaces.md)  
<dl>

[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Instalación y registro de códecs</a>  
<dl>

[Registro de un códec](-wic-codecinstallandreg.md)  
<dl>

[Entradas generales de registro](-wic-generalregentries.md)  
[Entradas del registro específicas del codificador](-wic-encoderregentries.md)  
<dl>

[Registrar un formato de contenedor con escritores de metadatos](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">Entradas del registro específicas del codificador</a>  
<dl>

[Registrar un nuevo formato de contenedor con lectores de metadatos](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">Integración con Fotogalería y explorador de Windows Vista</a>  
<dl>

[Almacén de propiedades de Windows](-wic-integrationregentries.md)  
[Galería fotográfica de Windows Vista](-wic-integrationregentries.md)  
[Caché en miniatura de Windows Vista](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Actualización de la caché en miniatura al instalar un códec</a> [que pone el códec de WIC-Enabled a disposición de los usuarios](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Introducción (cómo escribir un códec WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



