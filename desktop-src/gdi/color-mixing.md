---
description: La combinación de colores permite a una aplicación crear nuevos colores combinando el lápiz o el color del pincel con los colores de la imagen existente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Combinación de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1adde68360d7050e0cebb6e7d5ac073b36a3c18c3687990c1f2aea6a5719f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105734"
---
# <a name="color-mixing"></a>Combinación de colores

La combinación de colores permite a una aplicación crear nuevos colores combinando el lápiz o el color del pincel con los colores de la imagen existente. La aplicación puede elegir dibujar el lápiz o el color del pincel tal y como está (dibujando eficazmente sobre cualquier imagen existente) o mezclar el color con los colores ya presentes.

El modo de combinación de primer plano, a veces denominado operación de trama binaria, determina cómo se mezclan estos colores. Una aplicación puede combinar colores, conservando todos los componentes de ambos colores. enmascarar colores, quitar o moderar componentes que no son comunes; o enmascara exclusivamente los colores, quitando o moderando los componentes que son comunes. Hay varias variaciones en estas operaciones básicas de combinación.

La combinación de colores está sujeta a la aproximación de color. Si el resultado de la combinación de colores es un color que el dispositivo no puede generar, el sistema se aproxima al resultado, con un color que puede generar. Si una aplicación combina colores entrelazados, los colores individuales que se usan para crear el color entrelazado se mezclan y los resultados están sujetos a una aproximación de color.

Una aplicación establece el modo de combinación en primer plano mediante la función [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) y recupera el modo actual mediante la [**función GetROP2.**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)

Aunque hay un modo de combinación de fondo, ese modo no controla la combinación de colores. En su lugar, especifica si se usa un color de fondo al dibujar líneas con estilo, pinceles sombreados y texto.

 

 



