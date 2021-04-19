---
description: Devuelve un identificador para el dispositivo que está asociado a este canal autenticado.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696147"
---
# <a name="d3dauthenticatedquery_devicehandle"></a><span data-ttu-id="5ee19-103">D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE</span><span class="sxs-lookup"><span data-stu-id="5ee19-103">D3DAUTHENTICATEDQUERY\_DEVICEHANDLE</span></span>

<span data-ttu-id="5ee19-104">Devuelve un identificador para el dispositivo que está asociado a este canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="5ee19-104">Returns a handle to the device that is associated with this authenticated channel.</span></span> <span data-ttu-id="5ee19-105">Puede usar este identificador para comprobar si dos canales autenticados se están comunicando con el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5ee19-105">You can use this handle to verify whether two authenticated channels are communicating with the same device.</span></span>



| <span data-ttu-id="5ee19-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee19-106">Requirement</span></span> | <span data-ttu-id="5ee19-107">Value</span><span class="sxs-lookup"><span data-stu-id="5ee19-107">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee19-108">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="5ee19-108">Query GUID</span></span>  | <span data-ttu-id="5ee19-109">**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5ee19-109">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>                                                                        |
| <span data-ttu-id="5ee19-110">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="5ee19-110">Input data</span></span>  | [<span data-ttu-id="5ee19-111">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="5ee19-111">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                           |
| <span data-ttu-id="5ee19-112">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="5ee19-112">Return data</span></span> | [<span data-ttu-id="5ee19-113">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_**</span><span class="sxs-lookup"><span data-stu-id="5ee19-113">**D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="5ee19-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ee19-114">Remarks</span></span>

<span data-ttu-id="5ee19-115">Esta consulta es válida para todos los tipos de canales.</span><span class="sxs-lookup"><span data-stu-id="5ee19-115">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee19-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ee19-116">Requirements</span></span>



| <span data-ttu-id="5ee19-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee19-117">Requirement</span></span> | <span data-ttu-id="5ee19-118">Value</span><span class="sxs-lookup"><span data-stu-id="5ee19-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee19-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ee19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ee19-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ee19-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5ee19-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ee19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ee19-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ee19-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5ee19-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ee19-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ee19-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee19-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ee19-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ee19-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee19-126">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="5ee19-126">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="5ee19-127">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="5ee19-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="5ee19-128">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="5ee19-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




