---
description: La combinación de colores permite a una aplicación crear nuevos colores combinando el color del lápiz o del pincel con los colores de la imagen existente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Combinación de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155660"
---
# <a name="color-mixing"></a>Combinación de colores

La combinación de colores permite a una aplicación crear nuevos colores combinando el color del lápiz o del pincel con los colores de la imagen existente. La aplicación puede elegir entre dibujar el color del lápiz o del pincel tal como está (dibujando de forma eficaz sobre cualquier imagen existente) o mezclar el color con los colores ya presentes.

El modo de combinación de primer plano, que a veces se denomina operación de trama binaria, determina cómo se mezclan estos colores. Una aplicación puede combinar colores, conservando todos los componentes de ambos colores; enmascarar colores, quitar o moderar componentes que no son comunes; o bien, desenmascarar los colores de forma exclusiva, quitar o moderar los componentes que son comunes. Hay varias variaciones en estas operaciones básicas de mezcla.

La combinación de colores está sujeta a la aproximación del color. Si el resultado de la combinación de colores es un color que el dispositivo no puede generar, el sistema aproxima el resultado, con un color que puede generar. Si una aplicación mezcla colores propuestos, se mezclan los colores individuales que se usan para crear el color dipuesto, y los resultados están sujetos a la aproximación del color.

Una aplicación establece el modo de combinación de primer plano mediante la función [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) y recupera el modo actual mediante la función [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .

Aunque hay un modo de combinación en segundo plano, ese modo no controla la combinación de colores. En su lugar, especifica si se usa un color de fondo al dibujar líneas con estilo, pinceles tramados y texto.

 

 



