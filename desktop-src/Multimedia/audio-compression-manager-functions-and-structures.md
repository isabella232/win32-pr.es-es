---
title: Funciones y estructuras del Administrador de compresión de audio
description: Funciones y estructuras del Administrador de compresión de audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimedia, funciones de ACM
- audio, funciones de ACM
- administrador de compresión de audio (ACM), funciones
- ACM (administrador de compresión de audio), funciones
- audio multimedia, estructuras de ACM
- audio, estructuras de ACM
- administrador de compresión de audio (ACM), estructuras
- ACM (administrador de compresión de audio), estructuras
- Estructuras de ACM
- Funciones de ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371966"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funciones y estructuras del Administrador de compresión de audio

Las funciones de ACM se divide en varias categorías. Las convenciones de nomenclatura para las funciones hacen que sea fácil identificar estas categorías. Los nombres de función (con dos excepciones) tienen el formato *acmGroupFunction*, donde *Group* designa la categoría ACM (como "Driver", "Format", "FormatTag", "Filter", "FilterTag" o "Stream") y *Function* describe la acción realizada por la función.

Las funciones de los grupos de filtros y formato son muy similares. Casi todas las funciones que actúan en filtros tienen una función paralela que actúa en formatos.

En el grupo de formato, algunas funciones usan etiquetas de formato de audio de forma de onda (el **miembro wFormatTag** de una estructura [**DEFORMATEX),**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) mientras que otras requieren formatos de audio de forma de onda completos (la estructura **COMPLETA DE FORMA DE ONDAATEX).** (Para obtener información de referencia sobre la **estructura DE FORMA DEDATOX,** vea [Error](error.md)).

En el grupo de filtros, algunas funciones usan etiquetas de filtro de audio de forma de onda (el **miembro dwFilterTag** de una estructura [**WAVEFILTER),**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) mientras que otras requieren filtros de audio de forma de onda completos (la estructura **WAVEFILTER completa).**

Las funciones del grupo de secuencias representan los muchos pasos implicados en una conversión: abrir una instancia de conversión, preparar la conversión, realizar la conversión, limpiar una vez completada la conversión y cerrar la instancia de conversión.

 

 