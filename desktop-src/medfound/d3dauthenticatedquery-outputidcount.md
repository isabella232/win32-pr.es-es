---
description: Devuelve el número de identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808119"
---
# <a name="d3dauthenticatedquery_outputidcount"></a><span data-ttu-id="6446d-103">D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="6446d-103">D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT</span></span>

<span data-ttu-id="6446d-104">Devuelve el número de identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.</span><span class="sxs-lookup"><span data-stu-id="6446d-104">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="6446d-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="6446d-105">Requirement</span></span> | <span data-ttu-id="6446d-106">Value</span><span class="sxs-lookup"><span data-stu-id="6446d-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6446d-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="6446d-107">Query GUID</span></span>  | <span data-ttu-id="6446d-108">**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="6446d-108">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>                                                                         |
| <span data-ttu-id="6446d-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="6446d-109">Input data</span></span>  | [<span data-ttu-id="6446d-110">**\_Entrada QUERYOUTPUTIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="6446d-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| <span data-ttu-id="6446d-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="6446d-111">Return data</span></span> | [<span data-ttu-id="6446d-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="6446d-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="6446d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6446d-113">Remarks</span></span>

<span data-ttu-id="6446d-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="6446d-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="6446d-115">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="6446d-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="6446d-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="6446d-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="6446d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6446d-117">Requirements</span></span>



| <span data-ttu-id="6446d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6446d-118">Requirement</span></span> | <span data-ttu-id="6446d-119">Value</span><span class="sxs-lookup"><span data-stu-id="6446d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6446d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6446d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6446d-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6446d-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6446d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6446d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6446d-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6446d-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6446d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6446d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6446d-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6446d-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6446d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6446d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6446d-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="6446d-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="6446d-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="6446d-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="6446d-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="6446d-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




