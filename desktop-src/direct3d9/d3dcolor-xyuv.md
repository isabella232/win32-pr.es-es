---
description: Inicializa un color con los valores (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: Macro D3DCOLOR_XYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914705"
---
# <a name="d3dcolor_xyuv-macro"></a><span data-ttu-id="9a250-103">D3DCOLOR \_ XYUV (macro)</span><span class="sxs-lookup"><span data-stu-id="9a250-103">D3DCOLOR\_XYUV macro</span></span>

<span data-ttu-id="9a250-104">Inicializa un color con los valores (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="9a250-104">Initializes a color with the (y, u, v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a250-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a250-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="9a250-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a250-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a250-107">*y*</span><span class="sxs-lookup"><span data-stu-id="9a250-107">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="9a250-108">Componente de luminancia del color.</span><span class="sxs-lookup"><span data-stu-id="9a250-108">Luminance component of the color.</span></span> <span data-ttu-id="9a250-109">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="9a250-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="9a250-110">*u*</span><span class="sxs-lookup"><span data-stu-id="9a250-110">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="9a250-111">Brillo azul del color.</span><span class="sxs-lookup"><span data-stu-id="9a250-111">Blue brightness of the color.</span></span> <span data-ttu-id="9a250-112">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="9a250-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="9a250-113">*v*</span><span class="sxs-lookup"><span data-stu-id="9a250-113">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="9a250-114">Brillo rojo del color.</span><span class="sxs-lookup"><span data-stu-id="9a250-114">Red brightness of the color.</span></span> <span data-ttu-id="9a250-115">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="9a250-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a250-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a250-116">Return value</span></span>

<span data-ttu-id="9a250-117">Devuelve el valor de [**D3DCOLOR**](d3dcolor.md) que corresponde a los valores proporcionados (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="9a250-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied (y, u, v) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a250-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a250-118">Remarks</span></span>

<span data-ttu-id="9a250-119">Un color RGB se puede reducir a 16 bits por píxel mediante la conversión a las diferencias de luminancia y color con las ecuaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="9a250-119">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="9a250-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a250-120">Requirements</span></span>



| <span data-ttu-id="9a250-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a250-121">Requirement</span></span> | <span data-ttu-id="9a250-122">Value</span><span class="sxs-lookup"><span data-stu-id="9a250-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a250-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a250-123">Header</span></span><br/> | <dl> <span data-ttu-id="9a250-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a250-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a250-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a250-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a250-126">Macros</span><span class="sxs-lookup"><span data-stu-id="9a250-126">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="9a250-127">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="9a250-127">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="9a250-128">**D3DCOLOR \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="9a250-128">**D3DCOLOR\_AYUV**</span></span>](d3dcolor-ayuv.md)
</dt> </dl>

 

 




