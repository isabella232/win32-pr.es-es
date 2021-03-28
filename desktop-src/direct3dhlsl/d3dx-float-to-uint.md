---
title: D3DX_FLOAT_to_UINT función)
description: Convierte un valor FLOAT en UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362458"
---
# <a name="d3dx_float_to_uint-function"></a><span data-ttu-id="7c354-104">D3DX \_ float \_ a \_ función uint</span><span class="sxs-lookup"><span data-stu-id="7c354-104">D3DX\_FLOAT\_to\_UINT function</span></span>

<span data-ttu-id="7c354-105">Convierte un valor FLOAT en UINT.</span><span class="sxs-lookup"><span data-stu-id="7c354-105">Converts a FLOAT value to UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c354-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c354-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="7c354-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c354-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c354-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="7c354-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="7c354-109">Vector v.</span><span class="sxs-lookup"><span data-stu-id="7c354-109">The v vector.</span></span>

</dd> <dt>

<span data-ttu-id="7c354-110">*\_Escala*</span><span class="sxs-lookup"><span data-stu-id="7c354-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="7c354-111">Valor de escala.</span><span class="sxs-lookup"><span data-stu-id="7c354-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c354-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c354-112">Return value</span></span>

<span data-ttu-id="7c354-113">Valor FLOAT convertido.</span><span class="sxs-lookup"><span data-stu-id="7c354-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="7c354-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c354-114">Requirements</span></span>



| <span data-ttu-id="7c354-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c354-115">Requirement</span></span> | <span data-ttu-id="7c354-116">Value</span><span class="sxs-lookup"><span data-stu-id="7c354-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c354-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c354-117">Header</span></span><br/> | <dl> <span data-ttu-id="7c354-118"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="7c354-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c354-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c354-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c354-120">Funciones</span><span class="sxs-lookup"><span data-stu-id="7c354-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="7c354-121">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="7c354-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





