---
description: Origen de archivo AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origen de archivo AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686409"
---
# <a name="aviwav-file-source"></a>Origen de archivo AVI/WAV

(En desuso. En el caso de los archivos AVI y WAV, use el [origen de archivo (Async)](file-source--async--filter.md) y el [divisor de AVI](avi-splitter-filter.md) o el [analizador de onda](wave-parser-filter.md)).

El filtro de origen de archivo AVI/WAV Lee los archivos de código fuente AVI y WAV y genera los pin de salida adecuados para el tipo de archivo.

En el caso de los archivos WAV, el filtro crea un PIN de salida de audio, que genera una secuencia de audio que se puede conectar a un filtro de representación de audio o a un filtro de transformación de audio intermedio.

En el caso de los archivos AVI, el filtro crea un PIN de salida de vídeo, que genera una secuencia AVI comprimida para el filtro de códec AVI y un PIN de salida de audio, que genera una secuencia de audio adecuada para un filtro de representación de audio o un filtro de transformación de audio intermedio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



