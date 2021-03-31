---
title: Elemento NetworkProfileName (settingsType)
description: Contiene el nombre de un perfil de red. El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento RunOnlyIfNetworkAvailable está establecido en true. El nombre se usa para fines de presentación.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Programador de tareas del elemento NetworkProfileName
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802768"
---
# <a name="networkprofilename-settingstype-element"></a><span data-ttu-id="d6dd9-106">Elemento NetworkProfileName (settingsType)</span><span class="sxs-lookup"><span data-stu-id="d6dd9-106">NetworkProfileName (settingsType) Element</span></span>

<span data-ttu-id="d6dd9-107">Contiene el nombre de un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="d6dd9-107">Contains the name of a network profile.</span></span> <span data-ttu-id="d6dd9-108">El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="d6dd9-108">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="d6dd9-109">El nombre se usa para fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="d6dd9-109">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="d6dd9-110">El elemento **NetworkProfileName** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d6dd9-110">The **NetworkProfileName** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d6dd9-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d6dd9-111">Parent element</span></span>



| <span data-ttu-id="d6dd9-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="d6dd9-112">Element</span></span>                                                                      | <span data-ttu-id="d6dd9-113">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d6dd9-113">Derived from</span></span>                                                         | <span data-ttu-id="d6dd9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6dd9-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6dd9-115">**Configuración (taskType)**</span><span class="sxs-lookup"><span data-stu-id="d6dd9-115">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="d6dd9-116">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="d6dd9-116">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="d6dd9-117">Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="d6dd9-117">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d6dd9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6dd9-118">Requirements</span></span>



| <span data-ttu-id="d6dd9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6dd9-119">Requirement</span></span> | <span data-ttu-id="d6dd9-120">Value</span><span class="sxs-lookup"><span data-stu-id="d6dd9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6dd9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6dd9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dd9-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d6dd9-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6dd9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6dd9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dd9-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6dd9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





