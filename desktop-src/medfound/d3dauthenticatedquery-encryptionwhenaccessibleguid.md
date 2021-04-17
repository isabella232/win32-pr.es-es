---
description: Devuelve uno de los tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696146"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a><span data-ttu-id="6d30a-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID</span><span class="sxs-lookup"><span data-stu-id="6d30a-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID</span></span>

<span data-ttu-id="6d30a-104">Devuelve uno de los tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.</span><span class="sxs-lookup"><span data-stu-id="6d30a-104">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="6d30a-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d30a-105">Requirement</span></span> | <span data-ttu-id="6d30a-106">Value</span><span class="sxs-lookup"><span data-stu-id="6d30a-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d30a-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="6d30a-107">Query GUID</span></span>  | <span data-ttu-id="6d30a-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**</span><span class="sxs-lookup"><span data-stu-id="6d30a-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>                                                                            |
| <span data-ttu-id="6d30a-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="6d30a-109">Input data</span></span>  | [<span data-ttu-id="6d30a-110">**\_Entrada QUERYEVICTIONENCRYPTIONGUID \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="6d30a-110">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| <span data-ttu-id="6d30a-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="6d30a-111">Return data</span></span> | [<span data-ttu-id="6d30a-112">**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_**</span><span class="sxs-lookup"><span data-stu-id="6d30a-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="6d30a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d30a-113">Remarks</span></span>

<span data-ttu-id="6d30a-114">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="6d30a-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="6d30a-115">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="6d30a-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="6d30a-116">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="6d30a-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="6d30a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d30a-117">Requirements</span></span>



| <span data-ttu-id="6d30a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d30a-118">Requirement</span></span> | <span data-ttu-id="6d30a-119">Value</span><span class="sxs-lookup"><span data-stu-id="6d30a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d30a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d30a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6d30a-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d30a-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6d30a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d30a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6d30a-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d30a-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6d30a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d30a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d30a-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d30a-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d30a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d30a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d30a-127">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="6d30a-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="6d30a-128">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="6d30a-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="6d30a-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="6d30a-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




