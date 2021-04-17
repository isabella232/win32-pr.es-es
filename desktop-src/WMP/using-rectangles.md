---
title: Usar rectángulos (SDK de Windows Media Player)
description: Usar rectángulos
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualizaciones, rectángulos
- visualizaciones personalizadas, rectángulos
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705109"
---
# <a name="using-rectangles-windows-media-player-sdk"></a><span data-ttu-id="24a10-108">Usar rectángulos (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="24a10-108">Using Rectangles (Windows Media Player SDK)</span></span>

<span data-ttu-id="24a10-109">Los rectángulos se usan para especificar áreas rectangulares en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="24a10-109">Rectangles are used to specify rectangular areas in Microsoft Windows.</span></span> <span data-ttu-id="24a10-110">Puede crear muchos rectángulos en la ventana, pero Windows Media Player proporciona los valores de un rectángulo a través de la función [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) .</span><span class="sxs-lookup"><span data-stu-id="24a10-110">You can create many rectangles in your window, but Windows Media Player supplies the values of one rectangle through the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function.</span></span> <span data-ttu-id="24a10-111">Si el complemento se representa mediante una ventana, el rectángulo es el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="24a10-111">If your plug-in renders using a window, the rectangle is the client area of the window.</span></span> <span data-ttu-id="24a10-112">Esto se denomina rectángulo PRC y define el rectángulo en el que Windows Media Player mostrará la visualización.</span><span class="sxs-lookup"><span data-stu-id="24a10-112">This is called the prc rectangle, and it defines the rectangle that Windows Media Player will display your visualization through.</span></span> <span data-ttu-id="24a10-113">Úselo con frecuencia para asegurarse de que no se dibuja más allá de las extensiones del rectángulo proporcionado por Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="24a10-113">Use this frequently to be sure you do not draw beyond the extents of the rectangle supplied by Windows Media Player.</span></span>

<span data-ttu-id="24a10-114">Un rectángulo tiene cuatro valores que lo definen.</span><span class="sxs-lookup"><span data-stu-id="24a10-114">A rectangle has four values that define it.</span></span> <span data-ttu-id="24a10-115">Son izquierda, superior, derecha e inferior.</span><span class="sxs-lookup"><span data-stu-id="24a10-115">They are left, top, right, and bottom.</span></span> <span data-ttu-id="24a10-116">La esquina superior izquierda del rectángulo se define por la izquierda y la parte superior, y la esquina inferior derecha del rectángulo se define por la parte inferior y derecha.</span><span class="sxs-lookup"><span data-stu-id="24a10-116">The top, left corner of the rectangle is defined by left and top, and the bottom, right corner of the rectangle is defined by bottom and right.</span></span>

<span data-ttu-id="24a10-117">Use el código siguiente para obtener las extensiones del rectángulo del dibujo.</span><span class="sxs-lookup"><span data-stu-id="24a10-117">Use the following code to get the extents of your drawing rectangle.</span></span> <span data-ttu-id="24a10-118">Debe hacerlo porque el usuario puede cambiar el tamaño de la ventana y desea asegurarse de que siempre dibuja en un área que el usuario puede ver.</span><span class="sxs-lookup"><span data-stu-id="24a10-118">You need to do this because the user may resize the window, and you want to be sure that you are always drawing in an area the user can see.</span></span>


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



<span data-ttu-id="24a10-119">Por ejemplo, para dibujar de izquierda a derecha, a lo largo de la parte superior de la ventana, use código similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="24a10-119">For example, to draw from left to right, along the top of the window, use code like this:</span></span>


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a><span data-ttu-id="24a10-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24a10-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24a10-121">**Implementación de render**</span><span class="sxs-lookup"><span data-stu-id="24a10-121">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




