---
title: Propiedad TargetName de ITsSbSession
description: Recupera el nombre del destino en el que se creó esta sesión.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Propiedad TargetName Servicios de Escritorio remoto
- Propiedad TargetName Servicios de Escritorio remoto, interfaz ITsSbSession
- Servicios de Escritorio remoto de la interfaz ITsSbSession, propiedad TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686206"
---
# <a name="itssbsessiontargetname-property"></a><span data-ttu-id="ac862-106">ITsSbSession:: TargetName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ac862-106">ITsSbSession::TargetName property</span></span>

<span data-ttu-id="ac862-107">Recupera el nombre del destino en el que se creó esta sesión.</span><span class="sxs-lookup"><span data-stu-id="ac862-107">Retrieves the name of the target on which this session was created.</span></span>

<span data-ttu-id="ac862-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ac862-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac862-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac862-109">Syntax</span></span>


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a><span data-ttu-id="ac862-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ac862-110">Property value</span></span>

<span data-ttu-id="ac862-111">Un puntero a una variable **BSTR** que recibe el nombre del destino en el que se creó esta sesión.</span><span class="sxs-lookup"><span data-stu-id="ac862-111">A pointer to a **BSTR** variable that receives the name of the target on which this session was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac862-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac862-112">Requirements</span></span>



| <span data-ttu-id="ac862-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac862-113">Requirement</span></span> | <span data-ttu-id="ac862-114">Value</span><span class="sxs-lookup"><span data-stu-id="ac862-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac862-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac862-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ac862-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ac862-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ac862-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac862-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ac862-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac862-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ac862-119">IDL</span><span class="sxs-lookup"><span data-stu-id="ac862-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac862-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac862-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac862-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac862-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac862-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="ac862-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





