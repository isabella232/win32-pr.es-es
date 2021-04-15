---
title: Elemento Command (execType)
description: Especifica el archivo ejecutable o el documento que se va a ejecutar.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Programador de tareas del elemento Command
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422522"
---
# <a name="command-exectype-element"></a><span data-ttu-id="eeac8-104">Elemento Command (execType)</span><span class="sxs-lookup"><span data-stu-id="eeac8-104">Command (execType) Element</span></span>

<span data-ttu-id="eeac8-105">Especifica el archivo ejecutable o el documento que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="eeac8-105">Specifies the executable file or document to be run.</span></span>

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

<span data-ttu-id="eeac8-106">El elemento **Command** se define mediante el tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eeac8-106">The **Command** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="eeac8-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="eeac8-107">Parent element</span></span>



| <span data-ttu-id="eeac8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="eeac8-108">Element</span></span>                                                      | <span data-ttu-id="eeac8-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="eeac8-109">Derived from</span></span>                                                 | <span data-ttu-id="eeac8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeac8-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="eeac8-111">**Ejec**</span><span class="sxs-lookup"><span data-stu-id="eeac8-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="eeac8-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="eeac8-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="eeac8-113">Especifica una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="eeac8-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eeac8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeac8-114">Remarks</span></span>

<span data-ttu-id="eeac8-115">Para el desarrollo de C++, vea la [**propiedad arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="eeac8-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="eeac8-116">Para el desarrollo de scripts, vea [**ExecAction. arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="eeac8-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eeac8-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eeac8-117">Examples</span></span>

<span data-ttu-id="eeac8-118">Para obtener un ejemplo completo del XML de una tarea que usa una acción ejecutable, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="eeac8-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeac8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeac8-119">Requirements</span></span>



| <span data-ttu-id="eeac8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeac8-120">Requirement</span></span> | <span data-ttu-id="eeac8-121">Value</span><span class="sxs-lookup"><span data-stu-id="eeac8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eeac8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeac8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eeac8-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eeac8-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eeac8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeac8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eeac8-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eeac8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eeac8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeac8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeac8-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="eeac8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





