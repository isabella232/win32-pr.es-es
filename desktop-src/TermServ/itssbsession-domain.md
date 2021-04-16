---
title: Propiedad de dominio ITsSbSession
description: Recupera el nombre de dominio del usuario.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedad de dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz ITsSbSession
- Servicios de Escritorio remoto de la interfaz ITsSbSession, propiedad del dominio
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686207"
---
# <a name="itssbsessiondomain-property"></a><span data-ttu-id="9ab15-106">ITsSbSession::D propiedad omain</span><span class="sxs-lookup"><span data-stu-id="9ab15-106">ITsSbSession::Domain property</span></span>

<span data-ttu-id="9ab15-107">Recupera el nombre de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="9ab15-107">Retrieves the domain name of the user.</span></span>

<span data-ttu-id="9ab15-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9ab15-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab15-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ab15-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a><span data-ttu-id="9ab15-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9ab15-110">Property value</span></span>

<span data-ttu-id="9ab15-111">Un puntero a una variable **BSTR** que recibe el nombre de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="9ab15-111">A pointer to a **BSTR** variable that receives the domain name of the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab15-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ab15-112">Requirements</span></span>



| <span data-ttu-id="9ab15-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ab15-113">Requirement</span></span> | <span data-ttu-id="9ab15-114">Value</span><span class="sxs-lookup"><span data-stu-id="9ab15-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab15-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ab15-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab15-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9ab15-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="9ab15-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ab15-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab15-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ab15-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="9ab15-119">IDL</span><span class="sxs-lookup"><span data-stu-id="9ab15-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ab15-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ab15-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab15-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ab15-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab15-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="9ab15-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





