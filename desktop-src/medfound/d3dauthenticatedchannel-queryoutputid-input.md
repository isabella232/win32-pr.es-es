---
description: Contiene datos de entrada para una \_ consulta de D3DAUTHENTICATEDQUERY OUTPUTID.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720295"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a><span data-ttu-id="18001-103">D3DAUTHENTICATEDCHANNEL \_ \_ estructura de entrada QUERYOUTPUTID</span><span class="sxs-lookup"><span data-stu-id="18001-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT structure</span></span>

<span data-ttu-id="18001-104">Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="18001-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="18001-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="18001-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="18001-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18001-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a><span data-ttu-id="18001-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="18001-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="18001-108">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="18001-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="18001-109">Una estructura de [**\_ \_ entrada de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contiene el GUID para la consulta y otros datos.</span><span class="sxs-lookup"><span data-stu-id="18001-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="18001-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="18001-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="18001-111">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18001-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="18001-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="18001-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="18001-113">Identificador de la sesión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="18001-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="18001-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="18001-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="18001-115">Índice del identificador de salida.</span><span class="sxs-lookup"><span data-stu-id="18001-115">The index of the output ID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18001-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18001-116">Requirements</span></span>



| <span data-ttu-id="18001-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="18001-117">Requirement</span></span> | <span data-ttu-id="18001-118">Value</span><span class="sxs-lookup"><span data-stu-id="18001-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18001-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18001-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18001-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="18001-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="18001-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18001-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18001-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="18001-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="18001-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18001-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="18001-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="18001-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18001-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="18001-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18001-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="18001-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="18001-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="18001-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




