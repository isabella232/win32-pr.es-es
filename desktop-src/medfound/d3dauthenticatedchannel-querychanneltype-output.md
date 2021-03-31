---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ CHANNELTYPE.
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3120669da69f13359f49d8b8c38ed7d3e211a8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423559"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a><span data-ttu-id="4eda9-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_</span><span class="sxs-lookup"><span data-stu-id="4eda9-103">D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="4eda9-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) .</span><span class="sxs-lookup"><span data-stu-id="4eda9-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) query.</span></span>

<span data-ttu-id="4eda9-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="4eda9-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="4eda9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4eda9-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="4eda9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4eda9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4eda9-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="4eda9-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="4eda9-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="4eda9-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4eda9-110">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="4eda9-110">**ChannelType**</span></span>
</dt> <dd>

<span data-ttu-id="4eda9-111">Valor [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) que especifica el tipo de canal.</span><span class="sxs-lookup"><span data-stu-id="4eda9-111">A [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) value that specifies the channel type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4eda9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eda9-112">Requirements</span></span>



| <span data-ttu-id="4eda9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eda9-113">Requirement</span></span> | <span data-ttu-id="4eda9-114">Value</span><span class="sxs-lookup"><span data-stu-id="4eda9-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eda9-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eda9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4eda9-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4eda9-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4eda9-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eda9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4eda9-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4eda9-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4eda9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4eda9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eda9-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eda9-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eda9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4eda9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eda9-122">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4eda9-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4eda9-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="4eda9-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




