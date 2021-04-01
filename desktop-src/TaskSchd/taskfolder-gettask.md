---
title: Propiedad TaskFolder. GetTask
description: En el caso de scripting, obtiene una tarea en una ubicación especificada de una carpeta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Programador de tareas de la propiedad GetTask
- Programador de tareas de la propiedad GetTask, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad GetTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801598"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="016c3-106">Propiedad TaskFolder. GetTask</span><span class="sxs-lookup"><span data-stu-id="016c3-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="016c3-107">En el caso de scripting, obtiene una tarea en una ubicación especificada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="016c3-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="016c3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="016c3-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="016c3-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="016c3-109">Property value</span></span>

<span data-ttu-id="016c3-110">La ruta de acceso (ubicación) de la tarea en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="016c3-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="016c3-111">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) .</span><span class="sxs-lookup"><span data-stu-id="016c3-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="016c3-112">Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="016c3-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="016c3-113">No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. '</span><span class="sxs-lookup"><span data-stu-id="016c3-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="016c3-114">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="016c3-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="016c3-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="016c3-115">Error codes</span></span>

<span data-ttu-id="016c3-116">Tarea que se encuentra en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="016c3-116">The task at the specified location.</span></span> <span data-ttu-id="016c3-117">La tarea es un objeto [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="016c3-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="016c3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="016c3-118">Requirements</span></span>



| <span data-ttu-id="016c3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="016c3-119">Requirement</span></span> | <span data-ttu-id="016c3-120">Value</span><span class="sxs-lookup"><span data-stu-id="016c3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="016c3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="016c3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="016c3-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="016c3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="016c3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="016c3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="016c3-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="016c3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="016c3-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="016c3-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="016c3-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="016c3-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="016c3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="016c3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="016c3-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="016c3-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





