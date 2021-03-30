---
title: D3DX_INT4_to_R8G8B8A8_SINT función)
description: Vuelve a empaquetar el XMINT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ Sint.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- D3DX_INT4_to_R8G8B8A8_SINT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998335"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a><span data-ttu-id="9bfc7-104">D3DX \_ INT4 \_ a \_ R8G8B8A8 \_ función Sint</span><span class="sxs-lookup"><span data-stu-id="9bfc7-104">D3DX\_INT4\_to\_R8G8B8A8\_SINT function</span></span>

<span data-ttu-id="9bfc7-105">Vuelve a empaquetar el XMINT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="9bfc7-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bfc7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bfc7-106">Syntax</span></span>

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="9bfc7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9bfc7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bfc7-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="9bfc7-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="9bfc7-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="9bfc7-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bfc7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bfc7-110">Return value</span></span>

<span data-ttu-id="9bfc7-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="9bfc7-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bfc7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bfc7-112">Requirements</span></span>



| <span data-ttu-id="9bfc7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bfc7-113">Requirement</span></span> | <span data-ttu-id="9bfc7-114">Value</span><span class="sxs-lookup"><span data-stu-id="9bfc7-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bfc7-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9bfc7-115">Header</span></span><br/> | <dl> <span data-ttu-id="9bfc7-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="9bfc7-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bfc7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bfc7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bfc7-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="9bfc7-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="9bfc7-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="9bfc7-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





