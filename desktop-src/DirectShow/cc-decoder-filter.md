---
description: Filtro descodificador CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro descodificador CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5feab764883754407030f2b4f72f794d049f5a394efb107ac149b10125da8d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757405"
---
# <a name="cc-decoder-filter"></a>Filtro descodificador CC

> [!IMPORTANT]
> Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

 

El descodificador VBI de CC es un filtro de clase de secuencia en modo kernel. Aparece en GraphEdit en la categoría "Códecs de VBI de streaming de WDM". Acepta formas de onda de ejemplo que entrega un filtro de captura y entrega datos de subtítulos descodificados al descodificador de línea [21](line-21-decoder-filter.md) o a las aplicaciones interesadas.

Este filtro tiene dos pines de entrada, VBI y HWCC. El pin de VBI se usa para los datos de VBI sin procesar y el pin HWCC se usa cuando el filtro de captura realiza la decodización de VBI en hardware. Cuando los datos se reciben en el pin HWCC, el descodificador CC funciona en modo de "paso a través" y envía los datos directamente al descodificador de línea 21 sin procesarlo de ninguna manera. Si el filtro de captura expone un pin HWCC, debe estar conectado directamente al pin correspondiente en el descodificador CC. La categoría de pin es **PINNAME \_ VIDEO CC \_ \_ CAPTURE**.

El descodificador CC tiene hasta ocho patillas de salida, cada una de las cuales puede seleccionar sus propias líneas y subdiecciones. El primer pin de salida está conectado al descodificador Line-21.

El filtro descodificador CC aparece en la categoría de filtro "Códecs VBI de streaming de WDM" (**AM \_ KSCATEGORY \_ VBICODEC**).

Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante **CoCreateInstance**. En su lugar, use [el enumerador de dispositivos del sistema](system-device-enumerator.md). Para obtener más información, vea [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Visualización de subtítulos](viewing-closed-captions.md)
</dt> </dl>

 

 



