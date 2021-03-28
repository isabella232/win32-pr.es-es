---
description: Windows GDI+ proporciona varios niveles de calidad para dibujar texto. Normalmente, la representación de mayor calidad requiere más tiempo de procesamiento que la representación de menor calidad.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Suavizado de contorno con texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997597"
---
# <a name="antialiasing-with-text"></a><span data-ttu-id="f920f-104">Suavizado de contorno con texto</span><span class="sxs-lookup"><span data-stu-id="f920f-104">Antialiasing with Text</span></span>

<span data-ttu-id="f920f-105">Windows GDI+ proporciona varios niveles de calidad para dibujar texto.</span><span class="sxs-lookup"><span data-stu-id="f920f-105">Windows GDI+ provides various quality levels for drawing text.</span></span> <span data-ttu-id="f920f-106">Normalmente, la representación de mayor calidad requiere más tiempo de procesamiento que la representación de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="f920f-106">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span>

<span data-ttu-id="f920f-107">El nivel de calidad es una propiedad de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f920f-107">The quality level is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="f920f-108">Para establecer el nivel de calidad, llame al método [**Graphics:: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) de un objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="f920f-108">To set the quality level, call the [**Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method of a **Graphics** object.</span></span> <span data-ttu-id="f920f-109">El método **Graphics:: SetTextRenderingHint** recibe uno de los elementos de la enumeración [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , que se declara en Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="f920f-109">The **Graphics::SetTextRenderingHint** method receives one of the elements of the [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="f920f-110">GDI+ proporciona suavizado de contorno tradicional y un nuevo tipo de suavizado de contorno basado en la tecnología de visualización de ClearType de Microsoft solo disponible en Windows XP y Windows Server 2003 y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="f920f-110">GDI+ provides traditional antialiasing and a new kind of antialiasing based on Microsoft ClearType display technology only available on Windows XP and Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="f920f-111">El suavizado de ClearType mejora la legibilidad en monitores LCD de color que tienen una interfaz digital, como los monitores de portátiles y las pantallas de escritorio plano de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="f920f-111">ClearType smoothing improves readability on color LCD monitors that have a digital interface, such as the monitors in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="f920f-112">La legibilidad en pantallas de CRT también se ha mejorado en cierto modo.</span><span class="sxs-lookup"><span data-stu-id="f920f-112">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="f920f-113">ClearType depende de la orientación y el orden de las franjas LCD.</span><span class="sxs-lookup"><span data-stu-id="f920f-113">ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="f920f-114">Actualmente, ClearType solo se implementa para las franjas verticales que se ordenan por RGB.</span><span class="sxs-lookup"><span data-stu-id="f920f-114">Currently, ClearType is implemented only for vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="f920f-115">Esto puede ser un problema si se usa un Tablet PC, donde la pantalla se puede orientar en cualquier dirección o si se usa una pantalla que se puede convertir horizontalmente a vertical.</span><span class="sxs-lookup"><span data-stu-id="f920f-115">This might be a concern if you are using a tablet PC, where the display can be oriented in any direction, or if you are using a screen that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="f920f-116">En el ejemplo siguiente se dibuja texto con dos configuraciones de calidad diferentes:</span><span class="sxs-lookup"><span data-stu-id="f920f-116">The following example draws text with two different quality settings:</span></span>


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



<span data-ttu-id="f920f-117">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="f920f-117">The following illustration shows the output of the preceding code.</span></span>

![captura de pantalla de una cadena cuyos caracteres tienen bordes irregulares en contraste con uno con bordes suaves](images/fontstext10.png)

 

 



