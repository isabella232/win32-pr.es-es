---
title: Servicios básicos
description: Servicios básicos
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- e/s de archivos multimedia, servicios básicos
- e/s de archivos, servicios básicos
- entrada y salida (e/s), servicios básicos
- E/s (entrada y salida), servicios básicos
- e/s básicas
- mmioOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420675"
---
# <a name="basic-services"></a><span data-ttu-id="51d9c-109">Servicios básicos</span><span class="sxs-lookup"><span data-stu-id="51d9c-109">Basic Services</span></span>

<span data-ttu-id="51d9c-110">El uso de los servicios de e/s básicos es similar al uso de los servicios de e/s de archivos en tiempo de ejecución de la biblioteca en tiempo de ejecución de C.</span><span class="sxs-lookup"><span data-stu-id="51d9c-110">Using the basic I/O services is similar to using the run-time file I/O services of the C run-time library.</span></span> <span data-ttu-id="51d9c-111">Los archivos se deben abrir antes de que se puedan leer o escribir.</span><span class="sxs-lookup"><span data-stu-id="51d9c-111">Files must be opened before they can be read or written.</span></span> <span data-ttu-id="51d9c-112">Después de leer o escribir, el archivo debe estar cerrado.</span><span class="sxs-lookup"><span data-stu-id="51d9c-112">After reading or writing, the file must be closed.</span></span> <span data-ttu-id="51d9c-113">También puede cambiar la ubicación de lectura o escritura actual dentro de un archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="51d9c-113">You can also change the current read or write location within an open file.</span></span>

<span data-ttu-id="51d9c-114">Antes de comenzar las operaciones de e/s en un archivo, debe abrir el archivo mediante la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="51d9c-114">Before you begin any I/O operations to a file, you must open the file by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="51d9c-115">Esta función devuelve un identificador de archivo de tipo **HMMIO**.</span><span class="sxs-lookup"><span data-stu-id="51d9c-115">This function returns a file handle of type **HMMIO**.</span></span> <span data-ttu-id="51d9c-116">Puede usar este identificador de archivo para identificar el archivo abierto al llamar a otras funciones de e/s de archivo.</span><span class="sxs-lookup"><span data-stu-id="51d9c-116">You can use this file handle to identify the open file when calling other file I/O functions.</span></span>

> [!Note]  
> <span data-ttu-id="51d9c-117">Un identificador de archivo **HMMIO** no es un identificador de archivo estándar.</span><span class="sxs-lookup"><span data-stu-id="51d9c-117">An **HMMIO** file handle is not a standard file handle.</span></span> <span data-ttu-id="51d9c-118">No use identificadores de archivo **HMMIO** con funciones de e/s de archivos en tiempo de ejecución de Win32 o C.</span><span class="sxs-lookup"><span data-stu-id="51d9c-118">Do not use **HMMIO** file handles with Win32 or C run-time file I/O functions.</span></span>

 

<span data-ttu-id="51d9c-119">Cuando se usa [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) para abrir un archivo, se usa una marca para especificar si se va a abrir para lectura, escritura o ambos.</span><span class="sxs-lookup"><span data-stu-id="51d9c-119">When you use [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) to open a file, you use a flag to specify whether you are opening it for reading, writing, or both.</span></span> <span data-ttu-id="51d9c-120">También puede especificar marcas que le permitan crear o eliminar un archivo.</span><span class="sxs-lookup"><span data-stu-id="51d9c-120">You can also specify flags that enable you to create or delete a file.</span></span> <span data-ttu-id="51d9c-121">Use la función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) para cerrar un archivo cuando haya terminado de leer o escribir en él.</span><span class="sxs-lookup"><span data-stu-id="51d9c-121">Use the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to close a file when you are finished reading or writing to it.</span></span>

<span data-ttu-id="51d9c-122">Puede leer y escribir archivos mediante las funciones [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) y [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="51d9c-122">You can read and write files by using the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) and [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) functions respectively.</span></span> <span data-ttu-id="51d9c-123">La siguiente operación de lectura o escritura se produce en la posición del archivo actual o en el puntero de archivo de un archivo.</span><span class="sxs-lookup"><span data-stu-id="51d9c-123">The next read or write operation occurs at the current file position or file pointer in a file.</span></span> <span data-ttu-id="51d9c-124">La posición del archivo actual es avanzada cada vez que se lee o se escribe un archivo.</span><span class="sxs-lookup"><span data-stu-id="51d9c-124">The current file position is advanced each time a file is read or written.</span></span>

<span data-ttu-id="51d9c-125">También puede cambiar la posición actual del archivo mediante la función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="51d9c-125">You can also change the current file position by using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span> <span data-ttu-id="51d9c-126">Debe asegurarse de especificar una ubicación válida en un archivo.</span><span class="sxs-lookup"><span data-stu-id="51d9c-126">You should ensure that you specify a valid location in a file.</span></span> <span data-ttu-id="51d9c-127">Si especifica una ubicación no válida, como más allá del final del archivo, es posible que **mmioSeek** no devuelva un error, pero se podrían producir errores en las operaciones de e/s posteriores.</span><span class="sxs-lookup"><span data-stu-id="51d9c-127">If you specify an invalid location, such as past the end of the file, **mmioSeek** may not return an error, but subsequent I/O operations could fail.</span></span>

<span data-ttu-id="51d9c-128">Hay marcas que puede usar con la función **mmioOpen** para operaciones más allá de la e/s de archivos básica.</span><span class="sxs-lookup"><span data-stu-id="51d9c-128">There are flags you can use with the **mmioOpen** function for operations beyond basic file I/O.</span></span> <span data-ttu-id="51d9c-129">Al especificar una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , por ejemplo, puede abrir archivos de memoria, especificar un procedimiento de e/s personalizado o proporcionar un búfer para la e/s almacenada en búfer.</span><span class="sxs-lookup"><span data-stu-id="51d9c-129">By specifying an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure, for example, you can open memory files, specify a custom I/O procedure, or supply a buffer for buffered I/O.</span></span>

 

 