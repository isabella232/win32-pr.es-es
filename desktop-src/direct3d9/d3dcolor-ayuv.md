---
description: Inicializa un color con los valores (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Macro D3DCOLOR_AYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649398"
---
# <a name="d3dcolor_ayuv-macro"></a><span data-ttu-id="a1210-103">D3DCOLOR \_ AYUV (macro)</span><span class="sxs-lookup"><span data-stu-id="a1210-103">D3DCOLOR\_AYUV macro</span></span>

<span data-ttu-id="a1210-104">Inicializa un color con los valores (a, y, u, v).</span><span class="sxs-lookup"><span data-stu-id="a1210-104">Initializes a color using the (a,y,u,v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1210-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1210-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="a1210-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1210-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1210-107">*un*</span><span class="sxs-lookup"><span data-stu-id="a1210-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="a1210-108">Componente alfa del color.</span><span class="sxs-lookup"><span data-stu-id="a1210-108">Alpha component of the color.</span></span> <span data-ttu-id="a1210-109">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a1210-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a1210-110">*y*</span><span class="sxs-lookup"><span data-stu-id="a1210-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a1210-111">Componente de luminancia del color.</span><span class="sxs-lookup"><span data-stu-id="a1210-111">Luminance component of the color.</span></span> <span data-ttu-id="a1210-112">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a1210-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a1210-113">*u*</span><span class="sxs-lookup"><span data-stu-id="a1210-113">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="a1210-114">Brillo azul del color.</span><span class="sxs-lookup"><span data-stu-id="a1210-114">Blue brightness of the color.</span></span> <span data-ttu-id="a1210-115">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a1210-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a1210-116">*v*</span><span class="sxs-lookup"><span data-stu-id="a1210-116">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="a1210-117">Brillo rojo del color.</span><span class="sxs-lookup"><span data-stu-id="a1210-117">Red brightness of the color.</span></span> <span data-ttu-id="a1210-118">Este valor debe estar en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="a1210-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1210-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1210-119">Return value</span></span>

<span data-ttu-id="a1210-120">Devuelve el valor de [D3DCOLOR](d3dcolor.md) que corresponde a los valores ARGB proporcionados.</span><span class="sxs-lookup"><span data-stu-id="a1210-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1210-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1210-121">Remarks</span></span>

<span data-ttu-id="a1210-122">Un color RGB se puede reducir a 16 bits por píxel mediante la conversión a las diferencias de luminancia y color con las ecuaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1210-122">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="a1210-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1210-123">Requirements</span></span>



| <span data-ttu-id="a1210-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1210-124">Requirement</span></span> | <span data-ttu-id="a1210-125">Value</span><span class="sxs-lookup"><span data-stu-id="a1210-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1210-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1210-126">Header</span></span><br/> | <dl> <span data-ttu-id="a1210-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1210-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1210-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1210-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1210-129">Macros</span><span class="sxs-lookup"><span data-stu-id="a1210-129">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="a1210-130">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a1210-130">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="a1210-131">**D3DCOLOR \_ XYUV**</span><span class="sxs-lookup"><span data-stu-id="a1210-131">**D3DCOLOR\_XYUV**</span></span>](d3dcolor-xyuv.md)
</dt> </dl>

 

 




