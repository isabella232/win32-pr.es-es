---
description: Filtro de códec de elemento WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro de códec de elemento WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361558"
---
# <a name="wst-codec-filter"></a>Filtro de códec de elemento WST

> [!IMPORTANT]
> Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

 

A partir de Windows Vista, este filtro se sustituye por el filtro VBICodec, que se documenta en la documentación de las tecnologías de Microsoft TV.

El teletexto estándar mundial (elemento WST) es el estándar europeo para la transmisión de datos mediante VBI en señales de televisión analógica PAL. Los servicios de subtítulos y de datos se proporcionan mediante este estándar. El códec elemento WST es un filtro de modo kernel que recibe muestras de VBI sin procesar y, opcionalmente, muestras de teletexto descodificadas del filtro de captura a través del filtro de [convertidor Tee/Sink-to-Sink](tee-sink-to-sink-converter.md) . Este códec descodifica y/o duplica los datos de teletexto descodificados y con corrección de errores de reenvío para el filtro de [descodificador de elemento WST](wst-decoder-filter.md) . El códec elemento WST se corresponde con el filtro del descodificador de CC para las transmisiones NTSC. El descodificador de elemento WST corresponde al [descodificador de línea 21](line-21-decoder-filter.md) para NTSC; Estos filtros crean los mapas de bits que se envían al mezclador de superposición o al representador de mezcla de vídeo.

Este filtro tiene dos clavijas de entrada, VBI y HWCC. El PIN VBI se usa para los datos de VBI sin procesar y el PIN HWCC se usa cuando el filtro de captura realiza la descodificación de VBI en el hardware. Cuando los datos se reciben en el PIN HWCC, el códec elemento WST funciona en modo de "paso a través" y envía los datos directamente al descodificador elemento WST sin procesarlos de ningún modo. Si el filtro de captura expone un PIN HWCC, debe estar conectado directamente al pin correspondiente en el códec elemento WST.

El filtro de códecs de elemento WST aparece en la categoría de filtro "códecs de WDM streaming VBI" (**AM \_ KSCATEGORY \_ VBICODEC**).

Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante **CoCreateInstance**. En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md). Para obtener más información, vea [crear filtros de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Ver teletexto estándar del mundo](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



