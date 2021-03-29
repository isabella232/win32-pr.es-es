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
# <a name="searching-for-a-subchunk"></a><span data-ttu-id="21ee8-112">Buscar un subfragmento</span><span class="sxs-lookup"><span data-stu-id="21ee8-112">Searching for a Subchunk</span></span>

<span data-ttu-id="21ee8-113">En el ejemplo siguiente se usa la función [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para buscar el fragmento "FMT" en el fragmento "Riff" del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="21ee8-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for the "FMT" chunk in the "RIFF" chunk of the previous example.</span></span>


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



<span data-ttu-id="21ee8-114">Para buscar un subfragmento (es decir, cualquier fragmento que no sea un fragmento "RIFF" o "LIST"), identifique su fragmento primario en el parámetro *lpckParent* de la función [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .</span><span class="sxs-lookup"><span data-stu-id="21ee8-114">To search for a subchunk (that is, any chunk other than a "RIFF" or "LIST" chunk), identify its parent chunk in the *lpckParent* parameter of the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function.</span></span>

<span data-ttu-id="21ee8-115">Si no especifica un fragmento primario, la posición del archivo actual debe estar al principio de un fragmento antes de llamar a la función **mmioDescend** .</span><span class="sxs-lookup"><span data-stu-id="21ee8-115">If you do not specify a parent chunk, the current file position should be at the beginning of a chunk before you call the **mmioDescend** function.</span></span> <span data-ttu-id="21ee8-116">Si especifica un fragmento primario, la posición del archivo actual puede estar en cualquier parte de ese fragmento.</span><span class="sxs-lookup"><span data-stu-id="21ee8-116">If you do specify a parent chunk, the current file position can be anywhere in that chunk.</span></span>

<span data-ttu-id="21ee8-117">Si se produce un error en la búsqueda de un subfragmento, la posición del archivo actual es indefinida.</span><span class="sxs-lookup"><span data-stu-id="21ee8-117">If the search for a subchunk fails, the current file position is undefined.</span></span> <span data-ttu-id="21ee8-118">Puede usar la función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) y el miembro **dwDataOffset** de la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) que describe el fragmento primario para buscar de nuevo al principio del fragmento primario, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="21ee8-118">You can use the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function and the **dwDataOffset** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure describing the parent chunk to seek back to the beginning of the parent chunk, as in the following example:</span></span>


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



<span data-ttu-id="21ee8-119">Dado que **dwDataOffset** especifica el desplazamiento al principio de la parte de datos del fragmento, debe buscar 4 bytes después de **dwDataOffset** para establecer la posición del archivo después del tipo de formulario.</span><span class="sxs-lookup"><span data-stu-id="21ee8-119">Because **dwDataOffset** specifies the offset to the beginning of the data portion of the chunk, you must seek 4 bytes past **dwDataOffset** to set the file position after the form type.</span></span>

 

 