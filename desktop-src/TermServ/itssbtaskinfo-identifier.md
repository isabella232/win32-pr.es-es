---
title: Propiedad de identificador ITsSbTaskInfo
description: Recupera un GUID que el agente de tareas usa como identificador único.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Propiedad Identifier Servicios de Escritorio remoto
- Propiedad de identificador Servicios de Escritorio remoto, interfaz ITsSbTaskInfo
- Servicios de Escritorio remoto de la interfaz ITsSbTaskInfo, propiedad Identifier
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803878"
---
# <a name="itssbtaskinfoidentifier-property"></a><span data-ttu-id="c0746-106">ITsSbTaskInfo:: Identifier (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c0746-106">ITsSbTaskInfo::Identifier property</span></span>

<span data-ttu-id="c0746-107">Recupera un GUID que el agente de tareas usa como identificador único.</span><span class="sxs-lookup"><span data-stu-id="c0746-107">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

<span data-ttu-id="c0746-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c0746-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0746-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0746-109">Syntax</span></span>


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a><span data-ttu-id="c0746-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c0746-110">Property value</span></span>

<span data-ttu-id="c0746-111">Un puntero a un valor **BSTR** que recibe el GUID.</span><span class="sxs-lookup"><span data-stu-id="c0746-111">A pointer to a **BSTR** value that receives the GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0746-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0746-112">Requirements</span></span>



| <span data-ttu-id="c0746-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0746-113">Requirement</span></span> | <span data-ttu-id="c0746-114">Value</span><span class="sxs-lookup"><span data-stu-id="c0746-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0746-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0746-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c0746-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c0746-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c0746-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0746-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c0746-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0746-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="c0746-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c0746-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0746-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0746-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0746-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0746-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="c0746-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





