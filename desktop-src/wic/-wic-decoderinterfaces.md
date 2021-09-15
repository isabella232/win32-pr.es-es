---
description: Interfaces de descodificador
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces de descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570321"
---
# <a name="decoder-interfaces"></a>Interfaces de descodificador

En las tablas siguientes se muestran las interfaces implementadas por los descodificadores Windows Imaging Component (WIC) y el diagrama de clases muestra la jerarquía de herencia.

Container-Level decoder interfaces



| Interfaz                                                                                       | Responsabilidades                             | Implementación                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Servicios de nivel de contenedor                     | Obligatorio                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Notificación de progreso & de cancelación | Recomendado                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Enumeración de metadatos                         | Opcional (solo se requiere para los formatos que admiten metadatos de nivel de contenedor) |



 

Frame-Level decoder interfaces



| Interfaz                                                           | Responsabilidades          | Implementación                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Servicios de nivel de marco      | Obligatorio                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Enumeración de metadatos      | Obligatorio                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Transformaciones de descodificador nativo | Recomendado                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Servicios de procesamiento sin procesar   | Obligatorio solo para formatos sin formato |



 

![jerarquía de herencia de interfaz wic](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementación de un descodificador de WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



