---
description: Una vez que una aplicación crea un controlador de dominio de pantalla o impresora, puede empezar a dibujar en el dispositivo asociado o, en el caso del controlador de dominio de memoria, puede empezar a dibujar en el mapa de bits almacenado en memoria.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Operaciones en objetos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0574b8527dbf83b4cb4a38163dcf7b33017336
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475911"
---
# <a name="operations-on-graphic-objects"></a>Operaciones en objetos gráficos

Una vez que una aplicación crea un controlador de dominio de pantalla o impresora, puede empezar a dibujar en el dispositivo asociado o, en el caso del controlador de dominio de memoria, puede empezar a dibujar en el mapa de bits almacenado en memoria. Sin embargo, antes de que comience el dibujo, y a veces mientras el dibujo está en curso, a menudo es necesario reemplazar los objetos predeterminados por objetos nuevos.

Una aplicación puede examinar los atributos de un objeto predeterminado llamando a las [**funciones GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) [**y GetObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) La **función GetCurrentObject** devuelve un identificador que identifica el lápiz, el pincel, la paleta, el mapa de bits o la fuente actuales, y la función **GetObject** inicializa una estructura que contiene los atributos de ese objeto.

Algunas impresoras proporcionan lápices, pinceles y fuentes residentes que se pueden usar para mejorar la velocidad de dibujo en una aplicación. Se pueden usar dos funciones para enumerar estos objetos: [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) y [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa). Si la aplicación debe enumerar pinceles o lápices residentes, puede llamar a la función **EnumObjects** para examinar los atributos correspondientes. Si la aplicación debe enumerar las fuentes residentes, puede llamar a la función **EnumFontFamilies** (que también puede enumerar las fuentes GDI).

Una vez que una aplicación determina que un objeto predeterminado debe reemplazarse, crea un nuevo objeto mediante una llamada a una de las siguientes funciones de creación.



| Objeto gráfico | Función                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | [**CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateDiscardableBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| Pincel          | [**CreateBrushIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) [**CreateDIBPatternBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush) [**CreateDIBPatternBrushPt,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) [**CreateHatchBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush) [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush), [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| Paleta de colores  | [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Fuente           | [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta), [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Lápiz            | [**CreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect) [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| Region         | [**CreateVelopticRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn) [**CreateVelopticRgnIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) [**CreatePolygonRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn) [**CreatePolyPolygonRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn) [**CreateRectRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn) [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

Cada una de estas funciones devuelve un identificador que identifica un nuevo objeto. Una vez que una aplicación recupera un identificador, debe llamar a la [**función SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) para reemplazar el objeto predeterminado. Sin embargo, la aplicación debe guardar el identificador que identifica el objeto predeterminado y usar este identificador para reemplazar el nuevo objeto cuando ya no sea necesario. Cuando la aplicación termina de dibujar con el nuevo objeto, debe restaurar el objeto predeterminado llamando a la función **SelectObject** y, a continuación, eliminar el nuevo objeto llamando a [**la función DeleteObject.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) Si no se eliminan objetos, se produce un problema de rendimiento grave.

 

 



