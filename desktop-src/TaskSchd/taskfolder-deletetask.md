---
title: TaskFolder. DeleteTask, método
description: En el caso de scripting, elimina una tarea de la carpeta.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Método DeleteTask Programador de tareas
- Método DeleteTask Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, método DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802780"
---
# <a name="taskfolderdeletetask-method"></a><span data-ttu-id="6496f-106">TaskFolder. DeleteTask, método</span><span class="sxs-lookup"><span data-stu-id="6496f-106">TaskFolder.DeleteTask method</span></span>

<span data-ttu-id="6496f-107">En el caso de scripting, elimina una tarea de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6496f-107">For scripting, deletes a task from the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="6496f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6496f-108">Syntax</span></span>


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="6496f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6496f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6496f-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6496f-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6496f-111">El nombre de la tarea que se especifica cuando se registró la tarea.</span><span class="sxs-lookup"><span data-stu-id="6496f-111">The name of the task that is specified when the task was registered.</span></span> <span data-ttu-id="6496f-112">No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. '</span><span class="sxs-lookup"><span data-stu-id="6496f-112">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="6496f-113">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6496f-113">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="6496f-114">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6496f-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6496f-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="6496f-115">Not supported.</span></span> <span data-ttu-id="6496f-116">El valor es 0</span><span class="sxs-lookup"><span data-stu-id="6496f-116">Value is 0</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6496f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6496f-117">Return value</span></span>

<span data-ttu-id="6496f-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6496f-118">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6496f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6496f-119">Requirements</span></span>



| <span data-ttu-id="6496f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6496f-120">Requirement</span></span> | <span data-ttu-id="6496f-121">Value</span><span class="sxs-lookup"><span data-stu-id="6496f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6496f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6496f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6496f-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6496f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6496f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6496f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6496f-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6496f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6496f-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6496f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6496f-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6496f-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6496f-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6496f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6496f-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6496f-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6496f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6496f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6496f-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6496f-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





