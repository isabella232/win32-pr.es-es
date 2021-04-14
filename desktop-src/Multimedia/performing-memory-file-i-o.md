---
title: Realizar e/s de archivos de memoria
description: Realizar e/s de archivos de memoria
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- e/s de archivos multimedia, memoria
- e/s de archivos, memoria
- entrada y salida (e/s), memoria
- E/s (entrada y salida), memoria
- e/s de memoria
- mmioOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487538"
---
# <a name="performing-memory-file-io"></a><span data-ttu-id="3c3e7-109">Realizar e/s de archivos de memoria</span><span class="sxs-lookup"><span data-stu-id="3c3e7-109">Performing Memory File I/O</span></span>

<span data-ttu-id="3c3e7-110">Los servicios de e/s de archivos multimedia permiten tratar un bloque de memoria como un archivo.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-110">The multimedia file I/O services let you treat a block of memory as a file.</span></span> <span data-ttu-id="3c3e7-111">Esto puede ser útil si ya tiene una imagen de archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-111">This can be useful if you already have a file image in memory.</span></span> <span data-ttu-id="3c3e7-112">Los archivos de memoria permiten reducir el número de condiciones especiales en el código, ya que, con fines de e/s, puede tratar los archivos de memoria como si fueran archivos basados en disco.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-112">Memory files let you reduce the number of special-case conditions in your code because, for I/O purposes, you can treat memory files as if they were disk-based files.</span></span> <span data-ttu-id="3c3e7-113">También puede usar archivos de memoria con el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-113">You can also use memory files with the clipboard.</span></span>

<span data-ttu-id="3c3e7-114">Al igual que con los búferes de e/s, los archivos de memoria pueden usar la memoria asignada por la aplicación o por el administrador de e/s de archivos.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-114">As with I/O buffers, memory files can use memory allocated by the application or by the file I/O manager.</span></span> <span data-ttu-id="3c3e7-115">Además, los archivos de memoria pueden ser expansibles o no expansibles.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-115">In addition, memory files can be either expandable or nonexpandable.</span></span> <span data-ttu-id="3c3e7-116">Cuando el administrador de e/s de archivos alcanza el final de un archivo de memoria expansible, expande el archivo de memoria por un incremento predefinido.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-116">When the file I/O manager reaches the end of an expandable memory file, it expands the memory file by a predefined increment.</span></span>

<span data-ttu-id="3c3e7-117">Para abrir un archivo de memoria, use la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) con el parámetro *SzFilename* establecido en **null** y la \_ marca ReadWrite de MMIO establecida en el parámetro *dwOpenFlags* .</span><span class="sxs-lookup"><span data-stu-id="3c3e7-117">To open a memory file, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function with the *szFilename* parameter set to **NULL** and the MMIO\_READWRITE flag set in the *dwOpenFlags* parameter.</span></span> <span data-ttu-id="3c3e7-118">Establezca el parámetro *lpmmioinfo* para que apunte a una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) que se ha configurado de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3c3e7-118">Set the *lpmmioinfo* parameter to point to an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure that has been set up as follows:</span></span>

1.  <span data-ttu-id="3c3e7-119">Establezca el miembro **pIOProc** en **null**.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-119">Set the **pIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="3c3e7-120">Establezca el miembro **fccIOProc** en el valor de \_ MEM.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-120">Set the **fccIOProc** member to FOURCC\_MEM.</span></span>
3.  <span data-ttu-id="3c3e7-121">Establezca el miembro **pchBuffer** para que apunte al bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-121">Set the **pchBuffer** member to point to the memory block.</span></span> <span data-ttu-id="3c3e7-122">Para solicitar que el administrador de e/s de archivos asigne el bloque de memoria, establezca **pchBuffer** en **null**.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-122">To request that the file I/O manager allocate the memory block, set **pchBuffer** to **NULL**.</span></span>
4.  <span data-ttu-id="3c3e7-123">Establezca el miembro **cchBuffer** en el tamaño inicial del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-123">Set the **cchBuffer** member to the initial size of the memory block.</span></span>
5.  <span data-ttu-id="3c3e7-124">Establezca el miembro **adwInfo** en el tamaño mínimo de expansión del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-124">Set the **adwInfo** member to the minimum expansion size of the memory block.</span></span> <span data-ttu-id="3c3e7-125">Para un archivo de memoria no expansible, establezca **adwInfo** en **null**.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-125">For a nonexpandable memory file, set **adwInfo** to **NULL**.</span></span>
6.  <span data-ttu-id="3c3e7-126">Establezca el resto de miembros en cero.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-126">Set all other members to zero.</span></span>

<span data-ttu-id="3c3e7-127">No hay restricciones en la asignación de memoria para su uso como archivo de memoria no expansible.</span><span class="sxs-lookup"><span data-stu-id="3c3e7-127">There are no restrictions on allocating memory for use as a nonexpandable memory file.</span></span>

 

 