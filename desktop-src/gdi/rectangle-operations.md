---
description: La función SetRect crea un rectángulo, la función CopyRect realiza una copia de un rectángulo determinado y la función SetRectEmpty crea un rectángulo vacío.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operaciones de rectángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360527"
---
# <a name="rectangle-operations"></a>Operaciones de rectángulo

La función [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crea un rectángulo, la función [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) realiza una copia de un rectángulo determinado y la función [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crea un rectángulo vacío. Un rectángulo vacío es cualquier rectángulo que tenga un ancho de cero, un alto de cero o ambos. La función [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina si un rectángulo determinado está vacío. La función [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina si dos rectángulos son idénticos, es decir, si tienen las mismas coordenadas.

La función [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta o disminuye el ancho o el alto de un rectángulo, o ambos. Puede Agregar o quitar el ancho de ambos extremos del rectángulo; puede Agregar o quitar el alto de la parte superior e inferior del rectángulo.

La función [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) mueve un rectángulo en una cantidad determinada. Mueve el rectángulo agregando las cifras x-amount, y amount, o x-e y-amount especificadas a las coordenadas de la esquina.

La función [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina si un punto determinado se encuentra dentro de un rectángulo determinado. El punto está en el rectángulo si se encuentra en el lado izquierdo o superior o está completamente dentro del rectángulo. El punto no está en el rectángulo si se encuentra en el lado derecho o en el inferior.

La función [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crea un nuevo rectángulo que es la intersección de dos rectángulos existentes, tal como se muestra en la ilustración siguiente.

![Ilustración que muestra dos rectángulos superpuestos, con un sombreado más oscuro para indicar la intersección ](images/csrec-01.png)

La función [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crea un nuevo rectángulo que es la Unión de dos rectángulos existentes, tal como se muestra en la ilustración siguiente.

![Ilustración de dos rectángulos superpuestos, con un sombreado más oscuro que indica áreas dentro de la Unión, pero no dentro de un rectángulo](images/csrec-02.png)

Para obtener información sobre las funciones que dibujan elipses y polígonos, vea [formas rellenas](filled-shapes.md).

 

 



