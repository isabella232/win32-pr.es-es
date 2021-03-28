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
# <a name="antialiasing-with-text"></a>Suavizado de contorno con texto

Windows GDI+ proporciona varios niveles de calidad para dibujar texto. Normalmente, la representación de mayor calidad requiere más tiempo de procesamiento que la representación de menor calidad.

El nivel de calidad es una propiedad de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Para establecer el nivel de calidad, llame al método [**Graphics:: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) de un objeto **Graphics** . El método **Graphics:: SetTextRenderingHint** recibe uno de los elementos de la enumeración [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , que se declara en Gdiplusenums. h.

GDI+ proporciona suavizado de contorno tradicional y un nuevo tipo de suavizado de contorno basado en la tecnología de visualización de ClearType de Microsoft solo disponible en Windows XP y Windows Server 2003 y versiones posteriores de Windows. El suavizado de ClearType mejora la legibilidad en monitores LCD de color que tienen una interfaz digital, como los monitores de portátiles y las pantallas de escritorio plano de alta calidad. La legibilidad en pantallas de CRT también se ha mejorado en cierto modo.

ClearType depende de la orientación y el orden de las franjas LCD. Actualmente, ClearType solo se implementa para las franjas verticales que se ordenan por RGB. Esto puede ser un problema si se usa un Tablet PC, donde la pantalla se puede orientar en cualquier dirección o si se usa una pantalla que se puede convertir horizontalmente a vertical.

En el ejemplo siguiente se dibuja texto con dos configuraciones de calidad diferentes:


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



En la ilustración siguiente se muestra la salida del código anterior.

![captura de pantalla de una cadena cuyos caracteres tienen bordes irregulares en contraste con uno con bordes suaves](images/fontstext10.png)

 

 



