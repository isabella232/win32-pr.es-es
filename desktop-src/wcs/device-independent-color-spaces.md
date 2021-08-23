---
title: Espacios de color independientes del dispositivo
description: Al reconocer la necesidad de medidas de color estándar independientes del dispositivo, la Comisión Internacional de l'Eclairage (International Commission on Measurement) o CIE creó un espacio de colores basado en \ 0034;imaginario \ 0034; colores primarios.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Sistema de colores (WCS), espacios de color independientes del dispositivo
- WCS (Windows de colores), espacios de color independientes del dispositivo
- administración de colores de imagen, espacios de color independientes del dispositivo
- administración de colores, espacios de color independientes del dispositivo
- colores, espacios de colores independientes del dispositivo
- espacios de colores, independiente del dispositivo
- espacios de colores independientes del dispositivo
- Commission International de l'Eclairage (CIE)
- Comisión internacional de iluminación (CIE)
- CIE (Commission International de l'Eclairage)
- CIE (Comisión Internacional de Iluminación)
- Espacio de colores CIEXYZ
- Espacio de colores XYZ
- espacio de colores sRGB
- espacios de colores, CIEXYZ
- espacios de colores, sRGB
- espacios de colores,XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c350ca4aa4b046d35926cd7568c4fbdfe030b7d7c13b085b9f3837c5dd8418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028793"
---
# <a name="device-independent-color-spaces"></a>Espacios de color independientes del dispositivo

Al reconocer la necesidad de medidas de color estándar independientes del dispositivo, la Comisión Internacional de l'Eclairage (International Commission on Measurement) o CIE creó un espacio de [colores](c.md) basado en colores primarios "imaginarios". [](p.md) No se espera que ningún dispositivo real produzca colores en este espacio de colores. Se usa como un medio para convertir colores de un espacio de colores a otro. Los colores principales de este espacio de colores son los colores abstractos X, Y y Z.

El espacio de colores CIEXYZ 1931 se usa ampliamente como base para la conversión del espacio de colores. Sin embargo, con el aumento de Internet, las consideraciones sobre el ancho de banda han hecho que el espacio de color XYZ sea difícil de manejar. El intercambio de imágenes a través del ancho de banda limitado de Internet requiere un modelo [de color más compacto.](c.md)

Como resultado, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de color RGB predefinido estándar conocido como sRGB, para permitir la administración precisa del color con muy poca sobrecarga de datos. Este estándar se ha aprobado como un estándar internacional formal por el Comisión electrotécnica internacional (CEI) (IEC) como IEC 61966-2-1: Sistemas multimedia y Equipos Medición y administración de la claseColourPart 2-1: Administración de unidades de producciónDefault RGB Space. Está disponible directamente desde iec en <https://www.iec.ch/> . La información sobre los problemas técnicos implicados en sRGB está disponible en Internet en:

[Un espacio de colores predeterminado estándar para Internet: sRGB](https://www.w3.org/Graphics/Color/sRGB.html)

Hay disponible una versión del archivo de ayuda de un documento técnico que describe los problemas técnicos implicados en sRGB, sRGB.HLP, en la carpeta Ayuda de la referencia del programador de WCS 1.0 en el SDK de \\ plataforma.

Diferentes formatos de archivo pueden usar o agregar una marca para especificar que la imagen está en un espacio de colores sRGB. En el formato de mapa de bits independiente del dispositivo (DIB) de Windows, al establecer el miembro **bV5CSType** de la estructura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) en LCS sRGB se especifica que los colores DIB están en el espacio de \_ colores sRGB.

 

 




