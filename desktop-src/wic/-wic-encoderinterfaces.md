---
description: Interfaces de codificador
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces de codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570317"
---
# <a name="encoder-interfaces"></a>Interfaces de codificador


En las tablas siguientes se muestran las interfaces implementadas por los codificadores Windows Imaging Component (WIC) y el diagrama de clases muestra la jerarquía de herencia.

Container-Level interfaces de codificador



| Interfaz                                                                                       | Responsabilidades                             | Implementación                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Servicios de nivel de contenedor                     | Obligatorio                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Notificación de progreso & de cancelación | Recomendado                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Servicios de serialización de metadatos              | Opcional (solo se requiere para los formatos que admiten metadatos de nivel de contenedor) |



 

Frame-Level interfaces de codificador



| Interfaz                                                       | Responsabilidades                | Implementación |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Servicios de nivel de marco            | Obligatorio       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Servicios de serialización de metadatos | Obligatorio       |



 

![Jerarquía de herencia de la interfaz del codificador wic](graphics/wicencoderinterfaces.png)

Observará que las interfaces del codificador son imágenes casi reflejadas de las interfaces de descodificador y que la mayoría de los métodos de estas interfaces corresponden a métodos de las interfaces de descodificador relacionadas. Ahora que está familiarizado con la implementación de un descodificador habilitado para WIC, la implementación de un codificador habilitado para WIC también le parecerá familiar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementación de un WIC-Enabled Encoder](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementación de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



