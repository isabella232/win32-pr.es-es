---
title: Funciones y estructuras del administrador de compresión de audio
description: Funciones y estructuras del administrador de compresión de audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimedia, funciones ACM
- audio, funciones ACM
- Administrador de compresión de audio (ACM), funciones
- ACM (Administrador de compresión de audio), funciones
- audio multimedia, estructuras ACM
- estructuras de audio y ACM
- Administrador de compresión de audio (ACM), estructuras
- ACM (Administrador de compresión de audio), estructuras
- Estructuras ACM
- Funciones ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651348"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funciones y estructuras del administrador de compresión de audio

Las funciones ACM se dividen en varias categorías. Las convenciones de nomenclatura para las funciones facilitan la identificación de estas categorías. Los nombres de función (con dos excepciones) tienen el formato *acmGroupFunction*, donde *Group* designa la categoría ACM (como "driver", "format", "FormatTag", "Filter", "FilterTag" o "Stream") y la *función* describe la acción que realiza la función.

Las funciones de los grupos filtro y formato son muy similares. Casi todas las funciones que actúan en filtros tienen una función paralela que actúa en formatos.

En el grupo formato, algunas funciones usan etiquetas de formato de audio de forma de onda (el miembro **wFormatTag** de una estructura [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ), mientras que otras requieren formatos de audio de forma de onda completos (la estructura de **WaveFormatEx** completa). (Para obtener información de referencia sobre la estructura **WAVEFORMATEX** , vea [error](error.md)).

En el grupo filtro, algunas funciones usan etiquetas de filtro de audio de onda (el miembro **dwFilterTag** de la estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), mientras que otras requieren filtros de audio de onda completa (la estructura **WAVEFILTER** completa).

Las funciones del grupo de secuencias representan los numerosos pasos implicados en una conversión: abrir una instancia de conversión, preparar la conversión, realizar la conversión, limpiar una vez finalizada la conversión y cerrar la instancia de conversión.

 

 