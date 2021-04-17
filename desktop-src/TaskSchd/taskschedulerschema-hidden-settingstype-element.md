---
title: Elemento Hidden (settingsType)
description: Especifica que la tarea no será visible de forma predeterminada en la interfaz de usuario.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Programador de tareas de elementos ocultos
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676997"
---
# <a name="hidden-settingstype-element"></a><span data-ttu-id="2919f-104">Elemento Hidden (settingsType)</span><span class="sxs-lookup"><span data-stu-id="2919f-104">Hidden (settingsType) Element</span></span>

<span data-ttu-id="2919f-105">Especifica que la tarea no será visible de forma predeterminada en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2919f-105">Specifies that the task will not be visible in the UI by default.</span></span> <span data-ttu-id="2919f-106">Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador principal" que hace que todas las tareas sean visibles en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2919f-106">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="2919f-107">El elemento **Hidden** se define mediante el tipo complejo [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2919f-107">The **Hidden** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2919f-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2919f-108">Parent element</span></span>



| <span data-ttu-id="2919f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2919f-109">Element</span></span>                                                           | <span data-ttu-id="2919f-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2919f-110">Derived from</span></span>                                                         | <span data-ttu-id="2919f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2919f-111">Description</span></span>                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="2919f-112">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="2919f-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="2919f-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="2919f-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="2919f-114">Contiene la configuración que usa Programador de tareas para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="2919f-114">Contains the settings that Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2919f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2919f-115">Remarks</span></span>

<span data-ttu-id="2919f-116">Para el desarrollo de C++, vea [**Hidden (propiedad) de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span><span class="sxs-lookup"><span data-stu-id="2919f-116">For C++ development, see [**Hidden Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span></span>

<span data-ttu-id="2919f-117">Para el desarrollo de scripts, vea [**TaskSettings. Hidden**](tasksettings-hidden.md).</span><span class="sxs-lookup"><span data-stu-id="2919f-117">For script development, see [**TaskSettings.Hidden**](tasksettings-hidden.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2919f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2919f-118">Requirements</span></span>



| <span data-ttu-id="2919f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2919f-119">Requirement</span></span> | <span data-ttu-id="2919f-120">Value</span><span class="sxs-lookup"><span data-stu-id="2919f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2919f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2919f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2919f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2919f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2919f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2919f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2919f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2919f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2919f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2919f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2919f-126">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="2919f-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





