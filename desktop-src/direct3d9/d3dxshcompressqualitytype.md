---
description: Valor de compresión armónico (SH).
ms.assetid: 214d6efb-419d-4eea-8360-322885c26bc3
title: Enumeración D3DXSHCOMPRESSQUALITYTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHCOMPRESSQUALITYTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d61c70317505442ca4911a13dac8566f9bd7c6fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280301"
---
# <a name="d3dxshcompressqualitytype-enumeration"></a><span data-ttu-id="3b9c9-103">Enumeración D3DXSHCOMPRESSQUALITYTYPE</span><span class="sxs-lookup"><span data-stu-id="3b9c9-103">D3DXSHCOMPRESSQUALITYTYPE enumeration</span></span>

<span data-ttu-id="3b9c9-104">Valor de compresión armónico (SH).</span><span class="sxs-lookup"><span data-stu-id="3b9c9-104">Spherical harmonic (SH) compression setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b9c9-105">Syntax</span></span>


```C++
typedef enum D3DXSHCOMPRESSQUALITYTYPE { 
  D3DXSHCQUAL_FASTLOWQUALITY   = 1,
  D3DXSHCQUAL_SLOWHIGHQUALITY  = 2,
  D3DXSHCQUAL_FORCE_DWORD      = 0x7fffffff
} D3DXSHCOMPRESSQUALITYTYPE, *LPD3DXSHCOMPRESSQUALITYTYPE;
```



## <a name="constants"></a><span data-ttu-id="3b9c9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3b9c9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3b9c9-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL \_ FASTLOWQUALITY**</span><span class="sxs-lookup"><span data-stu-id="3b9c9-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL\_FASTLOWQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="3b9c9-108">La compresión de datos es de baja calidad, pero es rápida de comprimir.</span><span class="sxs-lookup"><span data-stu-id="3b9c9-108">The data compression is low quality, but is fast to compress.</span></span>

</dd> <dt>

<span data-ttu-id="3b9c9-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL \_ SLOWHIGHQUALITY**</span><span class="sxs-lookup"><span data-stu-id="3b9c9-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL\_SLOWHIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="3b9c9-110">La compresión de datos es de alta calidad, pero es lenta de comprimir.</span><span class="sxs-lookup"><span data-stu-id="3b9c9-110">The data compression is high quality, but is slow to compress.</span></span>

</dd> <dt>

<span data-ttu-id="3b9c9-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b9c9-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3b9c9-112">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="3b9c9-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3b9c9-113">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3b9c9-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3b9c9-114">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3b9c9-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b9c9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b9c9-115">Requirements</span></span>



| <span data-ttu-id="3b9c9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b9c9-116">Requirement</span></span> | <span data-ttu-id="3b9c9-117">Value</span><span class="sxs-lookup"><span data-stu-id="3b9c9-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9c9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b9c9-118">Header</span></span><br/> | <dl> <span data-ttu-id="3b9c9-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9c9-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9c9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b9c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9c9-121">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="3b9c9-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




