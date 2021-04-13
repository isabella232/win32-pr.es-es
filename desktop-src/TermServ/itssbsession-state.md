---
title: Propiedad de estado ITsSbSession
description: Recupera o especifica el estado de la sesión.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedad de estado
- Propiedad State Servicios de Escritorio remoto, interfaz ITsSbSession
- Interfaz ITsSbSession Servicios de Escritorio remoto, propiedad State
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492994"
---
# <a name="itssbsessionstate-property"></a><span data-ttu-id="cb35f-106">ITsSbSession:: State (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cb35f-106">ITsSbSession::State property</span></span>

<span data-ttu-id="cb35f-107">Recupera o especifica el estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="cb35f-107">Retrieves or specifies the session state.</span></span>

<span data-ttu-id="cb35f-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cb35f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb35f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb35f-109">Syntax</span></span>


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a><span data-ttu-id="cb35f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cb35f-110">Property value</span></span>

<span data-ttu-id="cb35f-111">Un valor de la enumeración de [**\_ Estado TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) que indica el estado de una sesión.</span><span class="sxs-lookup"><span data-stu-id="cb35f-111">A value of the [**TSSESSION\_STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) enumeration that indicates the state of a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb35f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb35f-112">Requirements</span></span>



| <span data-ttu-id="cb35f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb35f-113">Requirement</span></span> | <span data-ttu-id="cb35f-114">Value</span><span class="sxs-lookup"><span data-stu-id="cb35f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb35f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb35f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cb35f-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb35f-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="cb35f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb35f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cb35f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb35f-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="cb35f-119">IDL</span><span class="sxs-lookup"><span data-stu-id="cb35f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb35f-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb35f-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb35f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb35f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb35f-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="cb35f-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[<span data-ttu-id="cb35f-123">**Estado de TSSESSION \_**</span><span class="sxs-lookup"><span data-stu-id="cb35f-123">**TSSESSION\_STATE**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





