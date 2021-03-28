---
title: D3DX_R16G16_UINT_to_UINT2 función)
description: Desempaqueta los \_ \_ \_ datos de sombreador de formato de DXGI R16G16 uint en un XMUINT2.
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- D3DX_R16G16_UINT_to_UINT2 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UINT_to_UINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2586ff8876ee10368d49b816b38f5c9c8caf7c7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362408"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a><span data-ttu-id="317ee-104">D3DX \_ R16G16 \_ uint \_ a la \_ función UINT2</span><span class="sxs-lookup"><span data-stu-id="317ee-104">D3DX\_R16G16\_UINT\_to\_UINT2 function</span></span>

<span data-ttu-id="317ee-105">Desempaqueta los \_ \_ \_ datos de sombreador de formato de DXGI R16G16 uint en un XMUINT2.</span><span class="sxs-lookup"><span data-stu-id="317ee-105">Unpacks DXGI\_FORMAT\_R16G16\_UINT shader data to an XMUINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="317ee-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="317ee-106">Syntax</span></span>

``` syntax
XMUINT2 D3DX_R16G16_UINT_to_UINT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="317ee-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="317ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="317ee-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="317ee-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="317ee-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="317ee-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="317ee-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="317ee-110">Return value</span></span>

<span data-ttu-id="317ee-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="317ee-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="317ee-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="317ee-112">Requirements</span></span>



| <span data-ttu-id="317ee-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="317ee-113">Requirement</span></span> | <span data-ttu-id="317ee-114">Value</span><span class="sxs-lookup"><span data-stu-id="317ee-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="317ee-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="317ee-115">Header</span></span><br/> | <dl> <span data-ttu-id="317ee-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="317ee-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="317ee-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="317ee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317ee-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="317ee-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="317ee-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="317ee-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





