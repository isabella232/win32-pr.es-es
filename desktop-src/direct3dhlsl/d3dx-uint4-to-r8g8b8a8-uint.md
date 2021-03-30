---
title: D3DX_UINT4_to_R8G8B8A8_UINT función)
description: Vuelve a empaquetar el XMUINT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ uint.
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- D3DX_UINT4_to_R8G8B8A8_UINT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef8128d2d1989e986d8ff11e2d7e42e85f1fbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998394"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a><span data-ttu-id="cd29d-104">D3DX \_ UINT4 \_ a \_ R8G8B8A8 \_ uint (función)</span><span class="sxs-lookup"><span data-stu-id="cd29d-104">D3DX\_UINT4\_to\_R8G8B8A8\_UINT function</span></span>

<span data-ttu-id="cd29d-105">Vuelve a empaquetar el XMUINT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="cd29d-105">Packs the given XMUINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd29d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd29d-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="cd29d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd29d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd29d-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="cd29d-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29d-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="cd29d-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd29d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd29d-110">Return value</span></span>

<span data-ttu-id="cd29d-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="cd29d-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd29d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd29d-112">Requirements</span></span>



| <span data-ttu-id="cd29d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd29d-113">Requirement</span></span> | <span data-ttu-id="cd29d-114">Value</span><span class="sxs-lookup"><span data-stu-id="cd29d-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd29d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd29d-115">Header</span></span><br/> | <dl> <span data-ttu-id="cd29d-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="cd29d-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd29d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd29d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd29d-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="cd29d-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="cd29d-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="cd29d-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





