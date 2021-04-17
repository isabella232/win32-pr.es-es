---
title: Nombre (networkSettingsType) (elemento)
description: Contiene el nombre de un perfil de red. El nombre se usa para fines de presentación.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Name (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534456"
---
# <a name="name-networksettingstype-element"></a><span data-ttu-id="beff4-105">Nombre (networkSettingsType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="beff4-105">Name (networkSettingsType) Element</span></span>

<span data-ttu-id="beff4-106">Contiene el nombre de un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="beff4-106">Contains the name of a network profile.</span></span> <span data-ttu-id="beff4-107">El nombre se usa para fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="beff4-107">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

<span data-ttu-id="beff4-108">El elemento **Name** se define mediante el tipo complejo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="beff4-108">The **Name** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="beff4-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="beff4-109">Parent element</span></span>



| <span data-ttu-id="beff4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="beff4-110">Element</span></span>                                                                                            | <span data-ttu-id="beff4-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="beff4-111">Derived from</span></span>                                                                       | <span data-ttu-id="beff4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="beff4-112">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beff4-113">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="beff4-113">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="beff4-114">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="beff4-114">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="beff4-115">Contiene la configuración que usa el servicio de Programador de tareas para obtener un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="beff4-115">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="beff4-116">El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="beff4-116">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="beff4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="beff4-117">Remarks</span></span>

<span data-ttu-id="beff4-118">Para el desarrollo de C++, vea la [**propiedad Name de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span><span class="sxs-lookup"><span data-stu-id="beff4-118">For C++ development, see [**Name Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span></span>

<span data-ttu-id="beff4-119">Para el desarrollo de scripts, vea [**NetworkSettings.Name**](networksettings-name.md).</span><span class="sxs-lookup"><span data-stu-id="beff4-119">For script development, see [**NetworkSettings.Name**](networksettings-name.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="beff4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beff4-120">Requirements</span></span>



| <span data-ttu-id="beff4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="beff4-121">Requirement</span></span> | <span data-ttu-id="beff4-122">Value</span><span class="sxs-lookup"><span data-stu-id="beff4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="beff4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beff4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="beff4-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="beff4-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="beff4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beff4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="beff4-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="beff4-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





