---
title: Búsqueda de un subchunk
description: Búsqueda de un subchunk
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- E/S de archivos multimedia, buscar fragmento de RIFF
- E/S de archivo, buscar fragmento de RIFF
- entrada y salida (E/S), buscar fragmento de RIFF
- E/S (entrada y salida), buscar fragmento de RIFF
- buscar fragmento de RIFF
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- E/S de RIFF
- Fragmento de RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371828"
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



Para buscar un subchunk (es decir, cualquier fragmento que no sea un fragmento "RIFF" o "LIST"), identifique su fragmento primario en el parámetro *lpckParent* de la [**función mmioDescend.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)

Si no especifica un fragmento primario, la posición actual del archivo debe estar al principio de un fragmento antes de llamar a la **función mmioDescend.** Si especifica un fragmento primario, la posición actual del archivo puede estar en cualquier parte de ese fragmento.

Si se produce un error en la búsqueda de un subchunk, la posición del archivo actual no está definida. Puede usar la función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) y el miembro **dwDataOffset** de la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) que describe el fragmento primario para volver al principio del fragmento primario, como en el ejemplo siguiente:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Dado **que dwDataOffset** especifica el desplazamiento hasta el principio de la parte de datos del fragmento, debe buscar 4 bytes más allá de **dwDataOffset** para establecer la posición del archivo después del tipo de formulario.

 

 