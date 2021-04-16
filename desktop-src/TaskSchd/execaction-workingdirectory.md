---
title: Propiedad ExecAction. WorkingDirectory
description: En el caso de scripting, obtiene o establece el directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Programador de tareas de la propiedad WorkingDirectory
- Programador de tareas de la propiedad WorkingDirectory, objeto ExecAction
- Programador de tareas de objeto ExecAction, propiedad WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676685"
---
# <a name="execactionworkingdirectory-property"></a><span data-ttu-id="7ab67-106">Propiedad ExecAction. WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="7ab67-106">ExecAction.WorkingDirectory property</span></span>

<span data-ttu-id="7ab67-107">En el caso de scripting, obtiene o establece el directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7ab67-107">For scripting, gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab67-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ab67-108">Syntax</span></span>


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a><span data-ttu-id="7ab67-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7ab67-109">Property value</span></span>

<span data-ttu-id="7ab67-110">El directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7ab67-110">The directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ab67-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ab67-111">Remarks</span></span>

<span data-ttu-id="7ab67-112">Al leer o escribir XML, el directorio de trabajo de la aplicación se especifica en el elemento [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="7ab67-112">When reading or writing XML, the working directory of the application is specified in the [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="7ab67-113">La ruta de acceso se comprueba para asegurarse de que es válida cuando se registra la tarea, no cuando se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7ab67-113">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab67-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ab67-114">Requirements</span></span>



| <span data-ttu-id="7ab67-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab67-115">Requirement</span></span> | <span data-ttu-id="7ab67-116">Value</span><span class="sxs-lookup"><span data-stu-id="7ab67-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab67-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab67-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab67-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ab67-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7ab67-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab67-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab67-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ab67-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ab67-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7ab67-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ab67-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ab67-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ab67-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ab67-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ab67-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ab67-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab67-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ab67-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab67-126">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="7ab67-126">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="7ab67-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7ab67-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





