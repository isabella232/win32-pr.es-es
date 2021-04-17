---
title: TaskService. GetFolder, método
description: En el caso de scripting, obtiene una carpeta de tareas registradas.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder (método) Programador de tareas
- Método GetFolder Programador de tareas, objeto TaskService
- Programador de tareas de objeto TaskService, método GetFolder
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
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676989"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="17a1f-106">TaskService. GetFolder, método</span><span class="sxs-lookup"><span data-stu-id="17a1f-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="17a1f-107">En el caso de scripting, obtiene una carpeta de tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="17a1f-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a1f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17a1f-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="17a1f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17a1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a1f-110">*ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17a1f-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a1f-111">Ruta de acceso a la carpeta que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="17a1f-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="17a1f-112">No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="17a1f-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="17a1f-113">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) .</span><span class="sxs-lookup"><span data-stu-id="17a1f-113">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="17a1f-114">Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="17a1f-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="17a1f-115">No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. '</span><span class="sxs-lookup"><span data-stu-id="17a1f-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="17a1f-116">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="17a1f-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a1f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17a1f-117">Return value</span></span>

<span data-ttu-id="17a1f-118">Objeto [**TaskFolder**](taskfolder.md) para la carpeta solicitada.</span><span class="sxs-lookup"><span data-stu-id="17a1f-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a1f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17a1f-119">Requirements</span></span>



| <span data-ttu-id="17a1f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="17a1f-120">Requirement</span></span> | <span data-ttu-id="17a1f-121">Value</span><span class="sxs-lookup"><span data-stu-id="17a1f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a1f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17a1f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="17a1f-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17a1f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="17a1f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17a1f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="17a1f-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="17a1f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17a1f-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="17a1f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="17a1f-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17a1f-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17a1f-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17a1f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a1f-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17a1f-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a1f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="17a1f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a1f-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="17a1f-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





