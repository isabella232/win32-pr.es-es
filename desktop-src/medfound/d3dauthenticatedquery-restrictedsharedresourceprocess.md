---
description: Devuelve información sobre un proceso que puede abrir recursos compartidos con acceso restringido.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714923"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a><span data-ttu-id="3b270-103">D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS</span><span class="sxs-lookup"><span data-stu-id="3b270-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS</span></span>

<span data-ttu-id="3b270-104">Devuelve información sobre un proceso que puede abrir recursos compartidos con acceso restringido.</span><span class="sxs-lookup"><span data-stu-id="3b270-104">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="3b270-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b270-105">Requirement</span></span> | <span data-ttu-id="3b270-106">Value</span><span class="sxs-lookup"><span data-stu-id="3b270-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b270-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="3b270-107">Query GUID</span></span>  | <span data-ttu-id="3b270-108">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**</span><span class="sxs-lookup"><span data-stu-id="3b270-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>                                                                                           |
| <span data-ttu-id="3b270-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="3b270-109">Input data</span></span>  | [<span data-ttu-id="3b270-110">**\_Entrada QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="3b270-110">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| <span data-ttu-id="3b270-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="3b270-111">Return data</span></span> | [<span data-ttu-id="3b270-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**</span><span class="sxs-lookup"><span data-stu-id="3b270-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="3b270-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b270-113">Remarks</span></span>

<span data-ttu-id="3b270-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="3b270-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="3b270-115">**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="3b270-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="3b270-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="3b270-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="3b270-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b270-117">Requirements</span></span>



| <span data-ttu-id="3b270-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b270-118">Requirement</span></span> | <span data-ttu-id="3b270-119">Value</span><span class="sxs-lookup"><span data-stu-id="3b270-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b270-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b270-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b270-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b270-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3b270-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b270-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b270-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b270-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b270-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b270-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b270-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b270-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b270-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b270-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b270-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="3b270-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="3b270-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="3b270-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="3b270-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="3b270-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




