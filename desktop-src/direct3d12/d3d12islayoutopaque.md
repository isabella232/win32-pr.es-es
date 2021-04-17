---
title: Función D3D12IsLayoutOpaque (D3dx12. h)
description: Indica si el diseño es opaco.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque función)
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707756"
---
# <a name="d3d12islayoutopaque-function"></a><span data-ttu-id="fa1e2-104">D3D12IsLayoutOpaque función)</span><span class="sxs-lookup"><span data-stu-id="fa1e2-104">D3D12IsLayoutOpaque function</span></span>

<span data-ttu-id="fa1e2-105">Indica si el diseño es opaco.</span><span class="sxs-lookup"><span data-stu-id="fa1e2-105">Indicates whether the layout is opaque.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa1e2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa1e2-106">Syntax</span></span>


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a><span data-ttu-id="fa1e2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa1e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa1e2-108">*Diseño*</span><span class="sxs-lookup"><span data-stu-id="fa1e2-108">*Layout*</span></span> 
</dt> <dd>

<span data-ttu-id="fa1e2-109">Tipo: **[ **\_ \_ diseño de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span><span class="sxs-lookup"><span data-stu-id="fa1e2-109">Type: **[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span></span>

<span data-ttu-id="fa1e2-110">El diseño que se va a comprobar, como un [**\_ \_ diseño de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span><span class="sxs-lookup"><span data-stu-id="fa1e2-110">The layout to check, as a [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa1e2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa1e2-111">Return value</span></span>

<span data-ttu-id="fa1e2-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="fa1e2-112">Type: **bool**</span></span>

<span data-ttu-id="fa1e2-113">Un **booleano** que indica si el diseño es opaco.</span><span class="sxs-lookup"><span data-stu-id="fa1e2-113">A **bool** that indicates whether the layout is opaque.</span></span> <span data-ttu-id="fa1e2-114">Un diseño es opaco si es D3D12 \_ \_ diseño de textura \_ desconocido o D3D12 de \_ diseño de textura de \_ \_ 64 KB de SWIZZLE no \_ definidos \_ .</span><span class="sxs-lookup"><span data-stu-id="fa1e2-114">A layout is opaque if it is D3D12\_TEXTURE\_LAYOUT\_UNKNOWN or D3D12\_TEXTURE\_LAYOUT\_64KB\_UNDEFINED\_SWIZZLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa1e2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa1e2-115">Requirements</span></span>



| <span data-ttu-id="fa1e2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa1e2-116">Requirement</span></span> | <span data-ttu-id="fa1e2-117">Value</span><span class="sxs-lookup"><span data-stu-id="fa1e2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1e2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa1e2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fa1e2-119"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa1e2-119"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fa1e2-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa1e2-120">Library</span></span><br/> | <dl> <span data-ttu-id="fa1e2-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa1e2-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa1e2-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa1e2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="fa1e2-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa1e2-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa1e2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa1e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa1e2-125">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="fa1e2-125">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





