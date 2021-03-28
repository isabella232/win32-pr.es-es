---
title: D3DX_UINT4_to_R10G10B10A2_UINT función)
description: Vuelve a empaquetar el XMINT4 determinado en un formato de DXGI \_ \_ R10G10B10A2 \_ uint.
ms.assetid: fe10c62e-2d84-4f6b-886b-247ee344f6c7
keywords:
- D3DX_UINT4_to_R10G10B10A2_UINT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R10G10B10A2_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc7076b9e44ab1491bb8abbf8d4edb82158282c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998395"
---
# <a name="d3dx_uint4_to_r10g10b10a2_uint-function"></a><span data-ttu-id="ef4c2-104">D3DX \_ UINT4 \_ a \_ R10G10B10A2 \_ uint (función)</span><span class="sxs-lookup"><span data-stu-id="ef4c2-104">D3DX\_UINT4\_to\_R10G10B10A2\_UINT function</span></span>

<span data-ttu-id="ef4c2-105">Vuelve a empaquetar el XMINT4 determinado en un formato de DXGI \_ \_ R10G10B10A2 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="ef4c2-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4c2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef4c2-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R10G10B10A2_UINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="ef4c2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef4c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef4c2-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="ef4c2-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="ef4c2-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="ef4c2-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef4c2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef4c2-110">Return value</span></span>

<span data-ttu-id="ef4c2-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="ef4c2-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4c2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef4c2-112">Requirements</span></span>



| <span data-ttu-id="ef4c2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef4c2-113">Requirement</span></span> | <span data-ttu-id="ef4c2-114">Value</span><span class="sxs-lookup"><span data-stu-id="ef4c2-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4c2-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef4c2-115">Header</span></span><br/> | <dl> <span data-ttu-id="ef4c2-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="ef4c2-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef4c2-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef4c2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4c2-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="ef4c2-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ef4c2-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="ef4c2-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





