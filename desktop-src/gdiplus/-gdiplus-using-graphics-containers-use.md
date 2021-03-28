---
description: Un objeto Graphics proporciona métodos como DrawLine, DrawImage y DrawString para mostrar imágenes vectoriales, imágenes de trama y texto.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Utilizar contenedores de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985114"
---
# <a name="using-graphics-containers"></a>Utilizar contenedores de gráficos

Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona métodos como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))y [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) para mostrar imágenes vectoriales, imágenes de trama y texto. Un objeto **Graphics** también tiene varias propiedades que influyen en la calidad y la orientación de los elementos que se dibujan. Por ejemplo, la propiedad modo de suavizado determina si se aplica el suavizado de contorno a las líneas y las curvas, y la propiedad de transformación universal influye en la posición y la rotación de los elementos que se dibujan.

Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) suele estar asociado a un dispositivo de presentación determinado. Cuando se usa un objeto **Graphics** para dibujar en una ventana, el objeto **Graphics** también está asociado a esa ventana concreta.

Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) puede considerarse como un contenedor porque contiene un conjunto de propiedades que influyen en el dibujo y se vincula a información específica del dispositivo. Puede crear un contenedor secundario dentro de un objeto **Graphics** existente llamando al método [BeginContainer](/previous-versions//ms535731(v=vs.85)) de ese objeto **Graphics** .

En los temas siguientes se tratan los objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y los contenedores anidados con más detalle:

-   [Estado de un objeto de gráficos](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Contenedores de gráficos anidados](-gdiplus-nested-graphics-containers-use.md)

 

 
