---
title: Elemento AllowHardTerminate (settingsType)
description: Especifica que la tarea puede terminar con TerminateProcess.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- AllowHardTerminate (settingsType), elemento Programador de tareas
- Programador de tareas del elemento AllowHardTerminate
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685909"
---
# <a name="allowhardterminate-settingstype-element"></a><span data-ttu-id="c833a-105">Elemento AllowHardTerminate (settingsType)</span><span class="sxs-lookup"><span data-stu-id="c833a-105">AllowHardTerminate (settingsType) Element</span></span>

<span data-ttu-id="c833a-106">Especifica que la tarea puede terminar con TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="c833a-106">Specifies that the task may be terminated using TerminateProcess.</span></span>

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="c833a-107">El elemento **AllowHardTerminate** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c833a-107">The **AllowHardTerminate** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c833a-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c833a-108">Parent element</span></span>



| <span data-ttu-id="c833a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c833a-109">Element</span></span>                                                           | <span data-ttu-id="c833a-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c833a-110">Derived from</span></span>                                                 | <span data-ttu-id="c833a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c833a-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c833a-112">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="c833a-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c833a-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="c833a-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="c833a-114">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="c833a-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c833a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c833a-115">Remarks</span></span>

<span data-ttu-id="c833a-116">Para el desarrollo de C++, vea la [**propiedad AllowHardTerminate de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span><span class="sxs-lookup"><span data-stu-id="c833a-116">For C++ development, see the [**AllowHardTerminate property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span></span>

<span data-ttu-id="c833a-117">Para el desarrollo de scripts, vea [**TaskSettings. AllowHardTerminate**](tasksettings-allowhardterminate.md).</span><span class="sxs-lookup"><span data-stu-id="c833a-117">For script development, see [**TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c833a-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c833a-118">Examples</span></span>

<span data-ttu-id="c833a-119">Para obtener un ejemplo completo del XML de una tarea que permite la terminación completa, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="c833a-119">For a complete example of the XML for a task that allows hard termination, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c833a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c833a-120">Requirements</span></span>



| <span data-ttu-id="c833a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c833a-121">Requirement</span></span> | <span data-ttu-id="c833a-122">Value</span><span class="sxs-lookup"><span data-stu-id="c833a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c833a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c833a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c833a-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c833a-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c833a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c833a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c833a-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c833a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c833a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c833a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c833a-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="c833a-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





