---
description: Una curva normal es un conjunto de píxeles resaltados en una pantalla de trama (o puntos en una página impresa) que definen el perímetro (o parte del perímetro) de una sección cónica.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed6b7c0f6ad03a9ebe16dcffe85694397f6127ff15c2d9d3a9e68f79257a0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452245"
---
# <a name="curves"></a>Curvas

Una curva normal es un conjunto de píxeles resaltados en una pantalla de trama (o puntos en una página impresa) que definen el perímetro (o parte del perímetro) de una sección cónica. Una curva irregular es un conjunto de píxeles que definen una curva que no se ajusta al perímetro de una sección cónica. El punto final se excluye de una curva igual que se excluye de una línea.

Cuando una aplicación llama a una de las funciones de dibujo de curvas, GDI divide la curva en una serie de segmentos de línea discretos y extremadamente pequeños. Después de determinar los puntos de conexión (punto inicial y punto final) para cada uno de estos segmentos de línea, GDI determina qué píxeles (o puntos) definen cada línea aplicando su DDA.

Una aplicación puede dibujar una elipse o parte de una elipse llamando a la [**función Arc.**](/windows/desktop/api/Wingdi/nf-wingdi-arc) Esta función dibuja la curva dentro del perímetro de un rectángulo invisible denominado rectángulo delimitador. El tamaño de la elipse se especifica mediante dos radiales invisibles que se extienden desde el centro del rectángulo hasta los lados del rectángulo. En la ilustración siguiente se muestra un arco (parte de una elipse) dibujado mediante la **función Arc.**

![diagrama que muestra un arco que representa tres cuartos de un círculo completo](images/cslcv-03.png)

Al llamar a [**la función Arc,**](/windows/desktop/api/Wingdi/nf-wingdi-arc) una aplicación especifica las coordenadas del rectángulo delimitador y los radiales. En la ilustración anterior se muestra el rectángulo y los radiales con líneas discontinuas mientras el arco real se dibujaba con una línea sólida.

Al dibujar el arco de otro objeto, la aplicación puede llamar a las funciones [**SetErrorDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) y [**GetErrorDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) para controlar la dirección (en el sentido de las agujas del reloj o en el sentido contrario a las agujas del reloj) en la que se dibuja el objeto. La dirección predeterminada para dibujar arcos y otros objetos es en sentido contrario a las agujas del reloj.

Además de dibujar elipses o partes de elipses, las aplicaciones pueden dibujar curvas irregulares llamadas curvas de Bézier. Una *curva bézier* es una curva irregular cuya curvación se define mediante cuatro puntos de control (p1, p2, p3 y p4). Los puntos de control p1 y p4 definen los puntos inicial y final de la curva, y los puntos de control p2 y p3 definen la forma de la curva marcando los puntos donde la curva invierte la orientación, como se muestra en el diagrama siguiente.

![ilustración que muestra dos curvas bézier, cada una entre un punto inicial y final, y cada una con dos puntos de control](images/cslcv-04.png)

Una aplicación puede dibujar curvas irregulares llamando a [**la función PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) y suministrando los puntos de control adecuados.

 

 



