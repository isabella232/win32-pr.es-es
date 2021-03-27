---
title: D3DX_IsNan función)
description: Determina si el valor es un NaN (no un número).
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- D3DX_IsNan de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003948"
---
# <a name="d3dx_isnan-function"></a><span data-ttu-id="7e8f8-104">\_Función IsNan de D3DX</span><span class="sxs-lookup"><span data-stu-id="7e8f8-104">D3DX\_IsNan function</span></span>

<span data-ttu-id="7e8f8-105">Determina si el valor es un NaN (no un número).</span><span class="sxs-lookup"><span data-stu-id="7e8f8-105">Determines if the value is a NaN (Not a Number).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e8f8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e8f8-106">Syntax</span></span>

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="7e8f8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e8f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e8f8-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="7e8f8-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="7e8f8-109">Valor especificado.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-109">The specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e8f8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e8f8-110">Return value</span></span>

<span data-ttu-id="7e8f8-111">True si un NaN; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="7e8f8-111">true if a NaN; otherwise false.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e8f8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e8f8-112">Requirements</span></span>



| <span data-ttu-id="7e8f8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e8f8-113">Requirement</span></span> | <span data-ttu-id="7e8f8-114">Value</span><span class="sxs-lookup"><span data-stu-id="7e8f8-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8f8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e8f8-115">Header</span></span><br/> | <dl> <span data-ttu-id="7e8f8-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="7e8f8-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e8f8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e8f8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e8f8-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="7e8f8-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="7e8f8-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="7e8f8-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





