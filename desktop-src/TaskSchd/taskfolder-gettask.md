---
title: Propiedad TaskFolder.GetTask
description: Para el scripting, obtiene una tarea en una ubicación especificada de una carpeta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Propiedad GetTask Programador de tareas
- Propiedad GetTask Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas , propiedad GetTask
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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387681"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="9fdb9-106">Propiedad TaskFolder.GetTask</span><span class="sxs-lookup"><span data-stu-id="9fdb9-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="9fdb9-107">Para el scripting, obtiene una tarea en una ubicación especificada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fdb9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fdb9-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="9fdb9-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9fdb9-109">Property value</span></span>

<span data-ttu-id="9fdb9-110">Ruta de acceso (ubicación) a la tarea en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="9fdb9-111">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="9fdb9-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="9fdb9-112">Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="9fdb9-113">El carácter "." no se puede usar para especificar la carpeta de tareas actual y "..".</span><span class="sxs-lookup"><span data-stu-id="9fdb9-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="9fdb9-114">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9fdb9-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9fdb9-115">Error codes</span></span>

<span data-ttu-id="9fdb9-116">Tarea en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-116">The task at the specified location.</span></span> <span data-ttu-id="9fdb9-117">La tarea es un [**objeto RegisteredTask.**](registeredtask.md)</span><span class="sxs-lookup"><span data-stu-id="9fdb9-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fdb9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fdb9-118">Requirements</span></span>



| <span data-ttu-id="9fdb9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fdb9-119">Requirement</span></span> | <span data-ttu-id="9fdb9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9fdb9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdb9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fdb9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9fdb9-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9fdb9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9fdb9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fdb9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9fdb9-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fdb9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9fdb9-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9fdb9-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fdb9-126"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9fdb9-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9fdb9-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fdb9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fdb9-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fdb9-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





