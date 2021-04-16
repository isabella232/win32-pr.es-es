---
title: Exec (actionGroup), elemento
description: Especifica una acción que ejecuta una operación de línea de comandos.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Elemento exec Programador de tareas
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678651"
---
# <a name="exec-actiongroup-element"></a><span data-ttu-id="2b34d-104">Exec (actionGroup), elemento</span><span class="sxs-lookup"><span data-stu-id="2b34d-104">Exec (actionGroup) Element</span></span>

<span data-ttu-id="2b34d-105">Especifica una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="2b34d-105">Specifies an action that executes a command-line operation.</span></span>

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

<span data-ttu-id="2b34d-106">El elemento **exec** está definido por [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="2b34d-106">The **Exec** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="2b34d-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2b34d-107">Parent element</span></span>



| <span data-ttu-id="2b34d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2b34d-108">Element</span></span>                                                         | <span data-ttu-id="2b34d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2b34d-109">Derived from</span></span>                                                       | <span data-ttu-id="2b34d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b34d-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="2b34d-111">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="2b34d-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="2b34d-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="2b34d-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="2b34d-113">Contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="2b34d-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="2b34d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2b34d-114">Child elements</span></span>



| <span data-ttu-id="2b34d-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="2b34d-115">Element</span></span>                                                                           | <span data-ttu-id="2b34d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b34d-116">Type</span></span>       | <span data-ttu-id="2b34d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b34d-117">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b34d-118">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="2b34d-118">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="2b34d-119">**string**</span><span class="sxs-lookup"><span data-stu-id="2b34d-119">**string**</span></span> | <span data-ttu-id="2b34d-120">Especifica los argumentos asociados con la operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="2b34d-120">Specifies the arguments associated with the command-line operation.</span></span><br/>                               |
| [<span data-ttu-id="2b34d-121">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="2b34d-121">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | <span data-ttu-id="2b34d-122">**string**</span><span class="sxs-lookup"><span data-stu-id="2b34d-122">**string**</span></span> | <span data-ttu-id="2b34d-123">Especifica el archivo ejecutable o el documento que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="2b34d-123">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="2b34d-124">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="2b34d-124">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | <span data-ttu-id="2b34d-125">string</span><span class="sxs-lookup"><span data-stu-id="2b34d-125">string</span></span>     | <span data-ttu-id="2b34d-126">Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="2b34d-126">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="2b34d-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b34d-127">Attributes</span></span>



| <span data-ttu-id="2b34d-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b34d-128">Name</span></span> | <span data-ttu-id="2b34d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b34d-129">Type</span></span>       | <span data-ttu-id="2b34d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b34d-130">Description</span></span>                                                    |
|------|------------|----------------------------------------------------------------|
| <span data-ttu-id="2b34d-131">id</span><span class="sxs-lookup"><span data-stu-id="2b34d-131">id</span></span>   | <span data-ttu-id="2b34d-132">**string**</span><span class="sxs-lookup"><span data-stu-id="2b34d-132">**string**</span></span> | <span data-ttu-id="2b34d-133">Identificador de la acción realizada por la tarea.</span><span class="sxs-lookup"><span data-stu-id="2b34d-133">The identifier of the action performed by the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2b34d-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b34d-134">Remarks</span></span>

<span data-ttu-id="2b34d-135">Los elementos secundarios enumerados anteriormente se definen mediante el tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2b34d-135">The child elements listed above are defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

<span data-ttu-id="2b34d-136">Para el desarrollo de scripts, se define una acción de ejecución mediante el objeto [**ExecAction**](execaction.md) .</span><span class="sxs-lookup"><span data-stu-id="2b34d-136">For script development, an execution action is defined by the [**ExecAction**](execaction.md) object.</span></span>

<span data-ttu-id="2b34d-137">En el desarrollo de C++, la interfaz [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) define una acción de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2b34d-137">For C++ development, an execution action is defined by the [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) interface.</span></span>

<span data-ttu-id="2b34d-138">Si se usan variables de entorno en los elementos [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)o [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , los valores de las variables de entorno se almacenan en caché y se usan cuando se inicia el Taskeng.exe (el motor de tareas).</span><span class="sxs-lookup"><span data-stu-id="2b34d-138">If environment variables are used in the [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md), or [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) elements, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="2b34d-139">El motor de tareas no utilizará los cambios en las variables de entorno que se producen después de iniciar el motor de tareas.</span><span class="sxs-lookup"><span data-stu-id="2b34d-139">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

## <a name="examples"></a><span data-ttu-id="2b34d-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2b34d-140">Examples</span></span>

<span data-ttu-id="2b34d-141">Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador de eventos, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="2b34d-141">For a complete example of the XML for a task that uses an event trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b34d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b34d-142">Requirements</span></span>



| <span data-ttu-id="2b34d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b34d-143">Requirement</span></span> | <span data-ttu-id="2b34d-144">Value</span><span class="sxs-lookup"><span data-stu-id="2b34d-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b34d-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b34d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2b34d-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2b34d-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2b34d-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b34d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2b34d-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b34d-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b34d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b34d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b34d-150">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="2b34d-150">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





