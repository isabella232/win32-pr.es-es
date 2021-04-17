---
title: Espacios de color CMY y CMYK
description: Los espacios de colores CMY y CMYK se suelen usar en la impresión en color. Un espacio de colores CMY usa cian, magenta y amarillo (CMY) como sus colores primarios. Rojo, verde y azul son los colores secundarios.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Sistema de color de Windows (WCS), espacios de colores CMY
- WCS (sistema de colores de Windows), espacios de colores CMY
- Administración del color de imagen, espacios de colores CMY
- Administración del color, espacios de colores CMY
- colores, espacios de colores CMY
- espacios de colores, CMY
- Espacios de colores CMY
- Sistema de color de Windows (WCS), espacios de color CMYK
- WCS (sistema de colores de Windows), espacios de color CMYK
- Administración del color de imagen, espacios de color CMYK
- Administración del color, espacios de CMYKcolor
- colores, espacios de color CMYK
- espacios de colores, CMYK
- Espacios de colores CMYK
- cyan
- magenta
- yellow
- Aguamarina fucsia amarillo (CMY)
- CMY (aguamarina fucsia amarillo)
- Aguamarina fucsia amarillo negro (CMYK)
- CMYK (aguamarina fucsia amarillo negro)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721107"
---
# <a name="cmy-and-cmyk-color-spaces"></a>Espacios de color CMY y CMYK

Los [espacios de colores](c.md) CMY y CMYK se suelen usar en la impresión en color. Un espacio de colores CMY usa cian, magenta y amarillo (CMY) como sus [colores primarios](p.md). Rojo, verde y azul son los colores secundarios.

Las siguientes figuras son representaciones de color del espacio de colores CMY. El espacio de colores CMY se normaliza.

![cubo de espacio de colores CMY en valores máximos](images/cmyclrs1.png)

![cubo de espacio de colores CMY con valores mínimos](images/cmyclrs2.png)

El espacio de colores CMY es sustractivo. Por lo tanto, el blanco está en (0,0, 0,0, 0,0) y el negro está en (1,0, 1,0, 1,0). Si empieza con blanco y no resta ningún color, obtendrá blanco. Si empieza por blanco y resta todos los colores por igual, obtendrá el color negro.

El espacio de colores CMYK es una variación del modelo CMY. Agrega negro (aguamarina, fucsia, amarillo y negro). El espacio de colores CMYK cierra el intervalo entre la teoría y la práctica. En teoría, no es necesario el componente negro extra. Sin embargo, la experiencia con varios tipos de tintas y documentos ha demostrado que cuando se mezclan los componentes iguales de las tintas cian, magenta y amarillo, el resultado suele ser oscuro marrón, no negro. La adición de una tinta negra a la mezcla soluciona este problema.

Los espacios de colores CMY y CMYK pueden ser independientes del dispositivo, pero normalmente se usan en referencia a un dispositivo específico.

 

 




