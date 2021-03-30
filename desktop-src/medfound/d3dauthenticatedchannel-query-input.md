---
description: 'Contiene datos de entrada para el método IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: D3DAUTHENTICATEDCHANNEL_QUERY_INPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275132"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a><span data-ttu-id="6eb8d-103">D3DAUTHENTICATEDCHANNEL \_ estructura de entrada de consulta \_</span><span class="sxs-lookup"><span data-stu-id="6eb8d-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT structure</span></span>

<span data-ttu-id="6eb8d-104">Contiene datos de entrada para el método [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="6eb8d-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6eb8d-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a><span data-ttu-id="6eb8d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6eb8d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6eb8d-107">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="6eb8d-107">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="6eb8d-108">GUID que especifica la consulta.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-108">A GUID that specifies the query.</span></span> <span data-ttu-id="6eb8d-109">Para obtener una lista de valores, vea [consultas de Content Protection](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="6eb8d-109">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="6eb8d-110">**ASA**</span><span class="sxs-lookup"><span data-stu-id="6eb8d-110">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="6eb8d-111">Identificador del canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-111">A handle to the authenticated channel.</span></span> <span data-ttu-id="6eb8d-112">Para obtener el identificador, llame a [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="6eb8d-112">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="6eb8d-113">**UINT**</span><span class="sxs-lookup"><span data-stu-id="6eb8d-113">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="6eb8d-114">El número de secuencia de la consulta.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-114">The query sequence number.</span></span> <span data-ttu-id="6eb8d-115">Al inicio de la sesión, genere un número aleatorio de 32 bits criptográficamente seguro para usarlo como el número de secuencia inicial.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-115">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="6eb8d-116">Para cada consulta, incremente el número de secuencia en 1.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-116">For each query, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6eb8d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eb8d-117">Requirements</span></span>



| <span data-ttu-id="6eb8d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb8d-118">Requirement</span></span> | <span data-ttu-id="6eb8d-119">Value</span><span class="sxs-lookup"><span data-stu-id="6eb8d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb8d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eb8d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb8d-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6eb8d-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6eb8d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eb8d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb8d-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6eb8d-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6eb8d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6eb8d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eb8d-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb8d-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb8d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6eb8d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb8d-127">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="6eb8d-127">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="6eb8d-128">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="6eb8d-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




