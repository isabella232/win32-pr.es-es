---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 UNORM con formato DXGI en un XMFLOAT4. | D3DX_FLOAT4_to_R8G8B8A8_UNORM función)
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821455"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a><span data-ttu-id="fa023-105">D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ función UNORM</span><span class="sxs-lookup"><span data-stu-id="fa023-105">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM function</span></span>

<span data-ttu-id="fa023-106">Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 UNORM con formato DXGI en un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="fa023-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa023-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa023-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="fa023-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa023-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa023-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="fa023-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="fa023-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="fa023-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa023-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa023-111">Return value</span></span>

<span data-ttu-id="fa023-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="fa023-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa023-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa023-113">Requirements</span></span>



| <span data-ttu-id="fa023-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa023-114">Requirement</span></span> | <span data-ttu-id="fa023-115">Value</span><span class="sxs-lookup"><span data-stu-id="fa023-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa023-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa023-116">Header</span></span><br/> | <dl> <span data-ttu-id="fa023-117"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="fa023-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa023-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa023-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa023-119">Funciones</span><span class="sxs-lookup"><span data-stu-id="fa023-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="fa023-120">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="fa023-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





