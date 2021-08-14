---
description: Una región es una parte de la superficie de presentación.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Regiones (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd15a7a25b341556b312c540f6fa4caf870da75aa4973be1d7c1e8102511e6ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885038"
---
# <a name="regions-gdi"></a>Regiones (GDI+)

Una región es una parte de la superficie de presentación. Las regiones pueden ser simples (un rectángulo único) o complejas (una combinación de polígonos y curvas cerradas). En la ilustración siguiente se muestran dos regiones: una construida a partir de un rectángulo y la otra construida a partir de un trazado.

![ilustración que muestra una región rectangular transparente superpuesta a una forma curva opaca](images/aboutgdip02-art27.png)

Las regiones se usan a menudo para el recorte y las pruebas de impacto. El recorte implica restringir el dibujo a una determinada región de la pantalla, normalmente la parte de la pantalla que debe actualizarse. Las pruebas de acceso implican comprobar si el cursor está en una determinada región de la pantalla cuando se presiona un botón del mouse.

Puede construir una región a partir de un rectángulo o de un trazado. También puede crear regiones complejas combinando las regiones existentes. La [**clase Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) proporciona los métodos siguientes para combinar regiones: [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [Xor,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))y [**Region::Complement.**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath))

La intersección de dos regiones es el conjunto de todos los puntos que pertenecen a ambas regiones. La unión es el conjunto de todos los puntos que pertenecen a una u otra región o a ambas regiones. El complemento de una región es el conjunto de todos los puntos que no están en la región. En la ilustración siguiente se muestra la intersección y la unión de las dos regiones de la ilustración anterior.

![ilustración que muestra la intersección de las regiones de la ilustración anterior y su intersección](images/aboutgdip02-art28.png)

El [método Xor,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) aplicado a un par de regiones, genera una región que contiene todos los puntos que pertenecen a una región u otra, pero no a ambos. El [método Exclude,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) aplicado a un par de regiones, genera una región que contiene todos los puntos de la primera región que no están en la segunda región. En la ilustración siguiente se muestran las regiones resultantes de aplicar los métodos Xor y Exclude a las dos regiones que se muestran al principio de este tema.

![ilustración en la que se muestran las partes de cualquiera de las regiones, pero no ambas, y la parte del rectángulo que no se superpone a la región curva](images/aboutgdip02-art29.png)

Para rellenar una región, necesita un objeto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un [**objeto Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) y un [**objeto Region.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) El **objeto Graphics** proporciona el método [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) y el objeto **Brush** almacena los atributos del relleno, como el color o el patrón. En el ejemplo siguiente se rellena una región con un color sólido.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
