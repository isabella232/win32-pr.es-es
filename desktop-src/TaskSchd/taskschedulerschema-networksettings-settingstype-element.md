---
title: Elemento NetworkSettings (settingsType)
description: Contiene la configuración que usa el servicio de Programador de tareas para obtener un perfil de red. El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento RunOnlyIfNetworkAvailable está establecido en true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Programador de tareas del elemento NetworkSettings
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491356"
---
# <a name="networksettings-settingstype-element"></a><span data-ttu-id="8878b-105">Elemento NetworkSettings (settingsType)</span><span class="sxs-lookup"><span data-stu-id="8878b-105">NetworkSettings (settingsType) Element</span></span>

<span data-ttu-id="8878b-106">Contiene la configuración que usa el servicio de Programador de tareas para obtener un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="8878b-106">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="8878b-107">El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="8878b-107">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span>

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="8878b-108">El elemento **NetworkSettings** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8878b-108">The **NetworkSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8878b-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8878b-109">Parent element</span></span>



| <span data-ttu-id="8878b-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="8878b-110">Element</span></span>                                                                      | <span data-ttu-id="8878b-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8878b-111">Derived from</span></span>                                                         | <span data-ttu-id="8878b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8878b-112">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8878b-113">**Configuración (taskType)**</span><span class="sxs-lookup"><span data-stu-id="8878b-113">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="8878b-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="8878b-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="8878b-115">Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8878b-115">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8878b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8878b-116">Remarks</span></span>

<span data-ttu-id="8878b-117">Para el desarrollo de C++, consulte la [**propiedad NetworkSettings de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span><span class="sxs-lookup"><span data-stu-id="8878b-117">For C++ development, see [**NetworkSettings Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span></span>

<span data-ttu-id="8878b-118">Para el desarrollo de scripts, vea [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md).</span><span class="sxs-lookup"><span data-stu-id="8878b-118">For script development, see [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8878b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8878b-119">Requirements</span></span>



| <span data-ttu-id="8878b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8878b-120">Requirement</span></span> | <span data-ttu-id="8878b-121">Value</span><span class="sxs-lookup"><span data-stu-id="8878b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8878b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8878b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8878b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8878b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8878b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8878b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8878b-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8878b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





