---
description: Devuelve el tipo de canal autenticado.
ms.assetid: eec4b117-a9f2-479d-99d7-e5d4053cf6b4
title: D3DAUTHENTICATEDQUERY_CHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 58ac84a0caca5a5709c74adbca567633e12daa10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714927"
---
# <a name="d3dauthenticatedquery_channeltype"></a><span data-ttu-id="52f68-103">D3DAUTHENTICATEDQUERY \_ CHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="52f68-103">D3DAUTHENTICATEDQUERY\_CHANNELTYPE</span></span>

<span data-ttu-id="52f68-104">Devuelve el tipo de canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="52f68-104">Returns the type of authenticated channel.</span></span>



| <span data-ttu-id="52f68-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f68-105">Requirement</span></span> | <span data-ttu-id="52f68-106">Value</span><span class="sxs-lookup"><span data-stu-id="52f68-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f68-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="52f68-107">Query GUID</span></span>  | <span data-ttu-id="52f68-108">**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**</span><span class="sxs-lookup"><span data-stu-id="52f68-108">**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**</span></span>                                                                       |
| <span data-ttu-id="52f68-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="52f68-109">Input data</span></span>  | [<span data-ttu-id="52f68-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="52f68-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="52f68-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="52f68-111">Return data</span></span> | [<span data-ttu-id="52f68-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="52f68-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querychanneltype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="52f68-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52f68-113">Remarks</span></span>

<span data-ttu-id="52f68-114">Esta consulta es válida para todos los tipos de canales.</span><span class="sxs-lookup"><span data-stu-id="52f68-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f68-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f68-115">Requirements</span></span>



| <span data-ttu-id="52f68-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f68-116">Requirement</span></span> | <span data-ttu-id="52f68-117">Value</span><span class="sxs-lookup"><span data-stu-id="52f68-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52f68-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52f68-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52f68-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="52f68-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="52f68-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52f68-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52f68-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="52f68-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52f68-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52f68-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f68-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f68-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f68-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="52f68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f68-125">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="52f68-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="52f68-126">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="52f68-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="52f68-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="52f68-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




