---
title: Propiedad de estado ITsSbTaskInfo
description: Recupera un \_ \_ valor de enumeración de estado de la tarea RDV que representa el estado de la tarea.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Propiedad status Servicios de Escritorio remoto
- Propiedad status Servicios de Escritorio remoto, interfaz ITsSbTaskInfo
- Servicios de Escritorio remoto de la interfaz ITsSbTaskInfo, propiedad status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802132"
---
# <a name="itssbtaskinfostatus-property"></a><span data-ttu-id="42f61-106">ITsSbTaskInfo:: status (propiedad)</span><span class="sxs-lookup"><span data-stu-id="42f61-106">ITsSbTaskInfo::Status property</span></span>

<span data-ttu-id="42f61-107">Recupera un valor de enumeración de [**\_ \_ Estado de la tarea RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="42f61-107">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

<span data-ttu-id="42f61-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="42f61-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f61-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42f61-109">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a><span data-ttu-id="42f61-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="42f61-110">Property value</span></span>

<span data-ttu-id="42f61-111">Un valor de enumeración de [**\_ \_ Estado de la tarea RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="42f61-111">An [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f61-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f61-112">Requirements</span></span>



| <span data-ttu-id="42f61-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f61-113">Requirement</span></span> | <span data-ttu-id="42f61-114">Value</span><span class="sxs-lookup"><span data-stu-id="42f61-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42f61-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f61-115">Minimum supported client</span></span><br/> | <span data-ttu-id="42f61-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="42f61-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="42f61-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f61-117">Minimum supported server</span></span><br/> | <span data-ttu-id="42f61-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42f61-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="42f61-119">IDL</span><span class="sxs-lookup"><span data-stu-id="42f61-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42f61-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42f61-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f61-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="42f61-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f61-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="42f61-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





