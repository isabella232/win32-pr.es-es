---
description: Interfaces de codificador
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces de codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6169dcf55ffafe0bf4c006b45c173ecc7486555fb001456112f8f333a8ccf2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965133"
---
# <a name="encoder-interfaces"></a>Interfaces de codificador


En las tablas siguientes se muestran las interfaces implementadas por los codificadores Windows Imaging Component (WIC) y el diagrama de clases muestra la jerarquía de herencia.

Container-Level encoder interfaces



| Interfaz                                                                                       | Responsabilidades                             | Implementación                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Servicios de nivel de contenedor                     | Requerido                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Notificación de progreso & de cancelación | Recomendado                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Servicios de serialización de metadatos              | Opcional (solo se requiere para los formatos que admiten metadatos de nivel de contenedor) |



 

Frame-Level encoder interfaces



| Interfaz                                                       | Responsabilidades                | Implementación |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Servicios de nivel de marco            | Requerido       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Servicios de serialización de metadatos | Requerido       |



 

![Jerarquía de herencia de la interfaz del codificador wic](graphics/wicencoderinterfaces.png)

Observará que las interfaces del codificador son imágenes casi reflejadas de las interfaces de descodificador y que la mayoría de los métodos de estas interfaces se corresponden con los métodos de las interfaces de descodificador relacionadas. Ahora que está familiarizado con la implementación de un descodificador habilitado para WIC, la implementación de un codificador habilitado para WIC también le parecerá familiar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementación de un WIC-Enabled encoder](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementación de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



