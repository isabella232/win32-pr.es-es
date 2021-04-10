---
description: Devuelve el tipo de cifrado que se aplica antes de que el contenido sea accesible para la CPU o el bus.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275127"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a><span data-ttu-id="65e01-103">D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="65e01-103">D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="65e01-104">Devuelve el tipo de cifrado que se aplica antes de que el contenido sea accesible para la CPU o el bus.</span><span class="sxs-lookup"><span data-stu-id="65e01-104">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="65e01-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="65e01-105">Requirement</span></span> | <span data-ttu-id="65e01-106">Value</span><span class="sxs-lookup"><span data-stu-id="65e01-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e01-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="65e01-107">Query GUID</span></span>  | <span data-ttu-id="65e01-108">**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="65e01-108">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>                                                                                   |
| <span data-ttu-id="65e01-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="65e01-109">Input data</span></span>  | [<span data-ttu-id="65e01-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="65e01-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="65e01-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="65e01-111">Return data</span></span> | [<span data-ttu-id="65e01-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**</span><span class="sxs-lookup"><span data-stu-id="65e01-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="65e01-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65e01-113">Remarks</span></span>

<span data-ttu-id="65e01-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="65e01-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="65e01-115">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="65e01-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="65e01-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="65e01-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="65e01-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65e01-117">Requirements</span></span>



| <span data-ttu-id="65e01-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65e01-118">Requirement</span></span> | <span data-ttu-id="65e01-119">Value</span><span class="sxs-lookup"><span data-stu-id="65e01-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65e01-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65e01-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65e01-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="65e01-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65e01-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65e01-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65e01-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="65e01-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="65e01-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65e01-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65e01-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="65e01-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e01-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="65e01-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e01-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="65e01-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="65e01-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="65e01-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="65e01-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="65e01-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




