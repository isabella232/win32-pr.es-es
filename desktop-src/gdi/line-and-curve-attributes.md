---
description: Un contexto de dispositivo (DC) contiene atributos que afectan a la salida de línea y curva. Los atributos de línea y curva incluyen la posición actual, el estilo de pincel, el color del pincel, el estilo del lápiz, el color del lápiz, la transformación, y así sucesivamente.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Atributos de línea y curva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5ab8758cf6e77b28568cacafd8c57312c052d9e9415211f034e3d1a70b6c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831615"
---
# <a name="line-and-curve-attributes"></a>Atributos de línea y curva

Un contexto de dispositivo (DC) contiene atributos que afectan a la salida de línea y curva. Los *atributos de línea y curva* incluyen la posición actual, el estilo de pincel, el color del pincel, el estilo del lápiz, el color del lápiz, la transformación, y así sucesivamente.

La posición actual predeterminada de cualquier controlador de dominio se encuentra en el punto (0,0) en el espacio lógico (o mundo). Puede establecer estas coordenadas en una nueva posición llamando a la [**función MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) y pasando un nuevo conjunto de coordenadas.

> [!Note]  
> Hay dos conjuntos de funciones de dibujo de línea y curva. El primer conjunto conserva la posición actual en un controlador de dominio y el segundo conjunto modifica la posición. Puede identificar las funciones que modifican la posición actual examinando el nombre de la función. Si el nombre de la función termina con la preposición "To", la función establece la posición actual en el punto final de la última línea dibujada [**(LineTo,**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) [**ArcTo,**](/windows/desktop/api/Wingdi/nf-wingdi-arcto) [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)o [**PolyBezierTo).**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto) Si el nombre de la función no termina con esta preposición, deja intacta la posición actual [**(Arc,**](/windows/desktop/api/Wingdi/nf-wingdi-arc) [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)o [**PolyBezier).**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)

 

El pincel predeterminado es un pincel blanco sólido. Una aplicación puede crear un pincel mediante una llamada a la [**función CreateBrushIndirect.**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) Después de crear un pincel, la aplicación puede seleccionarlo en su controlador de dominio llamando a la [**función SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Windows proporciona un conjunto completo de funciones para crear, seleccionar y modificar el pincel en el controlador de dominio de una aplicación. Para obtener más información sobre estas funciones y sobre los pinceles en general, vea [Pinceles](brushes.md).

El lápiz predeterminado es un lápiz negro sólido y con un píxel de ancho. Una aplicación puede crear un lápiz mediante la [**función ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Después de crear un lápiz, la aplicación puede seleccionarlo en su controlador de dominio llamando a la [**función SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Windows proporciona un conjunto completo de funciones para crear, seleccionar y modificar el lápiz en el controlador de dominio de una aplicación. Para obtener más información sobre estas funciones y sobre los lápices en general, vea [Lápices](pens.md).

La transformación predeterminada es la transformación de Unity (especificada por la matriz de identidades). Una aplicación puede especificar una nueva transformación llamando a la [**función SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) Windows proporciona un conjunto completo de funciones para transformar líneas y curvas modificando su ancho, ubicación y apariencia general. Para obtener más información sobre estas funciones, vea [Espacios de coordenadas y transformaciones.](coordinate-spaces-and-transformations.md)

 

 



