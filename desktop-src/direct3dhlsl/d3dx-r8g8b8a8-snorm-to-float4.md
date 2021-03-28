---
title: D3DX_R8G8B8A8_SNORM_to_FLOAT4 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 SNORM con formato DXGI en un XMFLOAT4.
ms.assetid: 2f2b9d5e-f4d0-470a-a4bb-b333d57f03e7
keywords:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a4153fa30f2792008ccc45bc3e16f5d404f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986892"
---
# <a name="d3dx_r8g8b8a8_snorm_to_float4-function"></a><span data-ttu-id="1c86e-104">D3DX \_ R8G8B8A8 \_ SNORM \_ a la \_ función FLOAT4</span><span class="sxs-lookup"><span data-stu-id="1c86e-104">D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="1c86e-105">Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 SNORM con formato DXGI en un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="1c86e-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c86e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c86e-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="1c86e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c86e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c86e-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="1c86e-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="1c86e-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="1c86e-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c86e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c86e-110">Return value</span></span>

<span data-ttu-id="1c86e-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="1c86e-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c86e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c86e-112">Requirements</span></span>



| <span data-ttu-id="1c86e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c86e-113">Requirement</span></span> | <span data-ttu-id="1c86e-114">Value</span><span class="sxs-lookup"><span data-stu-id="1c86e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c86e-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c86e-115">Header</span></span><br/> | <dl> <span data-ttu-id="1c86e-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="1c86e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c86e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c86e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c86e-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="1c86e-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="1c86e-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="1c86e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





