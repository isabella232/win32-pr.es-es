---
title: D3DX_FLOAT_to_INT función)
description: Convierte un valor FLOAT en INT.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- D3DX_FLOAT_to_INT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548110"
---
# <a name="d3dx_float_to_int-function"></a><span data-ttu-id="2ba00-104">D3DX \_ float \_ a \_ función int</span><span class="sxs-lookup"><span data-stu-id="2ba00-104">D3DX\_FLOAT\_to\_INT function</span></span>

<span data-ttu-id="2ba00-105">Convierte un valor FLOAT en INT.</span><span class="sxs-lookup"><span data-stu-id="2ba00-105">Converts a FLOAT value to INT.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba00-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ba00-106">Syntax</span></span>

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="2ba00-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ba00-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba00-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="2ba00-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="2ba00-109">Valor v.</span><span class="sxs-lookup"><span data-stu-id="2ba00-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="2ba00-110">*\_Escala*</span><span class="sxs-lookup"><span data-stu-id="2ba00-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="2ba00-111">Valor de escala.</span><span class="sxs-lookup"><span data-stu-id="2ba00-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ba00-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ba00-112">Return value</span></span>

<span data-ttu-id="2ba00-113">Valor FLOAT convertido.</span><span class="sxs-lookup"><span data-stu-id="2ba00-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba00-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ba00-114">Requirements</span></span>



| <span data-ttu-id="2ba00-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ba00-115">Requirement</span></span> | <span data-ttu-id="2ba00-116">Value</span><span class="sxs-lookup"><span data-stu-id="2ba00-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba00-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ba00-117">Header</span></span><br/> | <dl> <span data-ttu-id="2ba00-118"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="2ba00-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba00-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ba00-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba00-120">Funciones</span><span class="sxs-lookup"><span data-stu-id="2ba00-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="2ba00-121">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="2ba00-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





