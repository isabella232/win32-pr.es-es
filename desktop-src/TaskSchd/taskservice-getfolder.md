---
title: Método TaskService.GetFolder
description: Para el scripting, obtiene una carpeta de tareas registradas.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Método GetFolder Programador de tareas
- Método GetFolder Programador de tareas , objeto TaskService
- Objeto TaskService Programador de tareas método , GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387104"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="13299-106">Método TaskService.GetFolder</span><span class="sxs-lookup"><span data-stu-id="13299-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="13299-107">Para el scripting, obtiene una carpeta de tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="13299-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="13299-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13299-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="13299-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13299-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13299-110">*ruta de acceso* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13299-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13299-111">Ruta de acceso a la carpeta que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="13299-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="13299-112">No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="13299-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="13299-113">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="13299-113">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="13299-114">Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="13299-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="13299-115">El carácter "." no se puede usar para especificar la carpeta de tareas actual y "..".</span><span class="sxs-lookup"><span data-stu-id="13299-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="13299-116">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="13299-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13299-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13299-117">Return value</span></span>

<span data-ttu-id="13299-118">Objeto [**TaskFolder**](taskfolder.md) para la carpeta solicitada.</span><span class="sxs-lookup"><span data-stu-id="13299-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="13299-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13299-119">Requirements</span></span>



| <span data-ttu-id="13299-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="13299-120">Requirement</span></span> | <span data-ttu-id="13299-121">Valor</span><span class="sxs-lookup"><span data-stu-id="13299-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13299-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13299-122">Minimum supported client</span></span><br/> | <span data-ttu-id="13299-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="13299-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="13299-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13299-124">Minimum supported server</span></span><br/> | <span data-ttu-id="13299-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="13299-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13299-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="13299-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="13299-127"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13299-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13299-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13299-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13299-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13299-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13299-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="13299-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13299-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="13299-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





