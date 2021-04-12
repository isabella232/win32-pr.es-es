---
description: Interfaces del codificador
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces del codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277624"
---
# <a name="encoder-interfaces"></a>Interfaces del codificador


En las tablas siguientes se muestran las interfaces implementadas por los codificadores de componentes de imágenes de Windows (WIC) y el diagrama de clases muestra la jerarquía de herencia.

Interfaces del codificador Container-Level



| Interfaz                                                                                       | Responsabilidades                             | Implementación                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Servicios de nivel de contenedor                     | Obligatorio                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Compatibilidad con la cancelación de notificación de progreso & | Recomendado                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Servicios de serialización de metadatos              | Opcional (solo es necesario para los formatos que admiten metadatos de nivel de contenedor) |



 

Interfaces del codificador Frame-Level



| Interfaz                                                       | Responsabilidades                | Implementación |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Servicios de nivel de marco            | Obligatorio       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Servicios de serialización de metadatos | Obligatorio       |



 

![jerarquía de herencia de la interfaz del codificador WIC](graphics/wicencoderinterfaces.png)

Observará que las interfaces del codificador son prácticamente imágenes reflejadas de las interfaces del descodificador y que la mayoría de los métodos de estas interfaces se corresponden con los métodos de las interfaces del descodificador relacionadas. Ahora que está familiarizado con la implementación de un descodificador habilitado para WIC, la implementación de un codificador habilitado para WIC también resultará familiar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Implementación de un codificador WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementación de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



