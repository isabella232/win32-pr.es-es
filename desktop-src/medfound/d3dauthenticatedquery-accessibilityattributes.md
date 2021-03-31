---
description: Devuelve el tipo de bus de e/s que se usa para enviar datos a la GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423551"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a><span data-ttu-id="826e0-103">D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="826e0-103">D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES</span></span>

<span data-ttu-id="826e0-104">Devuelve el tipo de bus de e/s que se usa para enviar datos a la GPU.</span><span class="sxs-lookup"><span data-stu-id="826e0-104">Returns the type of I/O bus used to send data to the GPU.</span></span>



| <span data-ttu-id="826e0-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="826e0-105">Requirement</span></span> | <span data-ttu-id="826e0-106">Value</span><span class="sxs-lookup"><span data-stu-id="826e0-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="826e0-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="826e0-107">Query GUID</span></span>  | <span data-ttu-id="826e0-108">**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="826e0-108">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>                                                           |
| <span data-ttu-id="826e0-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="826e0-109">Input data</span></span>  | [<span data-ttu-id="826e0-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="826e0-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="826e0-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="826e0-111">Return data</span></span> | [<span data-ttu-id="826e0-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="826e0-112">**D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="826e0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="826e0-113">Remarks</span></span>

<span data-ttu-id="826e0-114">Esta consulta también devuelve información sobre la accesibilidad del contenido cuando se coloca en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="826e0-114">This query also returns information about how accessible the content is when put into video memory.</span></span>

<span data-ttu-id="826e0-115">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="826e0-115">The following channel types support this query:</span></span>

-   <span data-ttu-id="826e0-116">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="826e0-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="826e0-117">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="826e0-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="826e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="826e0-118">Requirements</span></span>



| <span data-ttu-id="826e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="826e0-119">Requirement</span></span> | <span data-ttu-id="826e0-120">Value</span><span class="sxs-lookup"><span data-stu-id="826e0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="826e0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="826e0-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="826e0-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="826e0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="826e0-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="826e0-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="826e0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="826e0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="826e0-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="826e0-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826e0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="826e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826e0-128">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="826e0-128">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="826e0-129">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="826e0-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="826e0-130">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="826e0-130">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




