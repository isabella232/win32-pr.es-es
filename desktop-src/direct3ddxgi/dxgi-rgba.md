---
description: 'DXGI_RGBA estructura: representa un valor de color con alfa, que se usa para la transparencia.'
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA estructura (DXGItype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114273"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="d04fe-103">Estructura \_ RGBA de DXGI</span><span class="sxs-lookup"><span data-stu-id="d04fe-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="d04fe-104">Representa un valor de color con alfa, que se usa para la transparencia.</span><span class="sxs-lookup"><span data-stu-id="d04fe-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="d04fe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d04fe-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="d04fe-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d04fe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d04fe-107">**r**</span><span class="sxs-lookup"><span data-stu-id="d04fe-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="d04fe-108">Valor de punto flotante que especifica el componente rojo de un color.</span><span class="sxs-lookup"><span data-stu-id="d04fe-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="d04fe-109">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d04fe-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d04fe-110">Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="d04fe-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="d04fe-111">**g**</span><span class="sxs-lookup"><span data-stu-id="d04fe-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="d04fe-112">Valor de punto flotante que especifica el componente verde de un color.</span><span class="sxs-lookup"><span data-stu-id="d04fe-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="d04fe-113">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d04fe-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d04fe-114">Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="d04fe-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="d04fe-115">**b**</span><span class="sxs-lookup"><span data-stu-id="d04fe-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="d04fe-116">Valor de punto flotante que especifica el componente azul de un color.</span><span class="sxs-lookup"><span data-stu-id="d04fe-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="d04fe-117">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d04fe-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d04fe-118">Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="d04fe-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="d04fe-119">**Un**</span><span class="sxs-lookup"><span data-stu-id="d04fe-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="d04fe-120">Valor de punto flotante que especifica el componente alfa de un color.</span><span class="sxs-lookup"><span data-stu-id="d04fe-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="d04fe-121">Este valor suele estar en el intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d04fe-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d04fe-122">Un valor de 0,0 indica totalmente transparente, mientras que un valor de 1,0 indica totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="d04fe-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d04fe-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d04fe-123">Remarks</span></span>

<span data-ttu-id="d04fe-124">Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales.</span><span class="sxs-lookup"><span data-stu-id="d04fe-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="d04fe-125">Los valores mayores que 1 producen luces fuertes que tienden a apagar una escena.</span><span class="sxs-lookup"><span data-stu-id="d04fe-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="d04fe-126">Los valores negativos generan luces oscuras que realmente quitan la luz de una escena.</span><span class="sxs-lookup"><span data-stu-id="d04fe-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="d04fe-127">El tipo de encabezado DXGItype.h define **DXGI \_ RGBA** como un alias [**de D3DCOLORVALUE**](d3dcolorvalue.md), como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d04fe-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="d04fe-128">Puede usar **DXGI \_ RGBA** con [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)y [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="d04fe-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="d04fe-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d04fe-129">Requirements</span></span>



| <span data-ttu-id="d04fe-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d04fe-130">Requirement</span></span> | <span data-ttu-id="d04fe-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d04fe-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d04fe-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d04fe-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d04fe-133">Windows 8 y actualización de plataforma para aplicaciones de escritorio de Windows 7 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="d04fe-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d04fe-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d04fe-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d04fe-135">Windows Server 2012 y actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 R2 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="d04fe-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d04fe-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d04fe-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d04fe-137"><dt>DXGItype.h</dt></span><span class="sxs-lookup"><span data-stu-id="d04fe-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="d04fe-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d04fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d04fe-139">Estructuras DXGI</span><span class="sxs-lookup"><span data-stu-id="d04fe-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="d04fe-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="d04fe-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="d04fe-141">**D3DCOLORVALUE (en Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="d04fe-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
