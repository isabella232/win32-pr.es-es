---
description: El espacio de trabajo de un programa es una colección de las páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Espacio de trabajo del proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276817"
---
# <a name="process-working-set"></a><span data-ttu-id="f93be-103">Espacio de trabajo del proceso</span><span class="sxs-lookup"><span data-stu-id="f93be-103">Process Working Set</span></span>

<span data-ttu-id="f93be-104">El espacio de *trabajo* de un programa es una colección de las páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente.</span><span class="sxs-lookup"><span data-stu-id="f93be-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="f93be-105">Incluye datos compartidos y privados.</span><span class="sxs-lookup"><span data-stu-id="f93be-105">It includes both shared and private data.</span></span> <span data-ttu-id="f93be-106">Los datos compartidos incluyen páginas que contienen todas las instrucciones que ejecuta la aplicación, incluidas las de los archivos dll y los archivos DLL del sistema.</span><span class="sxs-lookup"><span data-stu-id="f93be-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="f93be-107">A medida que aumenta el tamaño del espacio de trabajo, aumenta la demanda de memoria.</span><span class="sxs-lookup"><span data-stu-id="f93be-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="f93be-108">Un proceso tiene un tamaño de espacio de trabajo mínimo asociado y un tamaño máximo del espacio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f93be-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="f93be-109">Cada vez que se llama a [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), reserva el tamaño mínimo del espacio de trabajo para el proceso.</span><span class="sxs-lookup"><span data-stu-id="f93be-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="f93be-110">El administrador de memoria virtual intenta mantener suficiente memoria para el espacio de trabajo mínimo residente cuando el proceso está activo, pero no mantiene más que el tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="f93be-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="f93be-111">Para obtener los tamaños mínimos y máximos solicitados del espacio de trabajo para la aplicación, llame a la función [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="f93be-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="f93be-112">El sistema establece los tamaños predeterminados del espacio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f93be-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="f93be-113">También puede modificar los tamaños del espacio de trabajo mediante la función [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="f93be-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="f93be-114">Establecer estos valores no es una garantía de que la memoria estará reservada o residente.</span><span class="sxs-lookup"><span data-stu-id="f93be-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="f93be-115">Tenga cuidado al solicitar un tamaño de espacio de trabajo mínimo o máximo, ya que esto puede reducir el rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="f93be-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="f93be-116">Para obtener el tamaño actual o máximo del espacio de trabajo para el proceso, utilice la función [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .</span><span class="sxs-lookup"><span data-stu-id="f93be-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f93be-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f93be-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f93be-118">[Información de rendimiento de memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f93be-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f93be-119">Espacio de trabajo</span><span class="sxs-lookup"><span data-stu-id="f93be-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
