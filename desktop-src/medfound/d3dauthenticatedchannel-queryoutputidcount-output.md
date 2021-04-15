---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 86a840de2b36b7089b31d15e8375c17a0610b77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496822"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a><span data-ttu-id="10aba-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="10aba-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="10aba-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="10aba-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="10aba-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="10aba-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="10aba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10aba-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="10aba-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="10aba-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="10aba-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="10aba-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="10aba-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="10aba-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="10aba-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="10aba-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="10aba-111">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10aba-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="10aba-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="10aba-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="10aba-113">Identificador de la sesión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="10aba-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="10aba-114">**NumOutputIDs**</span><span class="sxs-lookup"><span data-stu-id="10aba-114">**NumOutputIDs**</span></span>
</dt> <dd>

<span data-ttu-id="10aba-115">El número de identificadores de salida asociados al dispositivo y a la sesión de cifrado especificados.</span><span class="sxs-lookup"><span data-stu-id="10aba-115">The number of output IDs associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10aba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10aba-116">Requirements</span></span>



| <span data-ttu-id="10aba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="10aba-117">Requirement</span></span> | <span data-ttu-id="10aba-118">Value</span><span class="sxs-lookup"><span data-stu-id="10aba-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10aba-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10aba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="10aba-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="10aba-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="10aba-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10aba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="10aba-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="10aba-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="10aba-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10aba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="10aba-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="10aba-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10aba-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="10aba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10aba-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="10aba-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="10aba-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="10aba-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




