---
description: Windows GDI+ proporciona varios niveles de calidad para dibujar texto. Normalmente, una representación de mayor calidad tarda más tiempo de procesamiento que la representación de menor calidad.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Suavizado de contorno con texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9411206351340f58b63196ff880745743ad92325918b112ad2ddb5bcb8591e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249929"
---
# <a name="antialiasing-with-text"></a>Suavizado de contorno con texto

Windows GDI+ proporciona varios niveles de calidad para dibujar texto. Normalmente, una representación de mayor calidad tarda más tiempo de procesamiento que la representación de menor calidad.

El nivel de calidad es una propiedad de la [**clase Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Para establecer el nivel de calidad, llame al [**método Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) de un **objeto Graphics.** El **método Graphics::SetTextRenderingHint** recibe uno de los elementos de la enumeración [**TextRenderingHint,**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) que se declara en Gdiplusenums.h.

GDI+ proporciona suavizado de contorno tradicional y un nuevo tipo de suavizado de contorno basado en la tecnología de visualización ClearType de Microsoft solo disponible en Windows XP y Windows Server 2003 y versiones posteriores de Windows. El suavizado ClearType mejora la legibilidad en monitores DE COLOR DE COLOR que tienen una interfaz digital, como los monitores de los portátiles y las pantallas de escritorio plano de alta calidad. La legibilidad en las pantallas de CRT también se ha mejorado ligeramente.

ClearType depende de la orientación y el orden de las franjas de LAN. Actualmente, ClearType solo se implementa para franjas verticales ordenadas rgb. Esto puede ser un problema si usa un equipo de tableta, donde la pantalla se puede orientar en cualquier dirección, o si usa una pantalla que se puede convertir de horizontal a vertical.

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

![captura de pantalla de una cadena cuyos caracteres tienen bordes irregulares contrastados con uno con bordes suavizados](images/fontstext10.png)

 

 



