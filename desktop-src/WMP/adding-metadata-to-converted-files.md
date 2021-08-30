---
title: Agregar metadatos a archivos convertidos
description: Agregar metadatos a archivos convertidos
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Reproductor de Windows Media,proceso de conversión
- Reproductor de Windows Media complementos,conversión
- complementos, conversión
- complementos de conversión, agregar metadatos a archivos convertidos
- agregar metadatos a archivos convertidos
- metadatos, agregar a archivos convertidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d040c9f083258d24398ce29c84dbe8b25a525d8c8d3bc617a0adddbb2ba8df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031565"
---
# <a name="adding-metadata-to-converted-files"></a>Agregar metadatos a archivos convertidos

Los archivos convertidos deben contener determinados metadatos para garantizar una buena experiencia del usuario. Como mínimo, los archivos convertidos deben contener los atributos principales enumerados en Windows instrucciones de uso de [metadatos multimedia](/previous-versions/ms867702(v=msdn.10)).

Para los archivos de música, establezca el valor de **WM/MediaClassPrimaryID** en D1607DBC-E323-4BE2-86A1-48A42A28441E.

Para los archivos de voz, establezca el valor de **WM/MediaClassPrimaryID** en 01CD0F29-DA4E-4157-897B-6275D50C4F11, que es el GUID de clase principal para los archivos de audio. Establezca el valor de **WM/MediaClassSecondaryID** en 193c8824-4d52-4178-90bd-305240b04636.

Para las notas de voz, establezca el valor de **WM/MediaClassPrimaryID** en 01CD0F29-DA4E-4157-897B-6275D50C4F11. Establezca el valor de **WM/MediaClassSecondaryID** en 3A172A13-2BD9-4831-835B-114F6A95943F.

Establezca el valor de **WM/ContentDistributor en** el nombre de clave del servicio de música que proporcionó el contenido.

Establezca el valor de **WM/UniqueFileIdentifier en** el identificador de contenido. Esto le permitirá recuperar elementos de contenido específicos en un momento futuro.

Establezca un valor para **WM/WMShadowFileSourceFileType**.

Para el contenido protegido, use el SDK Windows Media Format para establecer el atributo **\_ DRM DRMHeader \_ ContentID** en el identificador de contenido.

Para el contenido protegido, establezca un valor para **WM/WMShadowFileSourceDRMType**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los complementos de conversión**](about-conversion-plug-ins.md)
</dt> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 