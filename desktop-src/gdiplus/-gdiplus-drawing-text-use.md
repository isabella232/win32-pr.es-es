---
description: Puede usar el método DrawString de la clase Graphics para dibujar texto en una ubicación especificada o dentro de un rectángulo especificado.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Dibujo de texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156193"
---
# <a name="drawing-text-gdi"></a><span data-ttu-id="b43fe-103">Dibujo de texto (GDI+)</span><span class="sxs-lookup"><span data-stu-id="b43fe-103">Drawing Text (GDI+)</span></span>

<span data-ttu-id="b43fe-104">Puede usar el método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar texto en una ubicación especificada o dentro de un rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="b43fe-104">You can use the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw text at a specified location or within a specified rectangle.</span></span>

-   [<span data-ttu-id="b43fe-105">Dibujar texto en una ubicación especificada</span><span class="sxs-lookup"><span data-stu-id="b43fe-105">Drawing Text at a Specified Location</span></span>](#drawing-text-at-a-specified-location)
-   [<span data-ttu-id="b43fe-106">Dibujar texto en un rectángulo</span><span class="sxs-lookup"><span data-stu-id="b43fe-106">Drawing Text in a Rectangle</span></span>](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a><span data-ttu-id="b43fe-107">Dibujar texto en una ubicación especificada</span><span class="sxs-lookup"><span data-stu-id="b43fe-107">Drawing Text at a Specified Location</span></span>

<span data-ttu-id="b43fe-108">Para dibujar texto en una ubicación especificada, se necesitan los objetos [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)y [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="b43fe-108">To draw text at a specified location, you need [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="b43fe-109">En el ejemplo siguiente se dibuja la cadena "Hello" en la ubicación (30, 10).</span><span class="sxs-lookup"><span data-stu-id="b43fe-109">The following example draws the string "Hello" at location (30, 10).</span></span> <span data-ttu-id="b43fe-110">La familia de fuentes es Times New Roman.</span><span class="sxs-lookup"><span data-stu-id="b43fe-110">The font family is Times New Roman.</span></span> <span data-ttu-id="b43fe-111">La fuente, que es un miembro individual de la familia de fuentes, es Times New Roman, tamaño de 24 píxeles, estilo normal.</span><span class="sxs-lookup"><span data-stu-id="b43fe-111">The font, which is an individual member of the font family, is Times New Roman, size 24 pixels, regular style.</span></span> <span data-ttu-id="b43fe-112">Supongamos que los **gráficos** son objetos [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existentes.</span><span class="sxs-lookup"><span data-stu-id="b43fe-112">Assume that **graphics** is an existing [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

<span data-ttu-id="b43fe-113">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="b43fe-113">The following illustration shows the output of the preceding code.</span></span>

![captura de pantalla de una ventana pequeña que contiene el texto "Hello"](images/fontstext1.png)

<span data-ttu-id="b43fe-115">En el ejemplo anterior, el constructor [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recibe una cadena que identifica la familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="b43fe-115">In the preceding example, the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a string that identifies the font family.</span></span> <span data-ttu-id="b43fe-116">La dirección del objeto **FontFamily** se pasa como primer argumento al constructor [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="b43fe-116">The address of the **FontFamily** object is passed as the first argument to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="b43fe-117">El segundo argumento pasado al constructor **Font** especifica el tamaño de la fuente medido en unidades dadas por el cuarto argumento.</span><span class="sxs-lookup"><span data-stu-id="b43fe-117">The second argument passed to the **Font** constructor specifies the size of the font measured in units given by the fourth argument.</span></span> <span data-ttu-id="b43fe-118">El tercer argumento especifica el estilo (normal, negrita, cursiva, etc.) de la fuente.</span><span class="sxs-lookup"><span data-stu-id="b43fe-118">The third argument specifies the style (regular, bold, italic, and so on) of the font.</span></span>

<span data-ttu-id="b43fe-119">El método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) recibe cinco argumentos.</span><span class="sxs-lookup"><span data-stu-id="b43fe-119">The [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method receives five arguments.</span></span> <span data-ttu-id="b43fe-120">El primer argumento es la cadena que se va a dibujar y el segundo argumento es la longitud (en caracteres, no bytes) de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="b43fe-120">The first argument is the string to be drawn, and the second argument is the length (in characters, not bytes) of that string.</span></span> <span data-ttu-id="b43fe-121">Si la cadena termina en null, puede pasar – 1 para la longitud.</span><span class="sxs-lookup"><span data-stu-id="b43fe-121">If the string is null-terminated, you can pass –1 for the length.</span></span> <span data-ttu-id="b43fe-122">El tercer argumento es la dirección del objeto de [**fuente**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) que se construyó previamente.</span><span class="sxs-lookup"><span data-stu-id="b43fe-122">The third argument is the address of the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object that was constructed previously.</span></span> <span data-ttu-id="b43fe-123">El cuarto argumento es un objeto de [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) que contiene las coordenadas de la esquina superior izquierda de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b43fe-123">The fourth argument is a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object that contains the coordinates of the upper-left corner of the string.</span></span> <span data-ttu-id="b43fe-124">El quinto argumento es la dirección de un objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) que se usará para rellenar los caracteres de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b43fe-124">The fifth argument is the address of a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object that will be used to fill the characters of the string.</span></span>

## <a name="drawing-text-in-a-rectangle"></a><span data-ttu-id="b43fe-125">Dibujar texto en un rectángulo</span><span class="sxs-lookup"><span data-stu-id="b43fe-125">Drawing Text in a Rectangle</span></span>

<span data-ttu-id="b43fe-126">Uno de los métodos [**DrawString**](https://www.bing.com/search?q=**DrawString**) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tiene un parámetro *RectF* .</span><span class="sxs-lookup"><span data-stu-id="b43fe-126">One of the [**DrawString**](https://www.bing.com/search?q=**DrawString**) methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has a *RectF* parameter.</span></span> <span data-ttu-id="b43fe-127">Al llamar a ese método **DrawString** , puede dibujar texto que se ajusta en un rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="b43fe-127">By calling that **DrawString** method, you can draw text that wraps in a specified rectangle.</span></span> <span data-ttu-id="b43fe-128">Para dibujar texto en un rectángulo, se necesitan los objetos **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)y [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="b43fe-128">To draw text in a rectangle, you need **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="b43fe-129">En el ejemplo siguiente se crea un rectángulo con la esquina superior izquierda (30, 10), el ancho 100 y el alto 122.</span><span class="sxs-lookup"><span data-stu-id="b43fe-129">The following example creates a rectangle with upper-left corner (30, 10), width 100, and height 122.</span></span> <span data-ttu-id="b43fe-130">A continuación, el código dibuja una cadena dentro de ese rectángulo.</span><span class="sxs-lookup"><span data-stu-id="b43fe-130">Then the code draws a string inside that rectangle.</span></span> <span data-ttu-id="b43fe-131">La cadena está restringida al rectángulo y se ajusta de tal forma que las palabras individuales no se rompen.</span><span class="sxs-lookup"><span data-stu-id="b43fe-131">The string is restricted to the rectangle and wraps in such a way that individual words are not broken.</span></span>

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

<span data-ttu-id="b43fe-132">En la ilustración siguiente se muestra el texto dibujado en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="b43fe-132">The following illustration shows the text drawn in the rectangle.</span></span>

![captura de pantalla de una ventana pequeña que contiene un recangle que aparece en la primera parte de una frase](images/fontstext2.png)

<span data-ttu-id="b43fe-134">En el ejemplo anterior, el cuarto argumento pasado al método [**DrawString**](https://www.bing.com/search?q=**DrawString**) es un objeto [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) que especifica el rectángulo delimitador del texto.</span><span class="sxs-lookup"><span data-stu-id="b43fe-134">In the preceding example, the fourth argument passed to the [**DrawString**](https://www.bing.com/search?q=**DrawString**) method is a [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) object that specifies the bounding rectangle for the text.</span></span> <span data-ttu-id="b43fe-135">El quinto parámetro es de tipo [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat): el argumento es **null** porque no se requiere ningún formato de cadena especial.</span><span class="sxs-lookup"><span data-stu-id="b43fe-135">The fifth parameter is of type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— the argument is **NULL** because no special string formatting is required.</span></span>
