---
description: Contiene un vector de inicialización (IV) para el cifrado de cifrado del modo Estándar de cifrado avanzado CTR (AES-CTR) de 128 bits.
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: D3DAES_CTR_IV estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360107"
---
# <a name="d3daes_ctr_iv-structure"></a><span data-ttu-id="1fd04-103">\_Estructura D3DAES CTR \_ IV</span><span class="sxs-lookup"><span data-stu-id="1fd04-103">D3DAES\_CTR\_IV structure</span></span>

<span data-ttu-id="1fd04-104">Contiene un vector de inicialización (IV) para el cifrado de cifrado del modo Estándar de cifrado avanzado CTR (AES-CTR) de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="1fd04-104">Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd04-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fd04-105">Syntax</span></span>


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a><span data-ttu-id="1fd04-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1fd04-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1fd04-107">**IV**</span><span class="sxs-lookup"><span data-stu-id="1fd04-107">**IV**</span></span>
</dt> <dd>

<span data-ttu-id="1fd04-108">El IV, en formato Big-Endian.</span><span class="sxs-lookup"><span data-stu-id="1fd04-108">The IV, in big-endian format.</span></span>

</dd> <dt>

<span data-ttu-id="1fd04-109">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="1fd04-109">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="1fd04-110">Recuento de bloques, en formato Big-Endian.</span><span class="sxs-lookup"><span data-stu-id="1fd04-110">The block count, in big-endian format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fd04-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fd04-111">Remarks</span></span>

<span data-ttu-id="1fd04-112">La estructura **D3DAES \_ CTR \_ IV** y la estructura [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="1fd04-112">The **D3DAES\_CTR\_IV** structure and the [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) structure are equivalent.</span></span>

<span data-ttu-id="1fd04-113">Para obtener más información, consulte [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span><span class="sxs-lookup"><span data-stu-id="1fd04-113">For details, see [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd04-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fd04-114">Requirements</span></span>



| <span data-ttu-id="1fd04-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fd04-115">Requirement</span></span> | <span data-ttu-id="1fd04-116">Value</span><span class="sxs-lookup"><span data-stu-id="1fd04-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd04-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fd04-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd04-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fd04-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1fd04-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fd04-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd04-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fd04-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1fd04-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fd04-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fd04-122"><dt>D3d9types. h (incluye d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd04-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd04-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fd04-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd04-124">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1fd04-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




