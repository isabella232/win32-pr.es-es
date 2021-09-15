---
description: La función SetRect crea un rectángulo, la función CopyRect realiza una copia de un rectángulo determinado y la función SetRectEmpty crea un rectángulo vacío.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operaciones de rectángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465729"
---
# <a name="rectangle-operations"></a>Operaciones de rectángulo

La [**función SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crea un rectángulo, la función [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) realiza una copia de un rectángulo determinado y la [**función SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crea un rectángulo vacío. Un rectángulo vacío es cualquier rectángulo que tenga ancho cero, alto cero o ambos. La [**función IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina si un rectángulo determinado está vacío. La [**función EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina si dos rectángulos son idénticos, es decir, si tienen las mismas coordenadas.

La [**función InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta o disminuye el ancho o alto de un rectángulo, o ambos. Puede agregar o quitar el ancho de ambos extremos del rectángulo; puede agregar o quitar el alto de la parte superior e inferior del rectángulo.

La [**función OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) mueve un rectángulo en una cantidad determinada. Mueve el rectángulo agregando las cantidades x, y o x e y dadas a las coordenadas de la esquina.

La [**función PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina si un punto determinado se encuentra dentro de un rectángulo determinado. El punto está en el rectángulo si se encuentra en el lado izquierdo o superior o está completamente dentro del rectángulo. El punto no está en el rectángulo si se encuentra en el lado derecho o inferior.

La [**función IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crea un nuevo rectángulo que es la intersección de dos rectángulos existentes, como se muestra en la ilustración siguiente.

![ilustración que muestra dos rectángulos superpuestos, con sombreado más oscuro para indicar la intersección ](images/csrec-01.png)

La [**función UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crea un nuevo rectángulo que es la unión de dos rectángulos existentes, como se muestra en la ilustración siguiente.

![ilustración de dos rectángulos superpuestos, con sombreado más oscuro que indica áreas dentro de la unión, pero no dentro de ninguno de los rectángulos](images/csrec-02.png)

Para obtener información sobre las funciones que dibujan puntos suspensivos y polígonos, vea [Formas rellenadas.](filled-shapes.md)

 

 



