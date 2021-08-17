---
description: Puede rellenar una ruta de acceso pasando la dirección de un objeto GraphicsPath al método Graphics::FillPath.
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Rellenar cifras abiertas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198a1a9e3a3cffa6aa5c0f3627c1415a54c8842c9f90a2ebdd6ebc2a9e0f3fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977545"
---
# <a name="filling-open-figures"></a>Rellenar cifras abiertas

Puede rellenar una ruta de acceso pasando la dirección de un [**objeto GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) al [**método Graphics::FillPath.**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) El **método Graphics::FillPath** rellena la ruta de acceso según el modo de relleno (alternativo o de sinuoso) establecido actualmente para la ruta de acceso. Si la ruta de acceso tiene alguna figura abierta, la ruta de acceso se rellena como si esas figuras estuvieran cerradas. GDI+ cierra una figura dibujando una línea recta desde su punto final hasta su punto inicial.

En el ejemplo siguiente se crea una ruta de acceso que tiene una figura abierta (un arco) y una figura cerrada (una elipse). El [**método Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) rellena la ruta de acceso según el modo de relleno predeterminado, que es FillModeAlternate.


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



En la ilustración siguiente se muestra la salida del código anterior. Tenga en cuenta que la ruta de acceso se rellena (según FillModeAlternate) como si la ilustración abierta se hubiera cerrado mediante una línea recta desde su punto final hasta su punto inicial.

![ilustración que muestra una elipse alta que se superpone a la mitad inferior de una elipse ancha; la unión se rellena, pero la intersección está vacía](images/fillopenpath.png)

 

 



