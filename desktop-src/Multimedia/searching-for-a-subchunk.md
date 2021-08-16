---
title: Búsqueda de un subchunk
description: Búsqueda de un subchunk
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- E/S de archivos multimedia, buscar fragmentos de RIFF
- E/S de archivo, buscar fragmento de RIFF
- entrada y salida (E/S), búsqueda de fragmento de RIFF
- E/S (entrada y salida), buscar fragmento de RIFF
- buscar fragmento de RIFF
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- E/S de RIFF
- Fragmento de RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f77cc4d3b9640e0d262a113d3c8f352bb30fce625737b1bf13dde24adbe578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371143"
---
# <a name="searching-for-a-subchunk"></a>Búsqueda de un subchunk

En el ejemplo siguiente se usa la función [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para buscar el fragmento "FMT" en el fragmento "RIFF" del ejemplo anterior.


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



Para buscar un subcunk (es decir, cualquier fragmento que no sea un fragmento "RIFF" o "LIST"), identifique su fragmento primario en el parámetro *lpckParent* de la [**función mmioDescend.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)

Si no especifica un fragmento primario, la posición actual del archivo debe estar al principio de un fragmento antes de llamar a la **función mmioDescend.** Si especifica un fragmento primario, la posición actual del archivo puede estar en cualquier parte de ese fragmento.

Si se produce un error en la búsqueda de un subcunk, la posición del archivo actual no está definida. Puede usar la función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) y el miembro **dwDataOffset** de la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) que describe el fragmento primario para volver al principio del fragmento primario, como en el ejemplo siguiente:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Dado **que dwDataOffset** especifica el desplazamiento al principio de la parte de datos del fragmento, debe buscar 4 bytes más allá de **dwDataOffset** para establecer la posición del archivo después del tipo de formulario.

 

 