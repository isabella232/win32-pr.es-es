---
description: Un contexto de dispositivo (DC) contiene atributos que afectan a la salida de línea y de curva. Los atributos line y Curve incluyen la posición actual, el estilo de pincel, el color del pincel, el estilo del lápiz, el color de la pluma, la transformación, etc.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Atributos line y Curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ec13ea49a72447045c45ea2837ba40e64e6741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997341"
---
# <a name="line-and-curve-attributes"></a>Atributos line y Curve

Un contexto de dispositivo (DC) contiene atributos que afectan a la salida de línea y de curva. Los *atributos line y Curve* incluyen la posición actual, el estilo de pincel, el color del pincel, el estilo del lápiz, el color de la pluma, la transformación, etc.

La posición actual predeterminada de cualquier controlador de dominio se encuentra en el punto (0,0) en el espacio lógico (o del mundo). Puede establecer estas coordenadas en una nueva posición llamando a la función [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) y pasando un nuevo conjunto de coordenadas.

> [!Note]  
> Hay dos conjuntos de funciones de dibujo de líneas y curvas. El primer conjunto conserva la posición actual en un controlador de dominio y el segundo conjunto modifica la posición. Puede identificar las funciones que modifican la posición actual examinando el nombre de la función. Si el nombre de la función termina con la posición anterior "to", la función establece la posición actual en el punto final de la última línea dibujada ([**lineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto), [**Polilineto**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)o [**polibézierto**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)). Si el nombre de la función no termina con esta preposición, deja la posición actual intacta ([**arco**](/windows/desktop/api/Wingdi/nf-wingdi-arc), [**polilínea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)o [**polibézier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)).

 

El pincel predeterminado es un pincel blanco sólido. Una aplicación puede crear un nuevo pincel mediante una llamada a la función [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) . Después de crear un pincel, la aplicación puede seleccionarlo en su controlador de dominio mediante una llamada a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows proporciona un conjunto completo de funciones para crear, seleccionar y modificar el pincel en el controlador de dominio de una aplicación. Para obtener más información sobre estas funciones y sobre los pinceles en general, vea [pinceles](brushes.md).

El lápiz predeterminado es un lápiz negro estético y liso de un píxel de ancho. Una aplicación puede crear un lápiz mediante la función [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Después de crear un lápiz, la aplicación puede seleccionarlo en su controlador de dominio mediante una llamada a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows proporciona un conjunto completo de funciones para crear, seleccionar y modificar el lápiz en el controlador de dominio de una aplicación. Para obtener más información sobre estas funciones y sobre los lápices en general, consulte [PENS](pens.md).

La transformación predeterminada es la transformación Unity (especificada por la matriz de identidad). Una aplicación puede especificar una nueva transformación mediante una llamada a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) . Windows proporciona un conjunto completo de funciones para transformar líneas y curvas modificando el ancho, la ubicación y la apariencia general. Para obtener más información sobre estas funciones, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md).

 

 



