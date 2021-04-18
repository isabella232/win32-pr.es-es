---
description: Devuelve el número de procesos que pueden abrir recursos compartidos con acceso restringido.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714922"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a><span data-ttu-id="8178a-103">D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span><span class="sxs-lookup"><span data-stu-id="8178a-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span></span>

<span data-ttu-id="8178a-104">Devuelve el número de procesos que pueden abrir recursos compartidos con acceso restringido.</span><span class="sxs-lookup"><span data-stu-id="8178a-104">Returns the number of processes that are allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="8178a-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="8178a-105">Requirement</span></span> | <span data-ttu-id="8178a-106">Value</span><span class="sxs-lookup"><span data-stu-id="8178a-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8178a-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="8178a-107">Query GUID</span></span>  | <span data-ttu-id="8178a-108">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span><span class="sxs-lookup"><span data-stu-id="8178a-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span></span>                                                                                                |
| <span data-ttu-id="8178a-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="8178a-109">Input data</span></span>  | [<span data-ttu-id="8178a-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="8178a-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                           |
| <span data-ttu-id="8178a-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="8178a-111">Return data</span></span> | [<span data-ttu-id="8178a-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="8178a-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="8178a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8178a-113">Remarks</span></span>

<span data-ttu-id="8178a-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="8178a-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="8178a-115">**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="8178a-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="8178a-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="8178a-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="8178a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8178a-117">Requirements</span></span>



| <span data-ttu-id="8178a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8178a-118">Requirement</span></span> | <span data-ttu-id="8178a-119">Value</span><span class="sxs-lookup"><span data-stu-id="8178a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8178a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8178a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8178a-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8178a-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8178a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8178a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8178a-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8178a-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8178a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8178a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8178a-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8178a-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8178a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8178a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8178a-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="8178a-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="8178a-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="8178a-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="8178a-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="8178a-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




