---
title: Identificador (networkSettingsType) (elemento)
description: Contiene un valor GUID que identifica un perfil de red.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Elemento ID Programador de tareas
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151182"
---
# <a name="id-networksettingstype-element"></a><span data-ttu-id="73bfd-104">Identificador (networkSettingsType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="73bfd-104">Id (networkSettingsType) Element</span></span>

<span data-ttu-id="73bfd-105">Contiene un valor GUID que identifica un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="73bfd-105">Contains a GUID value that identifies a network profile.</span></span>

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

<span data-ttu-id="73bfd-106">El elemento **ID** se define mediante el tipo complejo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="73bfd-106">The **Id** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="73bfd-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="73bfd-107">Parent element</span></span>



| <span data-ttu-id="73bfd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="73bfd-108">Element</span></span>                                                                                            | <span data-ttu-id="73bfd-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="73bfd-109">Derived from</span></span>                                                                       | <span data-ttu-id="73bfd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="73bfd-110">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73bfd-111">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="73bfd-111">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="73bfd-112">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="73bfd-112">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="73bfd-113">Contiene la configuración que usa el servicio de Programador de tareas para obtener un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="73bfd-113">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="73bfd-114">El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="73bfd-114">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="73bfd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73bfd-115">Remarks</span></span>

<span data-ttu-id="73bfd-116">Para el desarrollo de C++, vea [**propiedad ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span><span class="sxs-lookup"><span data-stu-id="73bfd-116">For C++ development, see [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span></span>

<span data-ttu-id="73bfd-117">Para el desarrollo de scripts, vea [**NetworkSettings.ID**](networksettings-id.md).</span><span class="sxs-lookup"><span data-stu-id="73bfd-117">For script development, see [**NetworkSettings.Id**](networksettings-id.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73bfd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73bfd-118">Requirements</span></span>



| <span data-ttu-id="73bfd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="73bfd-119">Requirement</span></span> | <span data-ttu-id="73bfd-120">Value</span><span class="sxs-lookup"><span data-stu-id="73bfd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="73bfd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73bfd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73bfd-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73bfd-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73bfd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73bfd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73bfd-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="73bfd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





