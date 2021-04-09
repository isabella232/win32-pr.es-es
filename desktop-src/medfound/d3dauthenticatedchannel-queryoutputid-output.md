---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ OUTPUTID.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080321"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a><span data-ttu-id="14db0-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYROUTPUTID \_</span><span class="sxs-lookup"><span data-stu-id="14db0-103">D3DAUTHENTICATEDCHANNEL\_QUERYROUTPUTID\_OUTPUT structure</span></span>

<span data-ttu-id="14db0-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="14db0-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="14db0-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="14db0-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="14db0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14db0-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="14db0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="14db0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="14db0-108">**Resultado de la \_ consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="14db0-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="14db0-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="14db0-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="14db0-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="14db0-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="14db0-111">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14db0-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="14db0-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="14db0-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="14db0-113">Identificador de la sesión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="14db0-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="14db0-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="14db0-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="14db0-115">Índice del identificador de salida proporcionado en el miembro **OutputID** .</span><span class="sxs-lookup"><span data-stu-id="14db0-115">The index of the output ID given in the **OutputID** member.</span></span>

</dd> <dt>

<span data-ttu-id="14db0-116">**OutputID**</span><span class="sxs-lookup"><span data-stu-id="14db0-116">**OutputID**</span></span>
</dt> <dd>

<span data-ttu-id="14db0-117">Un ID. de salida que está asociado al dispositivo y a la sesión de cifrado especificados.</span><span class="sxs-lookup"><span data-stu-id="14db0-117">An output ID that is associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14db0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14db0-118">Requirements</span></span>



| <span data-ttu-id="14db0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14db0-119">Requirement</span></span> | <span data-ttu-id="14db0-120">Value</span><span class="sxs-lookup"><span data-stu-id="14db0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14db0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14db0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14db0-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="14db0-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="14db0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14db0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14db0-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="14db0-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="14db0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14db0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14db0-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="14db0-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14db0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="14db0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14db0-128">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="14db0-128">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="14db0-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="14db0-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




