---
title: Arguments (execType), elemento
description: Especifica los argumentos asociados con la operación de línea de comandos.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Arguments (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534581"
---
# <a name="arguments-exectype-element"></a><span data-ttu-id="f844d-104">Arguments (execType), elemento</span><span class="sxs-lookup"><span data-stu-id="f844d-104">Arguments (execType) Element</span></span>

<span data-ttu-id="f844d-105">Especifica los argumentos asociados con la operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f844d-105">Specifies the arguments associated with the command-line operation.</span></span>

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

<span data-ttu-id="f844d-106">El elemento **arguments** se define mediante el tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f844d-106">The **Arguments** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f844d-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f844d-107">Parent element</span></span>



| <span data-ttu-id="f844d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f844d-108">Element</span></span>                                                      | <span data-ttu-id="f844d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f844d-109">Derived from</span></span>                                                 | <span data-ttu-id="f844d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f844d-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f844d-111">**Ejec**</span><span class="sxs-lookup"><span data-stu-id="f844d-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="f844d-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="f844d-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="f844d-113">Especifica una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f844d-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f844d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f844d-114">Remarks</span></span>

<span data-ttu-id="f844d-115">Para el desarrollo de C++, vea la [**propiedad arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="f844d-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="f844d-116">Para el desarrollo de scripts, vea [**ExecAction. arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="f844d-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f844d-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f844d-117">Examples</span></span>

<span data-ttu-id="f844d-118">Para obtener un ejemplo completo del XML de una tarea que usa una acción ejecutable, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="f844d-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f844d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f844d-119">Requirements</span></span>



| <span data-ttu-id="f844d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f844d-120">Requirement</span></span> | <span data-ttu-id="f844d-121">Value</span><span class="sxs-lookup"><span data-stu-id="f844d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f844d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f844d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f844d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f844d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f844d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f844d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f844d-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f844d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f844d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f844d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f844d-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="f844d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





