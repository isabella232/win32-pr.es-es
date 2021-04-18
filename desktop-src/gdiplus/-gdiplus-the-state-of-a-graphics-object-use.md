---
description: La clase Graphics es la esencia de Windows GDI+. Para dibujar algo, debe crear un objeto Graphics, establecer sus propiedades y llamar a sus métodos (DrawLine, DrawImage, DrawString y like).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Estado de un objeto de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571461"
---
# <a name="the-state-of-a-graphics-object"></a><span data-ttu-id="2ae1b-104">Estado de un objeto de gráficos</span><span class="sxs-lookup"><span data-stu-id="2ae1b-104">The State of a Graphics Object</span></span>

<span data-ttu-id="2ae1b-105">La clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) es la esencia de Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is at the heart of Windows GDI+.</span></span> <span data-ttu-id="2ae1b-106">Para dibujar algo, debe crear un objeto **Graphics** , establecer sus propiedades y llamar a sus métodos ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))y like).</span><span class="sxs-lookup"><span data-stu-id="2ae1b-106">To draw anything, you create a **Graphics** object, set its properties, and call its methods ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)), and the like).</span></span>

<span data-ttu-id="2ae1b-107">En el ejemplo siguiente se crea un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y, a continuación, se llama al método [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) del objeto **Graphics** :</span><span class="sxs-lookup"><span data-stu-id="2ae1b-107">The following example constructs a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and then calls the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object:</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



<span data-ttu-id="2ae1b-108">En el código anterior, el método [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) devuelve un identificador a un contexto de dispositivo y ese identificador se pasa al constructor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-108">In the preceding code, the [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) method returns a handle to a device context, and that handle is passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="2ae1b-109">Un contexto de dispositivo es una estructura (mantenida por Windows) que contiene información sobre el dispositivo de pantalla concreto que se está usando.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-109">A device context is a structure (maintained by Windows) that holds information about the particular display device being used.</span></span>

## <a name="graphics-state"></a><span data-ttu-id="2ae1b-110">Estado de gráficos</span><span class="sxs-lookup"><span data-stu-id="2ae1b-110">Graphics State</span></span>

