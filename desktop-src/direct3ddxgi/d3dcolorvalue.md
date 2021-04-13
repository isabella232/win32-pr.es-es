---
description: Representa un valor de color con alfa, que se usa para la transparencia.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Estructura D3DCOLORVALUE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362551"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="2e397-103">Estructura D3DCOLORVALUE (Dxgitype. h)</span><span class="sxs-lookup"><span data-stu-id="2e397-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="2e397-104">Representa un valor de color con alfa, que se usa para la transparencia.</span><span class="sxs-lookup"><span data-stu-id="2e397-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e397-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e397-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="2e397-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e397-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e397-107">**r**</span><span class="sxs-lookup"><span data-stu-id="2e397-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="2e397-108">Valor de punto flotante que especifica el componente rojo de un color.</span><span class="sxs-lookup"><span data-stu-id="2e397-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="2e397-109">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="2e397-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="2e397-110">Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="2e397-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="2e397-111">**g**</span><span class="sxs-lookup"><span data-stu-id="2e397-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="2e397-112">Valor de punto flotante que especifica el componente verde de un color.</span><span class="sxs-lookup"><span data-stu-id="2e397-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="2e397-113">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="2e397-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="2e397-114">Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el color verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="2e397-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="2e397-115">**b**</span><span class="sxs-lookup"><span data-stu-id="2e397-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="2e397-116">Valor de punto flotante que especifica el componente azul de un color.</span><span class="sxs-lookup"><span data-stu-id="2e397-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="2e397-117">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="2e397-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="2e397-118">Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="2e397-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="2e397-119">**un**</span><span class="sxs-lookup"><span data-stu-id="2e397-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="2e397-120">Valor de punto flotante que especifica el componente alfa de un color.</span><span class="sxs-lookup"><span data-stu-id="2e397-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="2e397-121">Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="2e397-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="2e397-122">Un valor de 0,0 indica que es completamente transparente, mientras que un valor de 1,0 indica que es totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="2e397-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e397-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e397-123">Remarks</span></span>

<span data-ttu-id="2e397-124">Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales.</span><span class="sxs-lookup"><span data-stu-id="2e397-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="2e397-125">Los valores mayores que 1 producen luces fuertes que tienden a lavar una escena.</span><span class="sxs-lookup"><span data-stu-id="2e397-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="2e397-126">Los valores negativos producen luces oscuras que realmente quitan la luz de una escena.</span><span class="sxs-lookup"><span data-stu-id="2e397-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="2e397-127">El tipo de encabezado DXGItype. h: define la [**DXGI \_ RGBA**](dxgi-rgba.md) como un alias de **D3DCOLORVALUE**, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2e397-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="2e397-128">Puede usar D3DCOLORVALUE o [**dxgi \_ RGBA**](dxgi-rgba.md) con [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)y el [**\_ \_ modo alfa de dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="2e397-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e397-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e397-129">Requirements</span></span>



| <span data-ttu-id="2e397-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e397-130">Requirement</span></span> | <span data-ttu-id="2e397-131">Value</span><span class="sxs-lookup"><span data-stu-id="2e397-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e397-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e397-132">Header</span></span><br/> | <dl> <span data-ttu-id="2e397-133"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e397-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e397-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e397-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e397-135">Estructuras de DXGI</span><span class="sxs-lookup"><span data-stu-id="2e397-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="2e397-136">**RGBA de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="2e397-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




