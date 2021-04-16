---
title: TaskService. NewTask, método
description: En el caso de scripting, devuelve un objeto de definición de tarea vacía que se rellenará con la configuración y las propiedades y, a continuación, se registrará mediante el método TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Método NewTask Programador de tareas
- Método NewTask Programador de tareas, objeto TaskService
- Programador de tareas objeto TaskService, NewTask (método)
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686218"
---
# <a name="taskservicenewtask-method"></a><span data-ttu-id="2e9be-106">TaskService. NewTask, método</span><span class="sxs-lookup"><span data-stu-id="2e9be-106">TaskService.NewTask method</span></span>

<span data-ttu-id="2e9be-107">En el caso de scripting, devuelve un objeto de definición de tarea vacía que se rellenará con la configuración y las propiedades y, a continuación, se registrará mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="2e9be-107">For scripting, returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9be-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e9be-108">Syntax</span></span>


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="2e9be-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e9be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9be-110">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2e9be-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9be-111">Este parámetro se reserva para uso futuro y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="2e9be-111">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e9be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e9be-112">Return value</span></span>

<span data-ttu-id="2e9be-113">La definición de tarea que especifica toda la información necesaria para crear una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="2e9be-113">The task definition that specifies all the information required to create a new task.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9be-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e9be-114">Requirements</span></span>



| <span data-ttu-id="2e9be-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e9be-115">Requirement</span></span> | <span data-ttu-id="2e9be-116">Value</span><span class="sxs-lookup"><span data-stu-id="2e9be-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9be-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e9be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9be-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e9be-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2e9be-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e9be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9be-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e9be-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e9be-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2e9be-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e9be-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2e9be-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2e9be-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e9be-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e9be-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e9be-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





