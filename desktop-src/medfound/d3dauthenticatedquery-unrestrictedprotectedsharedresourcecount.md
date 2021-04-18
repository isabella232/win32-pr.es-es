---
description: Devuelve el número de recursos compartidos protegidos que puede abrir cualquier proceso sin restricciones.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666207"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a><span data-ttu-id="9e720-103">D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span><span class="sxs-lookup"><span data-stu-id="9e720-103">D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span></span>

<span data-ttu-id="9e720-104">Devuelve el número de recursos compartidos protegidos que puede abrir cualquier proceso sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="9e720-104">Returns the number of protected shared resources that can be opened by any process without restrictions.</span></span>



| <span data-ttu-id="9e720-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e720-105">Requirement</span></span> | <span data-ttu-id="9e720-106">Value</span><span class="sxs-lookup"><span data-stu-id="9e720-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e720-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="9e720-107">Query GUID</span></span>  | <span data-ttu-id="9e720-108">**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span><span class="sxs-lookup"><span data-stu-id="9e720-108">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>                                                                                                    |
| <span data-ttu-id="9e720-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="9e720-109">Input data</span></span>  | [<span data-ttu-id="9e720-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="9e720-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                                   |
| <span data-ttu-id="9e720-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="9e720-111">Return data</span></span> | [<span data-ttu-id="9e720-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="9e720-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="9e720-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e720-113">Remarks</span></span>

<span data-ttu-id="9e720-114">El único tipo de canal que admite esta consulta es el **\_ \_ software del controlador D3DAUTHENTICATEDCHANNEL**.</span><span class="sxs-lookup"><span data-stu-id="9e720-114">The only channel type that supports this query is **D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e720-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e720-115">Requirements</span></span>



| <span data-ttu-id="9e720-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e720-116">Requirement</span></span> | <span data-ttu-id="9e720-117">Value</span><span class="sxs-lookup"><span data-stu-id="9e720-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e720-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e720-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9e720-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e720-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9e720-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e720-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9e720-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e720-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9e720-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e720-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e720-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e720-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e720-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e720-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e720-125">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="9e720-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="9e720-126">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="9e720-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="9e720-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9e720-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




