---
description: En el tema dibujar una línea se muestra cómo escribir una aplicación de Windows que usa Windows GDI+ para dibujar una línea.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Dibujo de una cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276395"
---
# <a name="drawing-a-string"></a><span data-ttu-id="0cf05-103">Dibujo de una cadena</span><span class="sxs-lookup"><span data-stu-id="0cf05-103">Drawing a String</span></span>

<span data-ttu-id="0cf05-104">En el tema [dibujar una línea](-gdiplus-drawing-a-line-use.md) se muestra cómo escribir una aplicación de Windows que usa Windows GDI+ para dibujar una línea.</span><span class="sxs-lookup"><span data-stu-id="0cf05-104">The topic [Drawing a Line](-gdiplus-drawing-a-line-use.md) shows how to write a Windows application that uses Windows GDI+ to draw a line.</span></span> <span data-ttu-id="0cf05-105">Para dibujar una cadena, reemplace la función **OnPaint** que se muestra en ese tema por la siguiente función **OnPaint** :</span><span class="sxs-lookup"><span data-stu-id="0cf05-105">To draw a string, replace the **OnPaint** function shown in that topic with the following **OnPaint** function:</span></span>


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



<span data-ttu-id="0cf05-106">El código anterior crea varios objetos GDI+.</span><span class="sxs-lookup"><span data-stu-id="0cf05-106">The previous code creates several GDI+ objects.</span></span> <span data-ttu-id="0cf05-107">El objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona el método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , que realiza el dibujo real.</span><span class="sxs-lookup"><span data-stu-id="0cf05-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method, which does the actual drawing.</span></span> <span data-ttu-id="0cf05-108">El objeto [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) especifica el color de la cadena.</span><span class="sxs-lookup"><span data-stu-id="0cf05-108">The [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object specifies the color of the string.</span></span>

<span data-ttu-id="0cf05-109">El constructor [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recibe un único argumento de cadena que identifica la familia de fuentes.</span><span class="sxs-lookup"><span data-stu-id="0cf05-109">The [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a single, string argument that identifies the font family.</span></span> <span data-ttu-id="0cf05-110">La dirección del objeto **FontFamily** es el primer argumento que se pasa al constructor [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="0cf05-110">The address of the **FontFamily** object is the first argument passed to the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="0cf05-111">El segundo argumento pasado al constructor [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) especifica el tamaño de fuente y el tercer argumento especifica el estilo.</span><span class="sxs-lookup"><span data-stu-id="0cf05-111">The second argument passed to the [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) constructor specifies the font size, and the third argument specifies the style.</span></span> <span data-ttu-id="0cf05-112">El valor **FontStyleRegular** es un miembro de la enumeración [**fontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que se declara en Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="0cf05-112">The value **FontStyleRegular** is a member of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span> <span data-ttu-id="0cf05-113">El último argumento del constructor de **fuente** indica que el tamaño de la fuente (en este caso, 24 en este caso) se mide en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0cf05-113">The last argument to the **Font** constructor indicates that the size of the font (24 in this case) is measured in pixels.</span></span> <span data-ttu-id="0cf05-114">El valor **UnitPixel** es un miembro de la enumeración [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .</span><span class="sxs-lookup"><span data-stu-id="0cf05-114">The value **UnitPixel** is a member of the [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) enumeration.</span></span>

<span data-ttu-id="0cf05-115">El primer argumento que se pasa al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) es la dirección de una cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="0cf05-115">The first argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method is the address of a wide-character string.</span></span> <span data-ttu-id="0cf05-116">El segundo argumento,-1, especifica que la cadena está terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="0cf05-116">The second argument, –1, specifies that the string is null terminated.</span></span> <span data-ttu-id="0cf05-117">(Si la cadena no termina en null, el segundo argumento debe especificar el número de caracteres anchos de la cadena). El tercer argumento es la dirección del objeto de [**fuente**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="0cf05-117">(If the string is not null terminated, the second argument should specify the number of wide characters in the string.) The third argument is the address of the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="0cf05-118">El cuarto argumento es una referencia a un objeto de [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) que especifica la ubicación donde se dibujará la cadena.</span><span class="sxs-lookup"><span data-stu-id="0cf05-118">The fourth argument is a reference to a [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) object that specifies the location where the string will be drawn.</span></span> <span data-ttu-id="0cf05-119">El último argumento es la dirección del objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , que especifica el color de la cadena.</span><span class="sxs-lookup"><span data-stu-id="0cf05-119">The last argument is the address of the [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, which specifies the color of the string.</span></span>

 

 
