---
title: D3DX_R8G8B8A8_SINT_to_INT4 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador R8G8B8A8 de los formatos de DXGI en un XMINT4.
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- D3DX_R8G8B8A8_SINT_to_INT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157208"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a><span data-ttu-id="22c37-104">D3DX \_ R8G8B8A8 \_ Sint \_ a la \_ función INT4</span><span class="sxs-lookup"><span data-stu-id="22c37-104">D3DX\_R8G8B8A8\_SINT\_to\_INT4 function</span></span>

<span data-ttu-id="22c37-105">Desempaqueta los \_ datos del \_ \_ sombreador R8G8B8A8 de los formatos de DXGI en un XMINT4.</span><span class="sxs-lookup"><span data-stu-id="22c37-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c37-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22c37-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="22c37-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22c37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c37-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="22c37-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="22c37-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="22c37-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c37-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22c37-110">Return value</span></span>

<span data-ttu-id="22c37-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="22c37-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c37-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c37-112">Requirements</span></span>



| <span data-ttu-id="22c37-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c37-113">Requirement</span></span> | <span data-ttu-id="22c37-114">Value</span><span class="sxs-lookup"><span data-stu-id="22c37-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c37-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22c37-115">Header</span></span><br/> | <dl> <span data-ttu-id="22c37-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="22c37-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c37-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="22c37-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c37-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="22c37-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="22c37-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="22c37-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





