---
title: D3DX_SaturateSigned_FLOAT función)
description: Recupera un valor saturado con signo del valor FLOAT dado.
ms.assetid: 2737ea61-5dbf-4451-bb4f-436e6ea95db6
keywords:
- D3DX_SaturateSigned_FLOAT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_SaturateSigned_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e6ccf5cf941b1abd3577efa5899b8d827e24e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280390"
---
# <a name="d3dx_saturatesigned_float-function"></a><span data-ttu-id="17200-104">D3DX \_ SaturateSigned \_ float (función)</span><span class="sxs-lookup"><span data-stu-id="17200-104">D3DX\_SaturateSigned\_FLOAT function</span></span>

<span data-ttu-id="17200-105">Recupera un valor saturado con signo del valor FLOAT dado.</span><span class="sxs-lookup"><span data-stu-id="17200-105">Retrieves a signed saturated value from the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="17200-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17200-106">Syntax</span></span>

``` syntax
 D3DX_SaturateSigned_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="17200-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17200-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17200-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="17200-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="17200-109">Valor que se va a saturar.</span><span class="sxs-lookup"><span data-stu-id="17200-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17200-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17200-110">Return value</span></span>

<span data-ttu-id="17200-111">Valor saturado con signo.</span><span class="sxs-lookup"><span data-stu-id="17200-111">The signed saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="17200-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17200-112">Requirements</span></span>



| <span data-ttu-id="17200-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="17200-113">Requirement</span></span> | <span data-ttu-id="17200-114">Value</span><span class="sxs-lookup"><span data-stu-id="17200-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17200-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17200-115">Header</span></span><br/> | <dl> <span data-ttu-id="17200-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="17200-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17200-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="17200-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17200-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="17200-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="17200-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="17200-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





