---
title: Espacios de color CMY y CMYK
description: Los espacios de colores CMY y OFFSET se usan a menudo en la impresión de colores. Un espacio de colores CMY usa el aguaz, elcolor y el amarillo (CMY) como colores principales. Rojo, verde y azul son los colores secundarios.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Sistema de colores (WCS), espacios de color CMY
- WCS (Windows de colores), espacios de color CMY
- administración de colores de imagen, espacios de color CMY
- administración de colores, espacios de colores CMY
- colors,CMY color spaces
- espacios de colores, CMY
- Espacios de colores CMY
- Windows Sistema de colores (WCS), espacios de color NTES
- WCS (Windows de colores), espacios de color NTES
- administración de colores de imagen, espacios de color COLOR
- administración de colores, espacios de color CMYK
- colores, espacios de colores COLOR
- espacios de colores, TIVOS
- Espacios de color TIVOS
- cyan
- magenta
- yellow
- yellow yellow (CMY)
- CMY (amarillo de agua nocródica)
- yellow black (LC)
- YELLOW (negro amarillo de cian)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcb1ea33bd32346dd541894342ec4af02274e4381eaf0c1925e2a4bc20e10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452109"
---
# <a name="cmy-and-cmyk-color-spaces"></a>Espacios de color CMY y CMYK

Los espacios de [colores](c.md) CMY y OFFSET se usan a menudo en la impresión de colores. Un espacio de colores CMY usa el aguaz, elcolor y el amarillo (CMY) como [colores principales.](p.md) Rojo, verde y azul son los colores secundarios.

Las siguientes figuras son representaciones de color del espacio de colores CMY. El espacio de colores CMY se normaliza.

![cubo de espacio de colores cmy con valores máximos](images/cmyclrs1.png)

![cubo de espacio de colores cmy con valores mínimos](images/cmyclrs2.png)

El espacio de colores CMY es resta. Por lo tanto, el blanco está en (0,0, 0,0, 0,0) y el negro en (1,0, 1,0, 1,0). Si empieza con blanco y no resta ningún color, obtiene el blanco. Si empieza con blanco y resta todos los colores por igual, se obtiene el negro.

El espacio de colores SPACE es una variación en el modelo CMY. Agrega negro (aguazco, rojo, amarillo y blacK). El espacio de color SPACE cierra la brecha entre la teoría y la práctica. En teoría, el componente negro adicional no es necesario. Sin embargo, la experiencia con distintos tipos de entrada de lápiz y papel ha demostrado que, cuando se mezclan los mismos componentes de la ez, el rojo y el amarillo, el resultado suele ser un color oscuro, no negro. La adición de lápiz negro a la combinación soluciona este problema.

Los espacios de colores CMY y VERSION pueden ser independientes del dispositivo, pero la mayoría de las veces se usan en referencia a un dispositivo específico.

 

 




