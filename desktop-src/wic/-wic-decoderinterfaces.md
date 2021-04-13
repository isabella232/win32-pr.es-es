---
description: Interfaces del descodificador
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces del descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278843"
---
# <a name="decoder-interfaces"></a>Interfaces del descodificador

En las tablas siguientes se muestran las interfaces implementadas por descodificadores de componentes de Windows Imaging (WIC) y el diagrama de clases muestra la jerarquía de herencia.

Container-Level interfaces del descodificador



| Interfaz                                                                                       | Responsabilidades                             | Implementación                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Servicios de nivel de contenedor                     | Obligatorio                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Compatibilidad con la cancelación de notificación de progreso & | Recomendado                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Enumeración de metadatos                         | Opcional (solo es necesario para los formatos que admiten metadatos de nivel de contenedor) |



 

Frame-Level interfaces del descodificador



| Interfaz                                                           | Responsabilidades          | Implementación                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Servicios de nivel de marco      | Obligatorio                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Enumeración de metadatos      | Obligatorio                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Transformaciones nativas del descodificador | Recomendado                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Servicios de procesamiento sin procesar   | Necesario solo para formatos RAW |



 

![jerarquía de herencia de la interfaz WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Implementar un descodificador de WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementar IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



