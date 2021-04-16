---
title: Elemento WorkingDirectory (execType)
description: Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el archivo ejecutable.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Programador de tareas del elemento WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686220"
---
# <a name="workingdirectory-exectype-element"></a><span data-ttu-id="316d4-104">Elemento WorkingDirectory (execType)</span><span class="sxs-lookup"><span data-stu-id="316d4-104">WorkingDirectory (execType) Element</span></span>

<span data-ttu-id="316d4-105">Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="316d4-105">Specifies the directory where either the executable or those files used by the executable exists.</span></span>

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

<span data-ttu-id="316d4-106">El elemento **WorkingDirectory** se define mediante el tipo complejo de [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="316d4-106">The **WorkingDirectory** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="316d4-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="316d4-107">Parent element</span></span>



| <span data-ttu-id="316d4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="316d4-108">Element</span></span>                                                      | <span data-ttu-id="316d4-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="316d4-109">Derived from</span></span>                                                 | <span data-ttu-id="316d4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="316d4-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="316d4-111">**Ejec**</span><span class="sxs-lookup"><span data-stu-id="316d4-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="316d4-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="316d4-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="316d4-113">Especifica una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="316d4-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="316d4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="316d4-114">Remarks</span></span>

<span data-ttu-id="316d4-115">Para el desarrollo de scripts, el directorio de trabajo se especifica mediante la propiedad [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="316d4-115">For script development, the working directory is specified by the [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) property.</span></span>

<span data-ttu-id="316d4-116">En el desarrollo de C++, el directorio de trabajo se especifica mediante la propiedad [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .</span><span class="sxs-lookup"><span data-stu-id="316d4-116">For C++ development, the working directory is specified by the [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) property.</span></span>

## <a name="examples"></a><span data-ttu-id="316d4-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="316d4-117">Examples</span></span>

<span data-ttu-id="316d4-118">En el código XML siguiente se define una acción de ejecución.</span><span class="sxs-lookup"><span data-stu-id="316d4-118">The following XML defines a execution action.</span></span>


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a><span data-ttu-id="316d4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="316d4-119">Requirements</span></span>



| <span data-ttu-id="316d4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="316d4-120">Requirement</span></span> | <span data-ttu-id="316d4-121">Value</span><span class="sxs-lookup"><span data-stu-id="316d4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="316d4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="316d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="316d4-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="316d4-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="316d4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="316d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="316d4-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="316d4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="316d4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="316d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="316d4-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="316d4-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="316d4-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="316d4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





