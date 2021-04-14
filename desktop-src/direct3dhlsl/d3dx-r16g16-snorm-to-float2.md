---
title: D3DX_R16G16_SNORM_to_FLOAT2 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de R16G16 SNORM con formato DXGI en un XMFLOAT2.
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- D3DX_R16G16_SNORM_to_FLOAT2 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3d45f486d2c44e2cbe319e920ab4bdec764fd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998413"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a><span data-ttu-id="c2e3c-104">D3DX \_ R16G16 \_ SNORM \_ a la \_ función FLOAT2</span><span class="sxs-lookup"><span data-stu-id="c2e3c-104">D3DX\_R16G16\_SNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="c2e3c-105">Desempaqueta los \_ datos del \_ \_ sombreador de R16G16 SNORM con formato DXGI en un XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-105">Unpacks DXGI\_FORMAT\_R16G16\_SNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e3c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2e3c-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c2e3c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2e3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e3c-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="c2e3c-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c2e3c-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e3c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2e3c-110">Return value</span></span>

<span data-ttu-id="c2e3c-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e3c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e3c-112">Requirements</span></span>



| <span data-ttu-id="c2e3c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e3c-113">Requirement</span></span> | <span data-ttu-id="c2e3c-114">Value</span><span class="sxs-lookup"><span data-stu-id="c2e3c-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e3c-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2e3c-115">Header</span></span><br/> | <dl> <span data-ttu-id="c2e3c-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="c2e3c-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e3c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2e3c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e3c-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="c2e3c-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e3c-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="c2e3c-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





