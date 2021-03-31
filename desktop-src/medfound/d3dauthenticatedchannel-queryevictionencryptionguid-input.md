---
description: Contiene datos de entrada para una \_ consulta de D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: 0e24e393-3f63-4c6f-aca1-f73ced3490ba
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1c4500d27577883f46d00580dcc7e306b4008cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423555"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_input-structure"></a><span data-ttu-id="68046-103">D3DAUTHENTICATEDCHANNEL \_ \_ estructura de entrada QUERYEVICTIONENCRYPTIONGUID</span><span class="sxs-lookup"><span data-stu-id="68046-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT structure</span></span>

<span data-ttu-id="68046-104">Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="68046-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="68046-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="68046-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="68046-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68046-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                EncryptionGuidIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT;
```



## <a name="members"></a><span data-ttu-id="68046-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="68046-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="68046-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="68046-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="68046-109">Una estructura de [**\_ \_ entrada de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contiene el GUID para la consulta y otros datos.</span><span class="sxs-lookup"><span data-stu-id="68046-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="68046-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="68046-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="68046-111">Índice del GUID de cifrado.</span><span class="sxs-lookup"><span data-stu-id="68046-111">The index of the encryption GUID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68046-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68046-112">Requirements</span></span>



| <span data-ttu-id="68046-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="68046-113">Requirement</span></span> | <span data-ttu-id="68046-114">Value</span><span class="sxs-lookup"><span data-stu-id="68046-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68046-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68046-115">Minimum supported client</span></span><br/> | <span data-ttu-id="68046-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="68046-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="68046-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68046-117">Minimum supported server</span></span><br/> | <span data-ttu-id="68046-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="68046-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="68046-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68046-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="68046-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="68046-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68046-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="68046-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68046-122">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="68046-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="68046-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="68046-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




