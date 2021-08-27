---
description: Filtro de códec WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro de códec WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e729e13500317711076f6cdbd39c9a6ab25bea77e8d378e12f917f2e20e4a561
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083455"
---
# <a name="wst-codec-filter"></a>Filtro de códec WST

> [!IMPORTANT]
> Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

 

A partir Windows Vista, este filtro se reemplaza por el filtro VBICodec, que se documenta en la documentación de Microsoft TV Technologies.

World Standard Teletext (WST) es el estándar europeo para la transmisión de datos mediante VBI en señales de televisión análogas PAL. Tanto los subtítulos como los servicios de datos se proporcionan con este estándar. El códec WST es un filtro en modo kernel que recibe muestras de VBI sin procesar y, opcionalmente, muestras de teletexto descodificadas del filtro de captura a través del filtro [Tee/Sink-to-Sink Converter.](tee-sink-to-sink-converter.md) Este códec descodifica o duplica los datos de teletexto descodificados y corregidos por error hacia delante para el filtro [descodificador WST.](wst-decoder-filter.md) El códec WST se corresponde con el filtro descodificador CC para las transmisiones FILTR. El descodificador WST corresponde al descodificador [de línea 21](line-21-decoder-filter.md) para WLAN; Estos filtros crean los mapas de bits que se envían a la Mixer o al representador de mezcla de vídeo.

Este filtro tiene dos pines de entrada, VBI y HWCC. El pin de VBI se usa para los datos de VBI sin procesar y el pin HWCC se usa cuando el filtro de captura realiza la descodización de VBI en hardware. Cuando los datos se reciben en el pin HWCC, el códec WST funciona en modo de "paso a través" y envía los datos directamente al descodificador de WST sin procesarlo de ninguna manera. Si el filtro de captura expone un pin HWCC, debe estar conectado directamente al pin correspondiente en el códec WST.

El filtro códec WST aparece en la categoría de filtro "Códecs de VBI de streaming de WDM" (**AM \_ KSCATEGORY \_ VBICODEC**).

Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante **CoCreateInstance**. En su lugar, use [el enumerador de dispositivos del sistema](system-device-enumerator.md). Para obtener más información, vea [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Visualización del texto teletexto estándar del mundo](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



