---
description: GDI+ proporciona degradados lineales horizontales, verticales y diagonales. De forma predeterminada, el color de un degradado lineal cambia de forma uniforme. Sin embargo, puede personalizar un degradado lineal para que el color cambie de manera no uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Crear un degradado lineal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565171"
---
# <a name="creating-a-linear-gradient"></a><span data-ttu-id="08f9d-105">Crear un degradado lineal</span><span class="sxs-lookup"><span data-stu-id="08f9d-105">Creating a Linear Gradient</span></span>

<span data-ttu-id="08f9d-106">GDI+ proporciona degradados lineales horizontales, verticales y diagonales.</span><span class="sxs-lookup"><span data-stu-id="08f9d-106">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="08f9d-107">De forma predeterminada, el color de un degradado lineal cambia de forma uniforme.</span><span class="sxs-lookup"><span data-stu-id="08f9d-107">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="08f9d-108">Sin embargo, puede personalizar un degradado lineal para que el color cambie de manera no uniforme.</span><span class="sxs-lookup"><span data-stu-id="08f9d-108">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>

-   [<span data-ttu-id="08f9d-109">Degradados lineales horizontales</span><span class="sxs-lookup"><span data-stu-id="08f9d-109">Horizontal Linear Gradients</span></span>](#horizontal-linear-gradients)
-   [<span data-ttu-id="08f9d-110">Personalizar degradados lineales</span><span class="sxs-lookup"><span data-stu-id="08f9d-110">Customizing Linear Gradients</span></span>](#customizing-linear-gradients)
-   [<span data-ttu-id="08f9d-111">Degradados lineales diagonales</span><span class="sxs-lookup"><span data-stu-id="08f9d-111">Diagonal Linear Gradients</span></span>](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a><span data-ttu-id="08f9d-112">Degradados lineales horizontales</span><span class="sxs-lookup"><span data-stu-id="08f9d-112">Horizontal Linear Gradients</span></span>

<span data-ttu-id="08f9d-113">En el ejemplo siguiente se usa un pincel de degradado lineal horizontal para rellenar una línea, una elipse y un rectángulo:</span><span class="sxs-lookup"><span data-stu-id="08f9d-113">The following example uses a horizontal linear gradient brush to fill a line, an ellipse, and a rectangle:</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="08f9d-114">El constructor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) recibe cuatro argumentos: dos puntos y dos colores.</span><span class="sxs-lookup"><span data-stu-id="08f9d-114">The [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="08f9d-115">El primer punto (0,0) está asociado al primer color (rojo) y el segundo (200, 10) se asocia al segundo color (azul).</span><span class="sxs-lookup"><span data-stu-id="08f9d-115">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="08f9d-116">Como cabría esperar, la línea dibujada de (0,0) a (200, 10) cambia gradualmente de rojo a azul.</span><span class="sxs-lookup"><span data-stu-id="08f9d-116">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>

<span data-ttu-id="08f9d-117">La decenas en los puntos (50, 10) y (200, 10) no es importante.</span><span class="sxs-lookup"><span data-stu-id="08f9d-117">The 10s in the points (50, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="08f9d-118">Lo importante es que los dos puntos tienen la misma segunda coordenada; la línea que los conecta es horizontal.</span><span class="sxs-lookup"><span data-stu-id="08f9d-118">What's important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="08f9d-119">La elipse y el rectángulo también cambian gradualmente de rojo a azul, ya que la coordenada horizontal va de 0 a 200.</span><span class="sxs-lookup"><span data-stu-id="08f9d-119">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>

<span data-ttu-id="08f9d-120">En la ilustración siguiente se muestra la línea, la elipse y el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="08f9d-120">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="08f9d-121">Tenga en cuenta que el degradado de color se repite a medida que la coordenada horizontal aumenta más allá de 200.</span><span class="sxs-lookup"><span data-stu-id="08f9d-121">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>

![Ilustración que muestra un degradado horizontal que rellena una línea y una elipse, y un rectángulo que es más largo que la elipse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a><span data-ttu-id="08f9d-123">Personalizar degradados lineales</span><span class="sxs-lookup"><span data-stu-id="08f9d-123">Customizing Linear Gradients</span></span>

<span data-ttu-id="08f9d-124">En el ejemplo anterior, los componentes de color cambian linealmente a medida que se desplaza de una coordenada horizontal de 0 a una coordenada horizontal de 200.</span><span class="sxs-lookup"><span data-stu-id="08f9d-124">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="08f9d-125">Por ejemplo, un punto cuya primera coordenada sea la mitad entre 0 y 200 tendrá un componente azul que se encuentra a la mitad de la distancia entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="08f9d-125">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>

<span data-ttu-id="08f9d-126">GDI+ permite ajustar el modo en que un color varía de un borde de un degradado al otro.</span><span class="sxs-lookup"><span data-stu-id="08f9d-126">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="08f9d-127">Supongamos que desea crear un pincel de degradado que cambie de negro a rojo según la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="08f9d-127">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>



| <span data-ttu-id="08f9d-128">Coordenada horizontal</span><span class="sxs-lookup"><span data-stu-id="08f9d-128">Horizontal coordinate</span></span> | <span data-ttu-id="08f9d-129">Componentes RGB</span><span class="sxs-lookup"><span data-stu-id="08f9d-129">RGB components</span></span> |
|-----------------------|----------------|
| <span data-ttu-id="08f9d-130">0</span><span class="sxs-lookup"><span data-stu-id="08f9d-130">0</span></span>                     | <span data-ttu-id="08f9d-131">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="08f9d-131">(0, 0, 0)</span></span>      |
| <span data-ttu-id="08f9d-132">40</span><span class="sxs-lookup"><span data-stu-id="08f9d-132">40</span></span>                    | <span data-ttu-id="08f9d-133">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="08f9d-133">(128, 0, 0)</span></span>    |
| <span data-ttu-id="08f9d-134">200</span><span class="sxs-lookup"><span data-stu-id="08f9d-134">200</span></span>                   | <span data-ttu-id="08f9d-135">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="08f9d-135">(255, 0, 0)</span></span>    |



 

<span data-ttu-id="08f9d-136">Tenga en cuenta que el componente rojo está a mitad de intensidad cuando la coordenada horizontal es solo el 20 por ciento del camino de 0 a 200.</span><span class="sxs-lookup"><span data-stu-id="08f9d-136">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>

<span data-ttu-id="08f9d-137">En el ejemplo siguiente se llama al método [**LinearGradientBrush:: SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) de un objeto [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) para asociar tres intensidades relativas con tres posiciones relativas.</span><span class="sxs-lookup"><span data-stu-id="08f9d-137">The following example calls the [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) method of a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) object to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="08f9d-138">Como en la tabla anterior, una intensidad relativa de 0,5 está asociada a una posición relativa de 0,2.</span><span class="sxs-lookup"><span data-stu-id="08f9d-138">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="08f9d-139">El código rellena una elipse y un rectángulo con el pincel de degradado.</span><span class="sxs-lookup"><span data-stu-id="08f9d-139">The code fills an ellipse and a rectangle with the gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="08f9d-140">En la ilustración siguiente se muestra la elipse y el rectángulo resultantes.</span><span class="sxs-lookup"><span data-stu-id="08f9d-140">The following illustration shows the resulting ellipse and rectangle.</span></span>

![Ilustración que muestra un degradado horizontal que rellena una elipse y un rectángulo que es más largo que la elipse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a><span data-ttu-id="08f9d-142">Degradados lineales diagonales</span><span class="sxs-lookup"><span data-stu-id="08f9d-142">Diagonal Linear Gradients</span></span>

<span data-ttu-id="08f9d-143">Los degradados de los ejemplos anteriores han sido horizontales; es decir, el color cambia gradualmente a medida que se mueve a lo largo de cualquier línea horizontal.</span><span class="sxs-lookup"><span data-stu-id="08f9d-143">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="08f9d-144">También puede definir degradados verticales y degradados diagonales.</span><span class="sxs-lookup"><span data-stu-id="08f9d-144">You can also define vertical gradients and diagonal gradients.</span></span> <span data-ttu-id="08f9d-145">En el código siguiente se pasan los puntos (0,0) y (200, 100) a un constructor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="08f9d-145">The following code passes the points (0, 0) and (200, 100) to a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor.</span></span> <span data-ttu-id="08f9d-146">El color azul está asociado a (0,0) y el color verde está asociado a (200, 100).</span><span class="sxs-lookup"><span data-stu-id="08f9d-146">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="08f9d-147">Una línea (con el ancho de lápiz 10) y una elipse se rellenan con el pincel de degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="08f9d-147">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



<span data-ttu-id="08f9d-148">En la ilustración siguiente se muestra la línea y la elipse.</span><span class="sxs-lookup"><span data-stu-id="08f9d-148">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="08f9d-149">Tenga en cuenta que el color de la elipse cambia gradualmente a medida que se mueve a lo largo de cualquier línea que sea paralela a la línea que se pasa a través de (0,0) y (200, 100).</span><span class="sxs-lookup"><span data-stu-id="08f9d-149">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>

![Ilustración que muestra un degradado diagonal que rellena una elipse y una línea diagonal](images/lineargradient3.png)

 

 



