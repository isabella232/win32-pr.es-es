---
title: Objeto RegisteredTaskCollection
description: Objeto de scripting que contiene todas las tareas que están registradas.
ms.assetid: 0bd2010d-af25-4316-8829-62e4ec4761e2
keywords:
- Objeto RegisteredTaskCollection Programador de tareas
- Programador de tareas de objeto RegisteredTaskCollection, descrito
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11c299bc8817cc1627c40b3c465cd182e0f4c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079049"
---
# <a name="registeredtaskcollection-object"></a><span data-ttu-id="46e6b-105">Objeto RegisteredTaskCollection</span><span class="sxs-lookup"><span data-stu-id="46e6b-105">RegisteredTaskCollection object</span></span>

<span data-ttu-id="46e6b-106">Objeto de scripting que contiene todas las tareas que están registradas.</span><span class="sxs-lookup"><span data-stu-id="46e6b-106">Scripting object that contains all the tasks that are registered.</span></span>

## <a name="members"></a><span data-ttu-id="46e6b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="46e6b-107">Members</span></span>

<span data-ttu-id="46e6b-108">El objeto **RegisteredTaskCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="46e6b-108">The **RegisteredTaskCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="46e6b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46e6b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46e6b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46e6b-110">Properties</span></span>

<span data-ttu-id="46e6b-111">El objeto **RegisteredTaskCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="46e6b-111">The **RegisteredTaskCollection** object has these properties.</span></span>



| <span data-ttu-id="46e6b-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46e6b-112">Property</span></span>                                                   | <span data-ttu-id="46e6b-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="46e6b-113">Access type</span></span>          | <span data-ttu-id="46e6b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="46e6b-114">Description</span></span>                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="46e6b-115">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="46e6b-115">**Count**</span></span>](registeredtaskcollection-count.md)<br/> | <span data-ttu-id="46e6b-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="46e6b-116">Read-only</span></span><br/> | <span data-ttu-id="46e6b-117">Obtiene el número de tareas registradas en la colección.</span><span class="sxs-lookup"><span data-stu-id="46e6b-117">Gets the number of registered tasks in the collection.</span></span><br/>  |
| [<span data-ttu-id="46e6b-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46e6b-118">**Item**</span></span>](registeredtaskcollection-item.md)<br/>   | <span data-ttu-id="46e6b-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="46e6b-119">Read-only</span></span><br/> | <span data-ttu-id="46e6b-120">Obtiene la tarea registrada especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="46e6b-120">Gets the specified registered task from the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="46e6b-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="46e6b-121">Examples</span></span>

<span data-ttu-id="46e6b-122">Para obtener más información y código de ejemplo de este objeto de scripting, vea [Mostrar los nombres y los Estados de las tareas (scripting)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="46e6b-122">For more information and example code for this scripting object, see [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46e6b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e6b-123">Requirements</span></span>



| <span data-ttu-id="46e6b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e6b-124">Requirement</span></span> | <span data-ttu-id="46e6b-125">Value</span><span class="sxs-lookup"><span data-stu-id="46e6b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e6b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e6b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="46e6b-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="46e6b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="46e6b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e6b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="46e6b-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="46e6b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46e6b-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="46e6b-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="46e6b-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46e6b-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46e6b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46e6b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e6b-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46e6b-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e6b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="46e6b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e6b-135">**TaskFolder.GetTasks**</span><span class="sxs-lookup"><span data-stu-id="46e6b-135">**TaskFolder.GetTasks**</span></span>](taskfolder-gettasks.md)
</dt> </dl>

 

 





