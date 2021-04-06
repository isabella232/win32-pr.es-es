---
title: Crear un fragmento RIFF
description: Crear un fragmento RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- e/s de archivos multimedia, crear un fragmento RIFF
- e/s de archivos, crear un fragmento RIFF
- entrada y salida (e/s), crear un fragmento RIFF
- E/s (entrada y salida), crear un fragmento RIFF
- crear un fragmento RIFF
- mmioCreateChunk función)
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- RIFF E/S
- Fragmento RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904555"
---
# <a name="creating-a-riff-chunk"></a><span data-ttu-id="87058-113">Crear un fragmento RIFF</span><span class="sxs-lookup"><span data-stu-id="87058-113">Creating a RIFF Chunk</span></span>

<span data-ttu-id="87058-114">En el ejemplo siguiente se usa la función [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para crear un fragmento con un identificador de fragmento "Riff" y un tipo de formulario "RDIB".</span><span class="sxs-lookup"><span data-stu-id="87058-114">The following example uses the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to create a chunk with a chunk identifier of "RIFF" and a form type of "RDIB".</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



<span data-ttu-id="87058-115">Si va a crear un fragmento "RIFF" o "LIST", debe especificar el tipo de formulario o de lista en el miembro **fccType** de la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) .</span><span class="sxs-lookup"><span data-stu-id="87058-115">If you are creating a "RIFF" or "LIST" chunk, you must specify the form type or list type in the **fccType** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure.</span></span> <span data-ttu-id="87058-116">En el ejemplo anterior, "RDIB" es el tipo de formulario.</span><span class="sxs-lookup"><span data-stu-id="87058-116">In the previous example, "RDIB" is the form type.</span></span>

<span data-ttu-id="87058-117">Si conoce el tamaño del campo de datos en un nuevo fragmento, puede establecer el miembro **cksize** de la estructura **MMCKINFO** al crear el fragmento.</span><span class="sxs-lookup"><span data-stu-id="87058-117">If you know the size of the data field in a new chunk, you can set the **cksize** member of the **MMCKINFO** structure when you create the chunk.</span></span> <span data-ttu-id="87058-118">Este valor se escribirá en el campo tamaño de los datos del nuevo fragmento.</span><span class="sxs-lookup"><span data-stu-id="87058-118">This value will be written to the data size field in the new chunk.</span></span> <span data-ttu-id="87058-119">Si este valor no es correcto cuando se llama a [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) para marcar el final del fragmento, se reescribirá automáticamente para reflejar el tamaño correcto del campo de datos.</span><span class="sxs-lookup"><span data-stu-id="87058-119">If this value is not correct when you call [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) to mark the end of the chunk, it will be automatically rewritten to reflect the correct size of the data field.</span></span>

<span data-ttu-id="87058-120">Después de crear un fragmento mediante la función [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , la posición del archivo se establece en el campo de datos del fragmento (8 bytes desde el principio del fragmento).</span><span class="sxs-lookup"><span data-stu-id="87058-120">After you create a chunk by using the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="87058-121">Si el fragmento es un fragmento "RIFF" o "LIST", la posición del archivo se establece en la ubicación que sigue al tipo de formulario o tipo de lista (12 bytes desde el principio del fragmento).</span><span class="sxs-lookup"><span data-stu-id="87058-121">If the chunk is a "RIFF" or "LIST" chunk, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span>

 

 