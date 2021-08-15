---
description: 'En la ilustración siguiente se muestran dos curvas: una abierta y otra cerrada.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Curvas abiertas y cerradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383f7c68909a73291c00c6e760d1cc6554b061d5749b33e6e90ba3a986c71906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885130"
---
# <a name="open-and-closed-curves"></a>Curvas abiertas y cerradas

En la ilustración siguiente se muestran dos curvas: una abierta y otra cerrada.

![ilustración de una curva abierta (una línea curva) y una curva cerrada (el contorno de una forma)](images/aboutgdip02-art24.png)

Las curvas cerradas tienen un interior y, por tanto, se pueden rellenar con un pincel. La clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) de Windows GDI+ proporciona los métodos siguientes para rellenar las figuras y curvas cerradas: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillDevpse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)y [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). Siempre que llame a uno de estos métodos, debe pasar la dirección de uno de los tipos de pincel específicos [**(SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)o [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) como argumento.

El [método FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) es un complemento del [método DrawAsync.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) Al igual que el método DrawMap dibuja una parte del contorno de una elipse, el método FillPie rellena una parte del interior de una elipse. En el ejemplo siguiente se dibuja un arco y se rellena la parte correspondiente del interior de la elipse.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



En la ilustración siguiente se muestra el arco y el circular relleno.

![ilustración que muestra un segmento de una elipse rellena](images/aboutgdip02-art25.png)

El [método FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) es un complemento del [método DrawClosedCurve.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) Ambos métodos cierran automáticamente la curva conectando el punto final al punto inicial. En el ejemplo siguiente se dibuja una curva que pasa a través de (0, 0), (60, 20) y (40, 50). A continuación, la curva se cierra automáticamente conectando (40, 50) al punto inicial (0, 0) y el interior se rellena con un color sólido.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Una ruta de acceso puede constar de varias figuras (subtrataciones). El [**método Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) rellena el interior de cada ilustración. Si no se cierra una figura, el método **Graphics::FillPath** rellena el área que se incluiría si se cerrara la figura. En el ejemplo siguiente se dibuja y rellena una ruta de acceso que consta de un arco, una spline cardinal, una cadena y un gráfico circular.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



En la ilustración siguiente se muestra la ruta de acceso antes y después de rellenarse con un pincel sólido. Tenga en cuenta que el texto de la cadena se describe, pero no se rellena, mediante el [**método Graphics::D rawPath.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) Es el método [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) el que pinta los interiores de los caracteres de la cadena.

![ilustración que muestra dos veces texto y una curva abierta y cerrada; están vacías la primera vez y se rellenan la segunda vez.](images/aboutgdip02-art26.png)

 

 



