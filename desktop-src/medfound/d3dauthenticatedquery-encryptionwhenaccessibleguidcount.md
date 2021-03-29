---
description: Devuelve el número de tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808125"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a><span data-ttu-id="b7d87-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="b7d87-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span></span>

<span data-ttu-id="b7d87-104">Devuelve el número de tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.</span><span class="sxs-lookup"><span data-stu-id="b7d87-104">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="b7d87-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d87-105">Requirement</span></span> | <span data-ttu-id="b7d87-106">Value</span><span class="sxs-lookup"><span data-stu-id="b7d87-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d87-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="b7d87-107">Query GUID</span></span>  | <span data-ttu-id="b7d87-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="b7d87-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>                                                                                 |
| <span data-ttu-id="b7d87-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="b7d87-109">Input data</span></span>  | [<span data-ttu-id="b7d87-110">**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b7d87-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="b7d87-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="b7d87-111">Return data</span></span> | [<span data-ttu-id="b7d87-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="b7d87-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="b7d87-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7d87-113">Remarks</span></span>

<span data-ttu-id="b7d87-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="b7d87-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="b7d87-115">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b7d87-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="b7d87-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b7d87-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d87-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7d87-117">Requirements</span></span>



| <span data-ttu-id="b7d87-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d87-118">Requirement</span></span> | <span data-ttu-id="b7d87-119">Value</span><span class="sxs-lookup"><span data-stu-id="b7d87-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d87-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7d87-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d87-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7d87-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b7d87-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7d87-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d87-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7d87-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b7d87-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7d87-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d87-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d87-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d87-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7d87-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d87-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="b7d87-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="b7d87-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="b7d87-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="b7d87-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="b7d87-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




