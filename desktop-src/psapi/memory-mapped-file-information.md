---
title: Memory-Mapped información de archivo
description: Un archivo asignado a la memoria (o asignación de archivos) es el resultado de asociar el contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso. Se puede usar para compartir un archivo o memoria entre dos o más procesos.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149534"
---
# <a name="memory-mapped-file-information"></a><span data-ttu-id="ba54f-104">Memory-Mapped información de archivo</span><span class="sxs-lookup"><span data-stu-id="ba54f-104">Memory-Mapped File Information</span></span>

<span data-ttu-id="ba54f-105">Un *archivo asignado a la memoria* (o *asignación de archivos*) es el resultado de asociar el contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso.</span><span class="sxs-lookup"><span data-stu-id="ba54f-105">A *memory-mapped file* (or *file mapping*) is the result of associating a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="ba54f-106">Se puede usar para compartir un archivo o memoria entre dos o más procesos.</span><span class="sxs-lookup"><span data-stu-id="ba54f-106">It can be used to share a file or memory between two or more processes.</span></span>

<span data-ttu-id="ba54f-107">La función [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) recibe un identificador de proceso y un puntero a una dirección como entrada.</span><span class="sxs-lookup"><span data-stu-id="ba54f-107">The [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) function receives a process handle and a pointer to an address as input.</span></span> <span data-ttu-id="ba54f-108">Si la dirección está dentro de un archivo asignado a la memoria en el espacio de direcciones virtuales del proceso, la función devuelve el nombre del archivo asignado a la memoria.</span><span class="sxs-lookup"><span data-stu-id="ba54f-108">If the address is within a memory-mapped file in the virtual address space of the process, the function returns the name of the memory-mapped file.</span></span> <span data-ttu-id="ba54f-109">Los nombres de archivo devueltos por **GetMappedFileName** usan el formato de dispositivo, en lugar de Letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="ba54f-109">The file names returned by **GetMappedFileName** use device form, rather than drive letters.</span></span> <span data-ttu-id="ba54f-110">Por ejemplo, el nombre de archivo c: \\ WinNT \\ system32 \\ CType. NLS sería similar al siguiente en forma de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="ba54f-110">For example, the file name c:\\winnt\\system32\\ctype.nls would look like this in device form:</span></span>

<span data-ttu-id="ba54f-111">\\Dispositivo \\ Harddisk0 \\ Partition1 \\ WinNT \\ system32 \\ CType. NLS</span><span class="sxs-lookup"><span data-stu-id="ba54f-111">\\Device\\Harddisk0\\Partition1\\WINNT\\System32\\ctype.nls</span></span>

<span data-ttu-id="ba54f-112">Para obtener más información sobre los archivos asignados a memoria, consulte [asignación de archivos](/windows/desktop/Memory/file-mapping).</span><span class="sxs-lookup"><span data-stu-id="ba54f-112">For more information about memory-mapped files, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="ba54f-113">Para obtener un ejemplo en el que se convierten los nombres de archivo en el formato de dispositivo a Letras de unidad, vea [obtener un nombre de archivo de un identificador de archivo](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span><span class="sxs-lookup"><span data-stu-id="ba54f-113">For an example that converts file names in device form to drive letters, see [Obtaining a File Name From a File Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span></span>

 

 