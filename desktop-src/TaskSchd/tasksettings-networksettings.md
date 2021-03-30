---
title: Propiedad TaskSettings. NetworkSettings
description: Para scripting, obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de Perfil de red.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Programador de tareas de la propiedad NetworkSettings
- Programador de tareas de la propiedad NetworkSettings, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801471"
---
# <a name="tasksettingsnetworksettings-property"></a><span data-ttu-id="3109e-106">Propiedad TaskSettings. NetworkSettings</span><span class="sxs-lookup"><span data-stu-id="3109e-106">TaskSettings.NetworkSettings property</span></span>

<span data-ttu-id="3109e-107">Para scripting, obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de Perfil de red.</span><span class="sxs-lookup"><span data-stu-id="3109e-107">For scripting, gets or sets the network settings object that contains a network profile identifier and name.</span></span> <span data-ttu-id="3109e-108">Si la propiedad [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) es **true** y se especifica una Propfile de red en la propiedad **NetworkSettings** , la tarea se ejecutará solo si el perfil de red especificado está disponible.</span><span class="sxs-lookup"><span data-stu-id="3109e-108">If the [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) property of [**TaskSettings**](tasksettings.md) is **True** and a network propfile is specified in the **NetworkSettings** property, then the task will run only if the specified network profile is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="3109e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3109e-109">Syntax</span></span>


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a><span data-ttu-id="3109e-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3109e-110">Property value</span></span>

<span data-ttu-id="3109e-111">Un objeto [**NetworkSettings**](networksettings.md) que contiene un identificador y un nombre de Perfil de red.</span><span class="sxs-lookup"><span data-stu-id="3109e-111">A [**NetworkSettings**](networksettings.md) object that contains a network profile identifier and name.</span></span>

## <a name="requirements"></a><span data-ttu-id="3109e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3109e-112">Requirements</span></span>



| <span data-ttu-id="3109e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3109e-113">Requirement</span></span> | <span data-ttu-id="3109e-114">Value</span><span class="sxs-lookup"><span data-stu-id="3109e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3109e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3109e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3109e-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3109e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3109e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3109e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3109e-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3109e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3109e-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3109e-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3109e-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3109e-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3109e-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3109e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3109e-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3109e-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3109e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3109e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3109e-124">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="3109e-124">**TaskSettings**</span></span>](tasksettings.md)
</dt> <dt>

[<span data-ttu-id="3109e-125">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="3109e-125">**NetworkSettings**</span></span>](networksettings.md)
</dt> </dl>

 

 





