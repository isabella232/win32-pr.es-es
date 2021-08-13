---
description: Interfaces de descodificador
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces de descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a52a0924f6302e45b10cb32a1d621db04967d33a3251ee39cce359e5030af5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393534"
---
# <a name="decoder-interfaces"></a>Interfaces de descodificador

En las tablas siguientes se muestran las interfaces implementadas por los descodificadores de Windows Imaging Component (WIC) y el diagrama de clases muestra la jerarquía de herencia.

Container-Level de descodificador



| Interfaz                                                                                       | Responsabilidades                             | Implementación                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Servicios de nivel de contenedor                     | Obligatorio                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Notificación de progreso & de cancelación | Recomendado                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Enumeración de metadatos                         | Opcional (solo se requiere para los formatos que admiten metadatos de nivel de contenedor) |



 

Frame-Level de descodificador



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

[Implementación de un descodificador WIC-Enabled de datos](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