<span data-ttu-id="2ae1b-111">Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) hace más que proporcionar métodos de dibujo, como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) y [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="2ae1b-111">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object does more than provide drawing methods, such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span></span> <span data-ttu-id="2ae1b-112">Un objeto **Graphics** también mantiene el estado de los gráficos, que se puede dividir en las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="2ae1b-112">A **Graphics** object also maintains graphics state, which can be divided into the following categories:</span></span>

-   <span data-ttu-id="2ae1b-113">Un vínculo a un contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2ae1b-113">A link to a device context</span></span>
-   <span data-ttu-id="2ae1b-114">Configuración de calidad</span><span class="sxs-lookup"><span data-stu-id="2ae1b-114">Quality settings</span></span>
-   <span data-ttu-id="2ae1b-115">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="2ae1b-115">Transformations</span></span>
-   <span data-ttu-id="2ae1b-116">Una región de recorte</span><span class="sxs-lookup"><span data-stu-id="2ae1b-116">A clipping region</span></span>

### <a name="device-context"></a><span data-ttu-id="2ae1b-117">Contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2ae1b-117">Device Context</span></span>

<span data-ttu-id="2ae1b-118">Como programador de la aplicación, no tiene que pensar en la interacción entre un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y su contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-118">As an application programmer, you don't have to think about the interaction between a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and its device context.</span></span> <span data-ttu-id="2ae1b-119">Esta interacción se controla mediante GDI+ en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-119">This interaction is handled by GDI+ behind the scenes.</span></span>

### <a name="quality-settings"></a><span data-ttu-id="2ae1b-120">Configuración de calidad</span><span class="sxs-lookup"><span data-stu-id="2ae1b-120">Quality Settings</span></span>

<span data-ttu-id="2ae1b-121">Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tiene varias propiedades que influyen en la calidad de los elementos que se dibujan en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-121">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object has several properties that influence the quality of the items that are drawn on the screen.</span></span> <span data-ttu-id="2ae1b-122">Puede ver y manipular estas propiedades mediante una llamada a los métodos GET y set.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-122">You can view and manipulate these properties by calling get and set methods.</span></span> <span data-ttu-id="2ae1b-123">Por ejemplo, puede llamar al método [**Graphics:: SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) para especificar el tipo de suavizado de contorno que se aplica al texto.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-123">For example, you can call the [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="2ae1b-124">Otros métodos set que afectan a la calidad son [**Graphics:: SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)y [**Graphics:: SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span><span class="sxs-lookup"><span data-stu-id="2ae1b-124">Other set methods that influence quality are [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality), and [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span></span>

<span data-ttu-id="2ae1b-125">En el ejemplo siguiente se dibujan dos elipses, una con el modo de suavizado establecido en [\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) \* \* y otra con el modo de suavizado establecido en [\* \* \* \* SmoothingModeHighSpeed \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \*:</span><span class="sxs-lookup"><span data-stu-id="2ae1b-125">The following example draws two ellipses, one with the smoothing mode set to [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) and one with the smoothing mode set to [\*\*\*\*SmoothingModeHighSpeed\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a><span data-ttu-id="2ae1b-126">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="2ae1b-126">Transformations</span></span>

<span data-ttu-id="2ae1b-127">Un objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene dos transformaciones (universal y de página) que se aplican a todos los elementos dibujados por ese objeto de **gráficos** .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-127">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains two transformations (world and page) that are applied to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="2ae1b-128">Cualquier transformación afín puede almacenarse en la transformación universal.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-128">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="2ae1b-129">Las transformaciones afines incluyen el escalado, la rotación, la reflexión, el sesgo y la traducción.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-129">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="2ae1b-130">La transformación página se puede usar para escalar y para cambiar las unidades (por ejemplo, de píxeles a pulgadas).</span><span class="sxs-lookup"><span data-stu-id="2ae1b-130">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="2ae1b-131">Para obtener más información sobre las transformaciones, vea [sistemas de coordenadas y transformaciones](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="2ae1b-131">For more information on transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="2ae1b-132">En el ejemplo siguiente se establecen las transformaciones de página y el mundo de un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-132">The following example sets the world and page transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="2ae1b-133">La transformación universal se establece en una rotación de 30 grados.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-133">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="2ae1b-134">La transformación página se establece para que las coordenadas pasadas al segundo [**gráfico::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) se traten como milímetros en lugar de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-134">The page transformation is set so that the coordinates passed to the second [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="2ae1b-135">El código realiza dos llamadas idénticas al método **Graphics::D rawellipse** .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-135">The code makes two identical calls to the **Graphics::DrawEllipse** method.</span></span> <span data-ttu-id="2ae1b-136">La transformación universal se aplica a la primera llamada de **gráficos::D rawellipse** y las dos transformaciones (universal y de página) se aplican a la segunda llamada de **gráficos::D rawellipse** .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-136">The world transformation is applied to the first **Graphics::DrawEllipse** call, and both transformations (world and page) are applied to the second **Graphics::DrawEllipse** call.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



<span data-ttu-id="2ae1b-137">En la ilustración siguiente se muestran los dos puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-137">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="2ae1b-138">Tenga en cuenta que la rotación de 30 grados se centra en el origen del sistema de coordenadas (esquina superior izquierda del área de cliente), no en los centros de las elipses.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-138">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="2ae1b-139">Tenga en cuenta también que el ancho del lápiz de 1 significa 1 píxel para la primera elipse y 1 milímetro para la segunda elipse.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-139">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>

![captura de pantalla de una ventana que contiene una elipse pequeña, fina y una elipse grande y gruesa](images/graphicsascon1.png)

 

### <a name="clipping-region"></a><span data-ttu-id="2ae1b-141">Región de recorte</span><span class="sxs-lookup"><span data-stu-id="2ae1b-141">Clipping Region</span></span>

<span data-ttu-id="2ae1b-142">Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene una región de recorte que se aplica a todos los elementos dibujados por ese objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-142">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains a clipping region that applies to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="2ae1b-143">Puede establecer la región de recorte llamando al método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-143">You can set the clipping region by calling the [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method.</span></span>

<span data-ttu-id="2ae1b-144">En el ejemplo siguiente se crea una región con forma de signo más formando la Unión de dos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-144">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="2ae1b-145">Esa región se designa como la región de recorte de un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="2ae1b-145">That region is designated as the clipping region of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="2ae1b-146">A continuación, el código dibuja dos líneas que están restringidas al interior de la región de recorte.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-146">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



<span data-ttu-id="2ae1b-147">En la ilustración siguiente se muestran las líneas recortadas.</span><span class="sxs-lookup"><span data-stu-id="2ae1b-147">The following illustration shows the clipped lines.</span></span>

![Ilustración en la que se muestra una forma coloreada en dos líneas rojas diagonales](images/graphicsascon2.png)

 

 
