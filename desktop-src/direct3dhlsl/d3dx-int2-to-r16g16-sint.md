---
title: D3DX_INT2_to_R16G16_SINT función)
description: Vuelve a empaquetar el XMINT2 determinado en un formato de DXGI \_ \_ R16G16 \_ Sint.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- D3DX_INT2_to_R16G16_SINT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987187"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a><span data-ttu-id="85312-104">D3DX \_ INT2 \_ a \_ R16G16 \_ función Sint</span><span class="sxs-lookup"><span data-stu-id="85312-104">D3DX\_INT2\_to\_R16G16\_SINT function</span></span>

<span data-ttu-id="85312-105">Vuelve a empaquetar el XMINT2 determinado en un formato de DXGI \_ \_ R16G16 \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="85312-105">Packs the given XMINT2 back into a DXGI\_FORMAT\_R16G16\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="85312-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85312-106">Syntax</span></span>

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="85312-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85312-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85312-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="85312-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="85312-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="85312-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85312-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85312-110">Return value</span></span>

<span data-ttu-id="85312-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="85312-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="85312-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85312-112">Requirements</span></span>



| <span data-ttu-id="85312-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="85312-113">Requirement</span></span> | <span data-ttu-id="85312-114">Value</span><span class="sxs-lookup"><span data-stu-id="85312-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85312-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85312-115">Header</span></span><br/> | <dl> <span data-ttu-id="85312-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="85312-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85312-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="85312-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85312-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="85312-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="85312-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="85312-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





