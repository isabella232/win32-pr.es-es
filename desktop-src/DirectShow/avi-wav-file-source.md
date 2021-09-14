---
description: Origen de archivo AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origen de archivo AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161708"
---
# <a name="aviwav-file-source"></a>Origen de archivo AVI/WAV

(En desuso. En el caso de los archivos AVI y WAV, use el origen [de archivo (Async)](file-source--async--filter.md) y el divisor [AVI](avi-splitter-filter.md) o el [analizador WAVE](wave-parser-filter.md)).

El filtro Origen de archivo AVI/WAV lee los archivos de origen AVI y WAV y genera los pines de salida adecuados para el tipo de archivo.

En el caso de los archivos WAV, el filtro crea un pin de salida de audio, que genera una secuencia de audio que se puede conectar a un filtro de representación de audio o a un filtro de transformación de audio que interviene.

En el caso de los archivos AVI, el filtro crea un pin de salida de vídeo, que genera una secuencia AVI comprimida adecuada para el filtro de códec AVI y un pin de salida de audio, que genera una secuencia de audio adecuada para un filtro de representación de audio o un filtro de transformación de audio que interviene.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



