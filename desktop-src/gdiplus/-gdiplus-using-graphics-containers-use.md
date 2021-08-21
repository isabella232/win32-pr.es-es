---
description: Un objeto Graphics proporciona métodos como DrawLine, DrawImage y DrawString para mostrar imágenes vectoriales, imágenes de trama y texto.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Utilizar contenedores de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96292395113b80ec79f8b59d4ac7f203c3d1f2d892c2da62ce4957e49b81860d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036293"
---
# <a name="using-graphics-containers"></a>Utilizar contenedores de gráficos

Un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona métodos como [DrawLine,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))y [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) para mostrar imágenes vectoriales, imágenes de trama y texto. Un **objeto Graphics** también tiene varias propiedades que influyen en la calidad y la orientación de los elementos que se dibujan. Por ejemplo, la propiedad del modo de suavizado determina si el suavizado de contorno se aplica a líneas y curvas, y la propiedad de transformación del mundo influye en la posición y rotación de los elementos que se dibujan.

A [**menudo,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un objeto Graphics se asocia a un dispositivo de visualización determinado. Cuando se usa un **objeto Graphics** para dibujar en una ventana, el objeto **Graphics** también se asocia a esa ventana determinada.

Un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) se puede pensar en como un contenedor porque contiene un conjunto de propiedades que influyen en el dibujo y está vinculado a información específica del dispositivo. Puede crear un contenedor secundario dentro de un objeto **Graphics** existente llamando al [método BeginContainer](/previous-versions//ms535731(v=vs.85)) de ese **objeto Graphics.**

En los temas siguientes se tratan con más detalle los objetos [**Gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y los contenedores anidados:

-   [Estado de un objeto de gráficos](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Contenedores de gráficos anidados](-gdiplus-nested-graphics-containers-use.md)

 

 
