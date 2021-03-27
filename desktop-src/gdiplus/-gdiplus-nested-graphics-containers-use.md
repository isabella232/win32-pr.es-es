---
description: Windows GDI+ proporciona contenedores que puede usar para reemplazar o aumentar temporalmente parte del estado en un objeto gráfico.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Contenedores de gráficos anidados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001664"
---
# <a name="nested-graphics-containers"></a><span data-ttu-id="d7b5e-103">Contenedores de gráficos anidados</span><span class="sxs-lookup"><span data-stu-id="d7b5e-103">Nested Graphics Containers</span></span>

<span data-ttu-id="d7b5e-104">Windows GDI+ proporciona contenedores que puede usar para reemplazar o aumentar temporalmente parte del estado en un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-104">Windows GDI+ provides containers that you can use to temporarily replace or augment part of the state in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="d7b5e-105">Puede crear un contenedor llamando al método [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de un objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-105">You create a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object.</span></span> <span data-ttu-id="d7b5e-106">Puede llamar a **Graphics:: BeginContainer** repetidamente para formar contenedores anidados.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-106">You can call **Graphics::BeginContainer** repeatedly to form nested containers.</span></span>

## <a name="transformations-in-nested-containers"></a><span data-ttu-id="d7b5e-107">Transformaciones en contenedores anidados</span><span class="sxs-lookup"><span data-stu-id="d7b5e-107">Transformations in Nested Containers</span></span>

<span data-ttu-id="d7b5e-108">En el ejemplo siguiente se crea un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un contenedor dentro de ese objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-108">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="d7b5e-109">La transformación universal del objeto **Graphics** es una traducción de 100 unidades en la dirección x y 80 unidades en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-109">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="d7b5e-110">La transformación universal del contenedor es una rotación de 30 grados.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-110">The world transformation of the container is a 30-degree rotation.</span></span> <span data-ttu-id="d7b5e-111">El código realiza la llamada</span><span class="sxs-lookup"><span data-stu-id="d7b5e-111">The code makes the call</span></span>


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



<span data-ttu-id="d7b5e-112">ocasiones.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-112">twice.</span></span> <span data-ttu-id="d7b5e-113">La primera llamada a [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) está *dentro del contenedor*; es decir, la llamada se encuentra entre las llamadas a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span><span class="sxs-lookup"><span data-stu-id="d7b5e-113">The first call to [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is *inside the container*; that is, the call is in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span></span> <span data-ttu-id="d7b5e-114">La segunda llamada a **Graphics::D rawrectangle** es después de la llamada a **Graphics:: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-114">The second call to **Graphics::DrawRectangle** is after the call to **Graphics::EndContainer**.</span></span>


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



<span data-ttu-id="d7b5e-115">En el código anterior, el rectángulo dibujado desde dentro del contenedor se transforma primero por la transformación universal del contenedor (rotación) y, a continuación, por la transformación universal del objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (traslación).</span><span class="sxs-lookup"><span data-stu-id="d7b5e-115">In the preceding code, the rectangle drawn from inside the container is transformed first by the world transformation of the container (rotation) and then by the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object (translation).</span></span> <span data-ttu-id="d7b5e-116">El rectángulo dibujado desde fuera del contenedor solo se transforma por la transformación universal del objeto **Graphics** (traslación).</span><span class="sxs-lookup"><span data-stu-id="d7b5e-116">The rectangle drawn from outside the container is transformed only by the world transformation of the **Graphics** object (translation).</span></span> <span data-ttu-id="d7b5e-117">En la ilustración siguiente se muestran los dos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-117">The following illustration shows the two rectangles.</span></span>

