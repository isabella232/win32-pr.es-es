---
description: Devuelve el nivel de protección actual del dispositivo.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275124"
---
# <a name="d3dauthenticatedquery_protection"></a><span data-ttu-id="3b5a4-103">Protección de D3DAUTHENTICATEDQUERY \_</span><span class="sxs-lookup"><span data-stu-id="3b5a4-103">D3DAUTHENTICATEDQUERY\_PROTECTION</span></span>

<span data-ttu-id="3b5a4-104">Devuelve el nivel de protección actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5a4-104">Returns the current protection level for the device.</span></span>



| <span data-ttu-id="3b5a4-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5a4-105">Requirement</span></span> | <span data-ttu-id="3b5a4-106">Value</span><span class="sxs-lookup"><span data-stu-id="3b5a4-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5a4-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="3b5a4-107">Query GUID</span></span>  | <span data-ttu-id="3b5a4-108">**Protección de D3DAUTHENTICATEDQUERY \_**</span><span class="sxs-lookup"><span data-stu-id="3b5a4-108">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>                                                                      |
| <span data-ttu-id="3b5a4-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="3b5a4-109">Input data</span></span>  | [<span data-ttu-id="3b5a4-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="3b5a4-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                       |
| <span data-ttu-id="3b5a4-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="3b5a4-111">Return data</span></span> | [<span data-ttu-id="3b5a4-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_**</span><span class="sxs-lookup"><span data-stu-id="3b5a4-112">**D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="3b5a4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b5a4-113">Remarks</span></span>

<span data-ttu-id="3b5a4-114">Esta consulta es válida para todos los tipos de canales.</span><span class="sxs-lookup"><span data-stu-id="3b5a4-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5a4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b5a4-115">Requirements</span></span>



| <span data-ttu-id="3b5a4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5a4-116">Requirement</span></span> | <span data-ttu-id="3b5a4-117">Value</span><span class="sxs-lookup"><span data-stu-id="3b5a4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5a4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5a4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5a4-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b5a4-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3b5a4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5a4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5a4-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b5a4-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b5a4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b5a4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b5a4-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b5a4-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b5a4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b5a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b5a4-125">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="3b5a4-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="3b5a4-126">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="3b5a4-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="3b5a4-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="3b5a4-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




