---
description: Opciones de ajuste de textura para las API de cálculo de IMT.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: Enumeración de marcas D3DXIMT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698244"
---
# <a name="d3dximt-flags-enumeration"></a><span data-ttu-id="84b13-103">Enumeración de marcas D3DXIMT</span><span class="sxs-lookup"><span data-stu-id="84b13-103">D3DXIMT FLAGS enumeration</span></span>

<span data-ttu-id="84b13-104">Opciones de ajuste de textura para las API de cálculo de IMT.</span><span class="sxs-lookup"><span data-stu-id="84b13-104">Texture wrapping options for IMT computation APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b13-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84b13-105">Syntax</span></span>


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a><span data-ttu-id="84b13-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="84b13-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="84b13-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="84b13-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="84b13-108">La textura se ajusta en la dirección U.</span><span class="sxs-lookup"><span data-stu-id="84b13-108">The texture wraps in the U direction.</span></span>

</dd> <dt>

<span data-ttu-id="84b13-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="84b13-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="84b13-110">La textura se ajusta en la dirección V.</span><span class="sxs-lookup"><span data-stu-id="84b13-110">The texture wraps in the V direction.</span></span>

</dd> <dt>

<span data-ttu-id="84b13-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT \_ encapsulado \_ UV**</span><span class="sxs-lookup"><span data-stu-id="84b13-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="84b13-112">La textura se ajusta tanto en la dirección de usuario como en la dirección de V.</span><span class="sxs-lookup"><span data-stu-id="84b13-112">The texture wraps in both the U and V direction.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84b13-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84b13-113">Requirements</span></span>



| <span data-ttu-id="84b13-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84b13-114">Requirement</span></span> | <span data-ttu-id="84b13-115">Value</span><span class="sxs-lookup"><span data-stu-id="84b13-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84b13-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84b13-116">Header</span></span><br/> | <dl> <span data-ttu-id="84b13-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="84b13-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b13-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="84b13-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b13-119">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="84b13-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="84b13-120">**D3DXComputeIMTFromSignal**</span><span class="sxs-lookup"><span data-stu-id="84b13-120">**D3DXComputeIMTFromSignal**</span></span>](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[<span data-ttu-id="84b13-121">**D3DXComputeIMTFromTexture**</span><span class="sxs-lookup"><span data-stu-id="84b13-121">**D3DXComputeIMTFromTexture**</span></span>](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[<span data-ttu-id="84b13-122">**D3DXComputeIMTFromPerTexelSignal**</span><span class="sxs-lookup"><span data-stu-id="84b13-122">**D3DXComputeIMTFromPerTexelSignal**</span></span>](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[<span data-ttu-id="84b13-123">**D3DXComputeIMTFromPerVertexSignal**</span><span class="sxs-lookup"><span data-stu-id="84b13-123">**D3DXComputeIMTFromPerVertexSignal**</span></span>](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