![captura de pantalla de una ventana con dos rectángulos rojos centrados en el mismo punto, pero con diferentes giros](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a><span data-ttu-id="d7b5e-119">Recorte en contenedores anidados</span><span class="sxs-lookup"><span data-stu-id="d7b5e-119">Clipping in Nested Containers</span></span>

<span data-ttu-id="d7b5e-120">En el ejemplo siguiente se muestra cómo los contenedores anidados controlan las regiones de recorte.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-120">The following example illustrates how nested containers handle clipping regions.</span></span> <span data-ttu-id="d7b5e-121">El código crea un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un contenedor dentro de ese objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-121">The code creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="d7b5e-122">La región de recorte del objeto **Graphics** es un rectángulo y la región de recorte del contenedor es una elipse.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-122">The clipping region of the **Graphics** object is a rectangle, and the clipping region of the container is an ellipse.</span></span> <span data-ttu-id="d7b5e-123">El código realiza dos llamadas al método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-123">The code makes two calls to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method.</span></span> <span data-ttu-id="d7b5e-124">La primera llamada a **Graphics::D rawline** está dentro del contenedor y la segunda llamada a **graphics::D rawline** está fuera del contenedor (después de la llamada a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="d7b5e-124">The first call to **Graphics::DrawLine** is inside the container, and the second call to **Graphics::DrawLine** is outside the container (after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="d7b5e-125">La primera línea se recorta por la intersección de las dos regiones de recorte.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-125">The first line is clipped by the intersection of the two clipping regions.</span></span> <span data-ttu-id="d7b5e-126">La segunda línea solo se recorta en la región de recorte rectangular del objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-126">The second line is clipped only by the rectangular clipping region of the **Graphics** object.</span></span>


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



<span data-ttu-id="d7b5e-127">En la ilustración siguiente se muestran las dos líneas recortadas.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-127">The following illustration shows the two clipped lines.</span></span>

![Ilustración de una elipse dentro de un rectángulo, con una línea recortada por la elipse y la otra por el rectángulo](images/nestedcontainers2.png)

<span data-ttu-id="d7b5e-129">Como muestran los dos ejemplos anteriores, las transformaciones y las regiones de recorte son acumulativas en contenedores anidados.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-129">As the two preceding examples show, transformations and clipping regions are cumulative in nested containers.</span></span> <span data-ttu-id="d7b5e-130">Si establece las transformaciones mundiales del contenedor y del objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , ambas transformaciones se aplicarán a los elementos que se dibujen desde dentro del contenedor.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-130">If you set the world transformations of the container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, both transformations will apply to items drawn from inside the container.</span></span> <span data-ttu-id="d7b5e-131">En primer lugar, se aplicará la transformación del contenedor y la transformación del objeto de **gráficos** se aplicará en segundo lugar.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-131">The transformation of the container will be applied first, and the transformation of the **Graphics** object will be applied second.</span></span> <span data-ttu-id="d7b5e-132">Si establece las regiones de recorte del contenedor y el objeto de **gráficos** , los elementos dibujados desde dentro del contenedor se recortarán por la intersección de las dos regiones de recorte.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-132">If you set the clipping regions of the container and the **Graphics** object, items drawn from inside the container will be clipped by the intersection of the two clipping regions.</span></span>

## <a name="quality-settings-in-nested-containers"></a><span data-ttu-id="d7b5e-133">Configuración de calidad en contenedores anidados</span><span class="sxs-lookup"><span data-stu-id="d7b5e-133">Quality Settings in Nested Containers</span></span>

<span data-ttu-id="d7b5e-134">Los valores de calidad ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)y similares) en los contenedores anidados no son acumulativos. en su lugar, los valores de calidad del contenedor reemplazan temporalmente la configuración de calidad de un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-134">Quality settings ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the like) in nested containers are not cumulative; rather, the quality settings of the container temporarily replace the quality settings of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="d7b5e-135">Al crear un nuevo contenedor, la configuración de calidad de ese contenedor se establece en los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-135">When you create a new container, the quality settings for that container are set to default values.</span></span> <span data-ttu-id="d7b5e-136">Por ejemplo, supongamos que tiene un objeto **Graphics** con un modo de suavizado de [\* \* \* \* SmoothingModeAntiAlias \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \* \*.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-136">For example, suppose you have a **Graphics** object with a smoothing mode of [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span></span> <span data-ttu-id="d7b5e-137">Al crear un contenedor, el modo de suavizado dentro del contenedor es el modo de suavizado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-137">When you create a container, the smoothing mode inside the container is the default smoothing mode.</span></span> <span data-ttu-id="d7b5e-138">Puede establecer el modo de suavizado del contenedor y todos los elementos que se dibujen desde dentro del contenedor se dibujarán según el modo que establezca.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-138">You are free to set the smoothing mode of the container, and any items drawn from inside the container will be drawn according to the mode you set.</span></span> <span data-ttu-id="d7b5e-139">Los elementos dibujados después de la llamada a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) se dibujarán según el modo de suavizado ([\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\*) que había antes de la llamada a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="d7b5e-139">Items drawn after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will be drawn according to the smoothing mode ([\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

## <a name="several-layers-of-nested-containers"></a><span data-ttu-id="d7b5e-140">Varios niveles de contenedores anidados</span><span class="sxs-lookup"><span data-stu-id="d7b5e-140">Several Layers of Nested Containers</span></span>

<span data-ttu-id="d7b5e-141">No está limitado a un contenedor en un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-141">You are not limited to one container in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="d7b5e-142">Puede crear una secuencia de contenedores, cada uno anidado en el anterior, y puede especificar la transformación universal, la región de recorte y la configuración de calidad de cada uno de esos contenedores anidados.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-142">You can create a sequence of containers, each nested in the preceding, and you can specify the world transformation, clipping region, and quality settings of each of those nested containers.</span></span> <span data-ttu-id="d7b5e-143">Si llama a un método de dibujo desde dentro del contenedor más interno, las transformaciones se aplicarán en orden, comenzando por el contenedor más interno y finalizando con el contenedor más externo.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-143">If you call a drawing method from inside the innermost container, the transformations will be applied in order, starting with the innermost container and ending with the outermost container.</span></span> <span data-ttu-id="d7b5e-144">Los elementos dibujados desde dentro del contenedor más interno se recortarán por la intersección de todas las regiones de recorte.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-144">Items drawn from inside the innermost container will be clipped by the intersection of all the clipping regions.</span></span>

<span data-ttu-id="d7b5e-145">En el ejemplo siguiente se crea un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y se establece su sugerencia de representación de texto en [\* \* \* \* TextRenderingHintAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \*.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-145">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and sets its text rendering hint to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="d7b5e-146">El código crea dos contenedores, uno anidado dentro de otro.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-146">The code creates two containers, one nested within the other.</span></span> <span data-ttu-id="d7b5e-147">La sugerencia de representación de texto del contenedor externo está establecida en [\* \* \* \* TextRenderingHintSingleBitPerPixel \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \* y la sugerencia de representación de texto del contenedor interno está establecida en [\* \* \* \* TextRenderingHintAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \*.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-147">The text rendering hint of the outer container is set to [\*\*\*\*TextRenderingHintSingleBitPerPixel\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the text rendering hint of the inner container is set to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="d7b5e-148">El código dibuja tres cadenas: una del contenedor interno, una del contenedor externo y otra del propio objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="d7b5e-148">The code draws three strings: one from the inner container, one from the outer container, and one from the **Graphics** object itself.</span></span>


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



<span data-ttu-id="d7b5e-149">En la ilustración siguiente se muestran las tres cadenas.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-149">The following illustration shows the three strings.</span></span> <span data-ttu-id="d7b5e-150">Las cadenas dibujadas desde el contenedor interno y el objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) se suavizan mediante el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-150">The strings drawn from the inner container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object are smoothed by antialiasing.</span></span> <span data-ttu-id="d7b5e-151">La cadena dibujada desde el contenedor externo no se suaviza mediante el suavizado de contorno debido a la configuración de TextRenderingHintSingleBitPerPixel.</span><span class="sxs-lookup"><span data-stu-id="d7b5e-151">The string drawn from the outer container is not smoothed by antialiasing because of the TextRenderingHintSingleBitPerPixel setting.</span></span>

![Ilustración de un rectángulo que contiene la misma cadena allí. solo los caracteres de la primera y la última línea son suaves](images/nestedcontainers3.png)

 

 
