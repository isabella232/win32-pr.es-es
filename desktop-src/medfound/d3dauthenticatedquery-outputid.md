---
description: Devuelve uno de los identificadores de salida que está asociado a una sesión criptográfica y un dispositivo Direct3D especificados.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808120"
---
# <a name="d3dauthenticatedquery_outputid"></a><span data-ttu-id="a228b-103">D3DAUTHENTICATEDQUERY \_ OUTPUTID</span><span class="sxs-lookup"><span data-stu-id="a228b-103">D3DAUTHENTICATEDQUERY\_OUTPUTID</span></span>

<span data-ttu-id="a228b-104">Devuelve uno de los identificadores de salida que está asociado a una sesión criptográfica y un dispositivo Direct3D especificados.</span><span class="sxs-lookup"><span data-stu-id="a228b-104">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="a228b-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="a228b-105">Requirement</span></span> | <span data-ttu-id="a228b-106">Value</span><span class="sxs-lookup"><span data-stu-id="a228b-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a228b-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="a228b-107">Query GUID</span></span>  | <span data-ttu-id="a228b-108">**D3DAUTHENTICATEDQUERY \_ OUTPUTID**</span><span class="sxs-lookup"><span data-stu-id="a228b-108">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>                                                                    |
| <span data-ttu-id="a228b-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="a228b-109">Input data</span></span>  | [<span data-ttu-id="a228b-110">**\_Entrada QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="a228b-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-input.md)   |
| <span data-ttu-id="a228b-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="a228b-111">Return data</span></span> | [<span data-ttu-id="a228b-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_**</span><span class="sxs-lookup"><span data-stu-id="a228b-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="a228b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a228b-113">Remarks</span></span>

<span data-ttu-id="a228b-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="a228b-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="a228b-115">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="a228b-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="a228b-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="a228b-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="a228b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a228b-117">Requirements</span></span>



| <span data-ttu-id="a228b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a228b-118">Requirement</span></span> | <span data-ttu-id="a228b-119">Value</span><span class="sxs-lookup"><span data-stu-id="a228b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a228b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a228b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a228b-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a228b-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a228b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a228b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a228b-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a228b-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a228b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a228b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a228b-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a228b-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a228b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a228b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a228b-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="a228b-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="a228b-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="a228b-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="a228b-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a228b-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




