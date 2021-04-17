---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Describe los componentes rojo, verde, azul y alfa de un color. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678701"
---
# <a name="d2d1_color_f"></a><span data-ttu-id="525dd-105">\_Color \_ F de D2D1</span><span class="sxs-lookup"><span data-stu-id="525dd-105">D2D1\_COLOR\_F</span></span>

<span data-ttu-id="525dd-106">Describe los componentes rojo, verde, azul y alfa de un color.</span><span class="sxs-lookup"><span data-stu-id="525dd-106">Describes the red, green, blue, and alpha components of a color.</span></span>


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a><span data-ttu-id="525dd-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="525dd-107">Remarks</span></span>

<span data-ttu-id="525dd-108">**D2D1 \_ El COLOR \_ f** es una definición de tipo para el [**\_ color \_ f de D2D**](d2d-color-f.md), que es una definición de tipo para [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="525dd-108">**D2D1\_COLOR\_F** is a typedef for [**D2D\_COLOR\_F**](d2d-color-f.md), which is itself a typedef for [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span> <span data-ttu-id="525dd-109">Para obtener información sobre los miembros proporcionados por **D2D1 \_ color \_ F**, consulte [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="525dd-109">For information about the members provided by **D2D1\_COLOR\_F**, see [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span>

<span data-ttu-id="525dd-110">La clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) proporciona un conjunto de colores predefinidos y funciones auxiliares para definir colores.</span><span class="sxs-lookup"><span data-stu-id="525dd-110">The [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class provides a set of predefined colors and helper functions for defining colors.</span></span> <span data-ttu-id="525dd-111">Para obtener más información, consulte la referencia de [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="525dd-111">For more information, see the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) reference.</span></span>

## <a name="examples"></a><span data-ttu-id="525dd-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="525dd-112">Examples</span></span>

<span data-ttu-id="525dd-113">En el ejemplo siguiente se usa la clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar un color predefinido (negro) al crear un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="525dd-113">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a predefined color (black) when creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



<span data-ttu-id="525dd-114">En el ejemplo siguiente se usa la clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar un color con los valores rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="525dd-114">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a color using red, green, blue, and alpha values.</span></span>


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a><span data-ttu-id="525dd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="525dd-115">Requirements</span></span>



| <span data-ttu-id="525dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="525dd-116">Requirement</span></span> | <span data-ttu-id="525dd-117">Value</span><span class="sxs-lookup"><span data-stu-id="525dd-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="525dd-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="525dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="525dd-119">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="525dd-119">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="525dd-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="525dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="525dd-121">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="525dd-121">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="525dd-122">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="525dd-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="525dd-123">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="525dd-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="525dd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="525dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="525dd-125"><dt>D2DBaseTypes. h (incluye D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="525dd-125"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="525dd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="525dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="525dd-127">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="525dd-127">D3DCOLORVALUE</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="525dd-128">**ColorF**</span><span class="sxs-lookup"><span data-stu-id="525dd-128">**ColorF**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

