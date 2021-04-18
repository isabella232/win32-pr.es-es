---
title: Espacios de color independientes del dispositivo
description: Al reconocer la necesidad de medidas de color estándar, independientes del dispositivo, la Comisión International de l'Eclairage (Comisión Internacional en iluminación) o CIE, creó un espacio de colores basado en \ 0034; imaginario \ 0034; colores primarios.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Sistema de color de Windows (WCS), espacios de colores independientes del dispositivo
- WCS (sistema de colores de Windows), espacios de colores independientes del dispositivo
- Administración del color de imagen, espacios de colores independientes del dispositivo
- Administración del color, espacios de colores independientes del dispositivo
- colores, espacios de colores independientes del dispositivo
- espacios de colores, independiente del dispositivo
- espacios de colores independientes del dispositivo
- Comisión International de l'Eclairage (CIE)
- Comisión Internacional de iluminación (CIE)
- CIE (Comisión International de l'Eclairage)
- CIE (Comisión Internacional sobre iluminación)
- Espacio de colores de CIEXYZ
- Espacio de colores XYZ
- espacio de color sRGB
- espacios de colores, CIEXYZ
- espacios de colores, sRGB
- espacios de colores, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721128"
---
# <a name="device-independent-color-spaces"></a>Espacios de color independientes del dispositivo

Al reconocer la necesidad de las medidas de color estándar, independientes del dispositivo, la Comisión International de l'Eclairage (Comisión Internacional sobre iluminación) o CIE, creó un [espacio de colores](c.md) basado en los [colores primarios](p.md)"imaginarios". No se espera que ningún dispositivo real genere colores en este espacio de colores. Se utiliza como medio para convertir colores de un espacio de colores a otro. Los colores primarios de este espacio de colores son los colores abstractos X, Y y Z.

El espacio de colores 1931 CIEXYZ se utiliza ampliamente como base para la conversión del espacio de colores. Con el aumento de Internet, sin embargo, las consideraciones de ancho de banda han hecho que el espacio de colores XYZ no sea manejable. El intercambio de imágenes sobre el ancho de banda limitado de Internet requiere un modelo de [color](c.md)más compacto.

Como resultado, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de colores RGB predefinido estándar conocido como sRGB, para permitir una administración de color precisa con muy poca sobrecarga de datos. Este estándar se ha aprobado como estándar internacional formal por el Comisión electrotécnica internacional (CEI) (IEC) como IEC 61966-2-1: sistemas multimedia y medida EquipmentColour y ManagementPart 2-1: el color ManagementDefault RGB de color. Está disponible directamente desde el IEC en <https://www.iec.ch/> . La información que describe los problemas técnicos implicados en sRGB está disponible en Internet en:

[Un espacio de colores predeterminado estándar para Internet-sRGB](https://www.w3.org/Graphics/Color/sRGB.html)

En la \\ carpeta ayuda de la referencia del programador de WCS 1,0 del SDK de la plataforma se encuentra disponible una versión de archivo de ayuda de una nota del producto en la que se describen los problemas técnicos relacionados con sRGB, sRGB. hlp.

Los distintos formatos de archivo pueden usar o agregar una marca para especificar que la imagen está en el espacio de color sRGB. En el formato de mapa de bits independiente del dispositivo (DIB) de Windows, al establecer el miembro **bV5CSType** de la estructura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) en LCS \_ sRGB, se especifica que los colores DIB están en el espacio de color sRGB.

 

 




