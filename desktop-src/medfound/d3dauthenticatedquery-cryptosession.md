---
description: Devuelve los identificadores de la sesión criptográfica y el dispositivo Direct3D que están asociados a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) especificado.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275126"
---
# <a name="d3dauthenticatedquery_cryptosession"></a><span data-ttu-id="eede6-103">D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="eede6-103">D3DAUTHENTICATEDQUERY\_CRYPTOSESSION</span></span>

<span data-ttu-id="eede6-104">Devuelve los identificadores de la sesión criptográfica y el dispositivo Direct3D que están asociados a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) especificado.</span><span class="sxs-lookup"><span data-stu-id="eede6-104">Returns handles to the cryptographic session and Direct3D device that are associated with a specified DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>



| <span data-ttu-id="eede6-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="eede6-105">Requirement</span></span> | <span data-ttu-id="eede6-106">Value</span><span class="sxs-lookup"><span data-stu-id="eede6-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eede6-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="eede6-107">Query GUID</span></span>  | <span data-ttu-id="eede6-108">**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="eede6-108">**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**</span></span>                                                                         |
| <span data-ttu-id="eede6-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="eede6-109">Input data</span></span>  | [<span data-ttu-id="eede6-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="eede6-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                             |
| <span data-ttu-id="eede6-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="eede6-111">Return data</span></span> | [<span data-ttu-id="eede6-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_**</span><span class="sxs-lookup"><span data-stu-id="eede6-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT**</span></span>](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="eede6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eede6-113">Remarks</span></span>

<span data-ttu-id="eede6-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="eede6-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="eede6-115">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="eede6-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="eede6-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="eede6-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="eede6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eede6-117">Requirements</span></span>



| <span data-ttu-id="eede6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eede6-118">Requirement</span></span> | <span data-ttu-id="eede6-119">Value</span><span class="sxs-lookup"><span data-stu-id="eede6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eede6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eede6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eede6-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="eede6-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eede6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eede6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eede6-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eede6-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eede6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eede6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eede6-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="eede6-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eede6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="eede6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eede6-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="eede6-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="eede6-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="eede6-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="eede6-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="eede6-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




