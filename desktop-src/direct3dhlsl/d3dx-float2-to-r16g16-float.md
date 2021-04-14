---
title: D3DX_FLOAT2_to_R16G16_FLOAT función)
description: Vuelve a empaquetar el XMFLOAT2 determinado en un formato de DXGI \_ \_ R16G16 \_ float.
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- D3DX_FLOAT2_to_R16G16_FLOAT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849eb4dde5ab11e98675a1581519aabbeeb1e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998299"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a><span data-ttu-id="8948a-104">D3DX \_ FLOAT2 \_ a \_ R16G16 \_ función Float</span><span class="sxs-lookup"><span data-stu-id="8948a-104">D3DX\_FLOAT2\_to\_R16G16\_FLOAT function</span></span>

<span data-ttu-id="8948a-105">Vuelve a empaquetar el XMFLOAT2 determinado en un formato de DXGI \_ \_ R16G16 \_ float.</span><span class="sxs-lookup"><span data-stu-id="8948a-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="8948a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8948a-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="8948a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8948a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8948a-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="8948a-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8948a-109">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="8948a-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8948a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8948a-110">Return value</span></span>

<span data-ttu-id="8948a-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="8948a-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8948a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8948a-112">Requirements</span></span>



| <span data-ttu-id="8948a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8948a-113">Requirement</span></span> | <span data-ttu-id="8948a-114">Value</span><span class="sxs-lookup"><span data-stu-id="8948a-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8948a-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8948a-115">Header</span></span><br/> | <dl> <span data-ttu-id="8948a-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="8948a-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8948a-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8948a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8948a-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="8948a-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="8948a-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="8948a-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





