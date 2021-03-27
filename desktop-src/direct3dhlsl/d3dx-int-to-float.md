---
title: D3DX_INT_to_FLOAT función)
description: Convierte un valor INT a FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987163"
---
# <a name="d3dx_int_to_float-function"></a><span data-ttu-id="4e940-104">D3DX \_ int \_ a \_ función Float</span><span class="sxs-lookup"><span data-stu-id="4e940-104">D3DX\_INT\_to\_FLOAT function</span></span>

<span data-ttu-id="4e940-105">Convierte un valor INT a FLOAT.</span><span class="sxs-lookup"><span data-stu-id="4e940-105">Converts a INT value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e940-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e940-106">Syntax</span></span>

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="4e940-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e940-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e940-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="4e940-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="4e940-109">Valor v.</span><span class="sxs-lookup"><span data-stu-id="4e940-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="4e940-110">*\_Escala*</span><span class="sxs-lookup"><span data-stu-id="4e940-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="4e940-111">Valor de escala.</span><span class="sxs-lookup"><span data-stu-id="4e940-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e940-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e940-112">Return value</span></span>

<span data-ttu-id="4e940-113">Valor int convertido.</span><span class="sxs-lookup"><span data-stu-id="4e940-113">The converted int value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e940-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e940-114">Requirements</span></span>



| <span data-ttu-id="4e940-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e940-115">Requirement</span></span> | <span data-ttu-id="4e940-116">Value</span><span class="sxs-lookup"><span data-stu-id="4e940-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e940-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e940-117">Header</span></span><br/> | <dl> <span data-ttu-id="4e940-118"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="4e940-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e940-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e940-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e940-120">Funciones</span><span class="sxs-lookup"><span data-stu-id="4e940-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4e940-121">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="4e940-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





