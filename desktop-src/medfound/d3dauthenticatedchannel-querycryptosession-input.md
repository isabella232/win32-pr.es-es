---
description: Contiene datos de entrada para una \_ consulta de D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360104"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a><span data-ttu-id="7f4a8-103">D3DAUTHENTICATEDCHANNEL \_ \_ estructura de entrada QUERYCRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="7f4a8-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_INPUT structure</span></span>

<span data-ttu-id="7f4a8-104">Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="7f4a8-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="7f4a8-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="7f4a8-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4a8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f4a8-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a><span data-ttu-id="7f4a8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f4a8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f4a8-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="7f4a8-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="7f4a8-109">Una estructura de [**\_ \_ entrada de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contiene el GUID para la consulta y otros datos.</span><span class="sxs-lookup"><span data-stu-id="7f4a8-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="7f4a8-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="7f4a8-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="7f4a8-111">Identificador de un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="7f4a8-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f4a8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f4a8-112">Requirements</span></span>



| <span data-ttu-id="7f4a8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f4a8-113">Requirement</span></span> | <span data-ttu-id="7f4a8-114">Value</span><span class="sxs-lookup"><span data-stu-id="7f4a8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4a8-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f4a8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4a8-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f4a8-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7f4a8-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f4a8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4a8-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f4a8-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f4a8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f4a8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4a8-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f4a8-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4a8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f4a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4a8-122">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7f4a8-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="7f4a8-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="7f4a8-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




