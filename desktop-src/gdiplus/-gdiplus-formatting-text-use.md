---
description: Para aplicar formato especial al texto, inicialice un objeto StringFormat y pase la dirección de ese objeto al método DrawString de la clase Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Formato de texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552217"
---
# <a name="formatting-text-gdi"></a><span data-ttu-id="43329-103">Formato de texto (GDI+)</span><span class="sxs-lookup"><span data-stu-id="43329-103">Formatting Text (GDI+)</span></span>

<span data-ttu-id="43329-104">Para aplicar formato especial al texto, inicialice un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) y pase la dirección de ese objeto al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="43329-104">To apply special formatting to text, initialize a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and pass the address of that object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="43329-105">Para dibujar texto con formato en un rectángulo, se necesitan los objetos [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)y [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="43329-105">To draw formatted text in a rectangle, you need [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), and [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

-   [<span data-ttu-id="43329-106">Alinear texto</span><span class="sxs-lookup"><span data-stu-id="43329-106">Aligning Text</span></span>](#aligning-text)
-   [<span data-ttu-id="43329-107">Configuración de tabulaciones</span><span class="sxs-lookup"><span data-stu-id="43329-107">Setting Tab Stops</span></span>](#setting-tab-stops)
-   [<span data-ttu-id="43329-108">Dibujo de texto vertical</span><span class="sxs-lookup"><span data-stu-id="43329-108">Drawing Vertical Text</span></span>](#drawing-vertical-text)

## <a name="aligning-text"></a><span data-ttu-id="43329-109">Alinear texto</span><span class="sxs-lookup"><span data-stu-id="43329-109">Aligning Text</span></span>

<span data-ttu-id="43329-110">En el ejemplo siguiente se dibuja texto en un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="43329-110">The following example draws text in a rectangle.</span></span> <span data-ttu-id="43329-111">Cada línea de texto está centrada (de lado a lado) y todo el bloque de texto está centrado (de arriba abajo) en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="43329-111">Each line of text is centered (side to side), and the entire block of text is centered (top to bottom) in the rectangle.</span></span>


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="43329-112">En la ilustración siguiente se muestra el rectángulo y el texto centrado.</span><span class="sxs-lookup"><span data-stu-id="43329-112">The following illustration shows the rectangle and the centered text.</span></span>

![captura de pantalla de una ventana que contiene un rectángulo que contiene seis líneas de texto, centrado horizontalmente](images/fontstext3.png)

<span data-ttu-id="43329-114">El código anterior llama a dos métodos del objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat:: SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) y [**StringFormat:: SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span><span class="sxs-lookup"><span data-stu-id="43329-114">The preceding code calls two methods of the [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object: [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) and [**StringFormat::SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span></span> <span data-ttu-id="43329-115">La llamada a **StringFormat:: SetAlignment** especifica que cada línea de texto está centrada en el rectángulo proporcionado por el tercer argumento pasado al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) .</span><span class="sxs-lookup"><span data-stu-id="43329-115">The call to **StringFormat::SetAlignment** specifies that each line of text is centered in the rectangle given by the third argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method.</span></span> <span data-ttu-id="43329-116">La llamada a **StringFormat:: SetLineAlignment** especifica que el bloque de texto está centrado (de arriba abajo) en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="43329-116">The call to **StringFormat::SetLineAlignment** specifies that the block of text is centered (top to bottom) in the rectangle.</span></span>

<span data-ttu-id="43329-117">El valor [\* \* \* \* StringAlignmentCenter \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) \* \* es un elemento de la enumeración **StringAlignment** , que se declara en Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="43329-117">The value [\*\*\*\*StringAlignmentCenter\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) is an element of the **StringAlignment** enumeration, which is declared in Gdiplusenums.h.</span></span>

## <a name="setting-tab-stops"></a><span data-ttu-id="43329-118">Configuración de tabulaciones</span><span class="sxs-lookup"><span data-stu-id="43329-118">Setting Tab Stops</span></span>

<span data-ttu-id="43329-119">Puede establecer las tabulaciones para el texto llamando al método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) de un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) y, a continuación, pasando la dirección de ese objeto **StringFormat** al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="43329-119">You can set tab stops for text by calling the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and then passing the address of that **StringFormat** object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="43329-120">En el ejemplo siguiente se establecen tabulaciones en 150, 250 y 350.</span><span class="sxs-lookup"><span data-stu-id="43329-120">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="43329-121">Después, el código muestra una lista con pestañas de nombres y puntuaciones de pruebas.</span><span class="sxs-lookup"><span data-stu-id="43329-121">Then the code displays a tabbed list of names and test scores.</span></span>


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="43329-122">En la ilustración siguiente se muestra el texto con pestañas.</span><span class="sxs-lookup"><span data-stu-id="43329-122">The following illustration shows the tabbed text.</span></span>

![Ilustración de un rectángulo que contiene cuatro columnas de texto; cada columna se alinea a la izquierda](images/fontstext4.png)

<span data-ttu-id="43329-124">En el código anterior se pasan tres argumentos al método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) .</span><span class="sxs-lookup"><span data-stu-id="43329-124">The preceding code passes three arguments to the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method.</span></span> <span data-ttu-id="43329-125">El tercer argumento es la dirección de una matriz que contiene los desplazamientos de tabulación.</span><span class="sxs-lookup"><span data-stu-id="43329-125">The third argument is the address of an array containing the tab offsets.</span></span> <span data-ttu-id="43329-126">El segundo argumento indica que hay tres desplazamientos en esa matriz.</span><span class="sxs-lookup"><span data-stu-id="43329-126">The second argument indicates that there are three offsets in that array.</span></span> <span data-ttu-id="43329-127">El primer argumento pasado a **StringFormat:: SetTabStops** es 0, que indica que el primer desplazamiento de la matriz se mide desde la posición 0, el borde izquierdo del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="43329-127">The first argument passed to **StringFormat::SetTabStops** is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>

## <a name="drawing-vertical-text"></a><span data-ttu-id="43329-128">Dibujo de texto vertical</span><span class="sxs-lookup"><span data-stu-id="43329-128">Drawing Vertical Text</span></span>

<span data-ttu-id="43329-129">Puede usar un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) para especificar que el texto se dibuje verticalmente en lugar de horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="43329-129">You can use a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object to specify that text be drawn vertically rather than horizontally.</span></span>

<span data-ttu-id="43329-130">En el ejemplo siguiente se pasa el valor [\* \* \* \* StringFormatFlagsDirectionVertical \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) al método [**StringFormat:: SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) de un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) .</span><span class="sxs-lookup"><span data-stu-id="43329-130">The following example passes the value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) to the [**StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object.</span></span> <span data-ttu-id="43329-131">La dirección de ese objeto **StringFormat** se pasa al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="43329-131">The address of that **StringFormat** object is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="43329-132">El valor [\* \* \* \* StringFormatFlagsDirectionVertical \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* es un elemento de la enumeración **StringFormatFlags** , que se declara en Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="43329-132">The value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) is an element of the **StringFormatFlags** enumeration, which is declared in Gdiplusenums.h.</span></span>


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



<span data-ttu-id="43329-133">En la ilustración siguiente se muestra el texto vertical.</span><span class="sxs-lookup"><span data-stu-id="43329-133">The following illustration shows the vertical text.</span></span>

![Ilustración que muestra una ventana que contiene el texto girado 90 grados en el sentido de las agujas del reloj](images/fontstext5.png)

 

 



