---
title: D3DX_B8G8R8A8_UNORM_to_FLOAT4 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de B8G8R8A8 UNORM con formato DXGI en un XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bca17f350d40b1f74884232da9d1250bdb0abd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986790"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a><span data-ttu-id="02faf-104">D3DX \_ B8G8R8A8 \_ UNORM \_ a la \_ función FLOAT4</span><span class="sxs-lookup"><span data-stu-id="02faf-104">D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="02faf-105">Desempaqueta los \_ datos del \_ \_ sombreador de B8G8R8A8 UNORM con formato DXGI en un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="02faf-105">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="02faf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02faf-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="02faf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02faf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02faf-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="02faf-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="02faf-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="02faf-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02faf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02faf-110">Return value</span></span>

<span data-ttu-id="02faf-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="02faf-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="02faf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02faf-112">Requirements</span></span>



| <span data-ttu-id="02faf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="02faf-113">Requirement</span></span> | <span data-ttu-id="02faf-114">Value</span><span class="sxs-lookup"><span data-stu-id="02faf-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02faf-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02faf-115">Header</span></span><br/> | <dl> <span data-ttu-id="02faf-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="02faf-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02faf-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="02faf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02faf-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="02faf-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="02faf-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="02faf-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





