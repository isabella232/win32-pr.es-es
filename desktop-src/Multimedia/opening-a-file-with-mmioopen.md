---
title: Abrir un archivo con mmioOpen
description: Abrir un archivo con mmioOpen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- e/s de archivos multimedia, abrir archivos
- e/s de archivos, abrir archivos
- entrada y salida (e/s), abrir archivos
- E/s (entrada y salida), abrir archivos
- e/s de archivos multimedia, función mmioOpen
- e/s de archivo, función mmioOpen
- entrada y salida (e/s), función mmioOpen
- E/s (entrada y salida), función mmioOpen
- mmioOpen función)
- abrir archivos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487698"
---
# <a name="opening-a-file-with-mmioopen"></a><span data-ttu-id="f952a-113">Abrir un archivo con mmioOpen</span><span class="sxs-lookup"><span data-stu-id="f952a-113">Opening a File with mmioOpen</span></span>

<span data-ttu-id="f952a-114">Para abrir un archivo para operaciones de e/s básicas, establezca el parámetro *lpmmioinfo* de la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) en **null**.</span><span class="sxs-lookup"><span data-stu-id="f952a-114">To open a file for basic I/O operations, set the *lpmmioinfo* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to **NULL**.</span></span> <span data-ttu-id="f952a-115">En el ejemplo siguiente se abre un archivo denominado "C: \\ samples \\SAMPLE1.TXT" para leerlo y se comprueba si hay un error en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f952a-115">The following example opens a file named "C:\\SAMPLES\\SAMPLE1.TXT" for reading, and checks the return value for error.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



<span data-ttu-id="f952a-116">Use el parámetro *dwFlags* de **mmioOpen** para especificar las marcas para abrir un archivo.</span><span class="sxs-lookup"><span data-stu-id="f952a-116">Use the *dwFlags* parameter of **mmioOpen** to specify flags for opening a file.</span></span>

 

 