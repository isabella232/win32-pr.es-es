---
description: Filtro del descodificador de CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro del descodificador de CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997712"
---
# <a name="cc-decoder-filter"></a>Filtro del descodificador de CC

> [!IMPORTANT]
> Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

 

El descodificador de la secuencia de CC es un filtro de clase de flujo de modo kernel. Aparece en GraphEdit en la categoría "códecs de WDM streaming VBI". Acepta las forma de onda de ejemplo entregadas por un filtro de captura y entrega los datos de subtítulos cerrados descodificados en el [descodificador de la línea 21](line-21-decoder-filter.md) y/o en las aplicaciones interesadas.

Este filtro tiene dos clavijas de entrada, VBI y HWCC. El PIN VBI se usa para los datos de VBI sin procesar y el PIN HWCC se usa cuando el filtro de captura realiza la descodificación de VBI en el hardware. Cuando los datos se reciben en el PIN de HWCC, el descodificador de CC funciona en modo de "paso a través" y envía los datos directamente al descodificador de la línea 21 sin procesarlos de ningún modo. Si el filtro de captura expone un PIN de HWCC, debe estar conectado directamente al pin correspondiente en el descodificador de CC. La categoría PIN es **PINNAME \_ video \_ CC \_ Capture**.

El descodificador de CC tiene hasta ocho clavijas de salida, cada una de las cuales puede seleccionar sus propias líneas y subflujos. El primer PIN de salida se conecta al descodificador line-21.

El filtro descodificador de CC aparece en la categoría de filtro "códecs de WDM streaming VBI" (**AM \_ KSCATEGORY \_ VBICODEC**).

Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante **CoCreateInstance**. En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md). Para obtener más información, vea [crear filtros de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Ver subtítulos (CC)](viewing-closed-captions.md)
</dt> </dl>

 

 



