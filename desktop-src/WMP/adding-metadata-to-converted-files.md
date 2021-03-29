---
title: Agregar metadatos a archivos convertidos
description: Agregar metadatos a archivos convertidos
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, proceso de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, agregar metadatos a archivos convertidos
- agregar metadatos a archivos convertidos
- metadatos, agregar a archivos convertidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791950"
---
# <a name="adding-metadata-to-converted-files"></a>Agregar metadatos a archivos convertidos

Los archivos convertidos deben contener determinados metadatos para garantizar una buena experiencia del usuario. Como mínimo, los archivos convertidos deben contener los atributos principales que aparecen en las instrucciones de uso de los [metadatos de Windows Media](/previous-versions/ms867702(v=msdn.10)).

En el caso de los archivos de música, establezca el valor de **WM/MediaClassPrimaryID** en D1607DBC-E323-4BE2-86A1-48A42A28441E.

En el caso de los archivos de correo de voz, establezca el valor de **WM/MediaClassPrimaryID** en 01CD0F29-DA4E-4157-897B-6275D50C4F11, que es el GUID de clase principal para los archivos de audio. Establezca el valor de **WM/MediaClassSecondaryID** en 193c8824-4d52-4178-90bd-305240b04636.

En el caso de las notas de voz, establezca el valor de **WM/MediaClassPrimaryID** en 01CD0F29-DA4E-4157-897B-6275D50C4F11. Establezca el valor de **WM/MediaClassSecondaryID** en 3A172A13-2BD9-4831-835B-114F6A95943F.

Establezca el valor de **WM/ContentDistributor** en el nombre de clave del servicio de música que proporcionó el contenido.

Establezca el valor de **WM/UniqueFileIdentifier** en el ID. de contenido. Esto le permitirá recuperar elementos de contenido específicos en el futuro.

Establezca un valor para **WM/WMShadowFileSourceFileType**.

Para contenido protegido, use el SDK de Windows Media Format para establecer el atributo **\_ DRMHeader \_ contentid de DRM** en el ID. de contenido.

Para contenido protegido, establezca un valor para **WM/WMShadowFileSourceDRMType**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los complementos de conversión**](about-conversion-plug-ins.md)
</dt> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 