---
description: Contiene datos de entrada para una \_ consulta de D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153653"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a><span data-ttu-id="23f10-103">D3DAUTHENTICATEDCHANNEL \_ \_ estructura de entrada QUERYOUTPUTIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="23f10-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT structure</span></span>

<span data-ttu-id="23f10-104">Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="23f10-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="23f10-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="23f10-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="23f10-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23f10-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a><span data-ttu-id="23f10-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="23f10-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="23f10-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="23f10-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="23f10-109">Una estructura de [**\_ \_ entrada de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contiene el GUID para la consulta y otros datos.</span><span class="sxs-lookup"><span data-stu-id="23f10-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="23f10-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="23f10-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="23f10-111">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23f10-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="23f10-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="23f10-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="23f10-113">Identificador de la sesión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="23f10-113">A handle to the cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23f10-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23f10-114">Requirements</span></span>



| <span data-ttu-id="23f10-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f10-115">Requirement</span></span> | <span data-ttu-id="23f10-116">Value</span><span class="sxs-lookup"><span data-stu-id="23f10-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23f10-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23f10-117">Minimum supported client</span></span><br/> | <span data-ttu-id="23f10-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="23f10-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="23f10-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23f10-119">Minimum supported server</span></span><br/> | <span data-ttu-id="23f10-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="23f10-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="23f10-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23f10-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f10-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="23f10-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f10-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="23f10-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f10-124">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="23f10-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="23f10-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="23f10-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




