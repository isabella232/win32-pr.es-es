---
title: D3DX_R8G8B8A8_UINT_to_UINT4 función)
description: Desempaqueta los \_ \_ \_ datos de sombreador de formato de DXGI R8G8B8A8 uint en un XMUINT4.
ms.assetid: fe25041f-db18-4555-a77a-e8d487143aa6
keywords:
- D3DX_R8G8B8A8_UINT_to_UINT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a371a36e797e1bff17aff457e11b140e4775894
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986886"
---
# <a name="d3dx_r8g8b8a8_uint_to_uint4-function"></a><span data-ttu-id="36b8f-104">D3DX \_ R8G8B8A8 \_ uint \_ a la \_ función UINT4</span><span class="sxs-lookup"><span data-stu-id="36b8f-104">D3DX\_R8G8B8A8\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="36b8f-105">Desempaqueta los \_ \_ \_ datos de sombreador de formato de DXGI R8G8B8A8 uint en un XMUINT4.</span><span class="sxs-lookup"><span data-stu-id="36b8f-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UINT shader data to an XMUINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b8f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36b8f-106">Syntax</span></span>

``` syntax
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="36b8f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36b8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36b8f-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="36b8f-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="36b8f-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="36b8f-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36b8f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36b8f-110">Return value</span></span>

<span data-ttu-id="36b8f-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="36b8f-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b8f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36b8f-112">Requirements</span></span>



| <span data-ttu-id="36b8f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="36b8f-113">Requirement</span></span> | <span data-ttu-id="36b8f-114">Value</span><span class="sxs-lookup"><span data-stu-id="36b8f-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36b8f-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36b8f-115">Header</span></span><br/> | <dl> <span data-ttu-id="36b8f-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="36b8f-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b8f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="36b8f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b8f-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="36b8f-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="36b8f-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="36b8f-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





