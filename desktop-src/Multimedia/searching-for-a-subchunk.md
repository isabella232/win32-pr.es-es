---
title: Buscar un subfragmento
description: Buscar un subfragmento
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- e/s de archivos multimedia, buscar un fragmento RIFF
- e/s de archivos, buscar un fragmento RIFF
- entrada y salida (e/s), buscar fragmentos RIFF
- E/s (entrada y salida), buscar fragmentos RIFF
- buscando fragmento RIFF
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- RIFF E/S
- Fragmento RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358966"
---
# <a name="searching-for-a-subchunk"></a>Buscar un subfragmento

En el ejemplo siguiente se usa la función [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para buscar el fragmento "FMT" en el fragmento "Riff" del ejemplo anterior.


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



Para buscar un subfragmento (es decir, cualquier fragmento que no sea un fragmento "RIFF" o "LIST"), identifique su fragmento primario en el parámetro *lpckParent* de la función [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .

Si no especifica un fragmento primario, la posición del archivo actual debe estar al principio de un fragmento antes de llamar a la función **mmioDescend** . Si especifica un fragmento primario, la posición del archivo actual puede estar en cualquier parte de ese fragmento.

Si se produce un error en la búsqueda de un subfragmento, la posición del archivo actual es indefinida. Puede usar la función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) y el miembro **dwDataOffset** de la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) que describe el fragmento primario para buscar de nuevo al principio del fragmento primario, como en el ejemplo siguiente:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Dado que **dwDataOffset** especifica el desplazamiento al principio de la parte de datos del fragmento, debe buscar 4 bytes después de **dwDataOffset** para establecer la posición del archivo después del tipo de formulario.

 

 