---
description: El espacio de trabajo de un programa es una colección de esas páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Conjunto de trabajo de proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549907"
---
# <a name="process-working-set"></a><span data-ttu-id="2d615-103">Conjunto de trabajo de proceso</span><span class="sxs-lookup"><span data-stu-id="2d615-103">Process Working Set</span></span>

<span data-ttu-id="2d615-104">El *espacio de trabajo* de un programa es una colección de esas páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente.</span><span class="sxs-lookup"><span data-stu-id="2d615-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="2d615-105">Incluye datos compartidos y privados.</span><span class="sxs-lookup"><span data-stu-id="2d615-105">It includes both shared and private data.</span></span> <span data-ttu-id="2d615-106">Los datos compartidos incluyen páginas que contienen todas las instrucciones que ejecuta la aplicación, incluidas las de los archivos DLL y los archivos DLL del sistema.</span><span class="sxs-lookup"><span data-stu-id="2d615-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="2d615-107">A medida que aumenta el tamaño del espacio de trabajo, aumenta la demanda de memoria.</span><span class="sxs-lookup"><span data-stu-id="2d615-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="2d615-108">Un proceso tiene un tamaño de espacio de trabajo mínimo asociado y un tamaño máximo del espacio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2d615-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="2d615-109">Cada vez que se [**llama a CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)se reserva el tamaño mínimo del espacio de trabajo para el proceso.</span><span class="sxs-lookup"><span data-stu-id="2d615-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="2d615-110">El administrador de memoria virtual intenta mantener suficiente memoria para el espacio de trabajo mínimo que residen cuando el proceso está activo, pero no conserva más del tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="2d615-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="2d615-111">Para obtener los tamaños mínimo y máximo solicitados del espacio de trabajo para la aplicación, llame a la [**función GetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)</span><span class="sxs-lookup"><span data-stu-id="2d615-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="2d615-112">El sistema establece los tamaños de los conjuntos de trabajo predeterminados.</span><span class="sxs-lookup"><span data-stu-id="2d615-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="2d615-113">También puede modificar los tamaños de los conjuntos de trabajo mediante la [**función SetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)</span><span class="sxs-lookup"><span data-stu-id="2d615-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="2d615-114">Establecer estos valores no es una garantía de que la memoria se reservará o será residentes.</span><span class="sxs-lookup"><span data-stu-id="2d615-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="2d615-115">Tenga cuidado al solicitar un tamaño de espacio de trabajo mínimo o máximo demasiado grande, ya que hacerlo puede degradar el rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="2d615-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="2d615-116">Para obtener el tamaño actual o máximo del conjunto de trabajo para el proceso, use la [**función GetProcessMemoryInfo.**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo)</span><span class="sxs-lookup"><span data-stu-id="2d615-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d615-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d615-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2d615-118">[Información de rendimiento de memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d615-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2d615-119">Espacio de trabajo</span><span class="sxs-lookup"><span data-stu-id="2d615-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
