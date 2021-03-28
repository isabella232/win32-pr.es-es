---
description: Una aplicación puede recuperar las métricas de fuente de una fuente física solo después de que se haya seleccionado la fuente en un contexto de dispositivo.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Dispositivo frente a unidades de diseño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908496"
---
# <a name="device-vs-design-units"></a>Dispositivo frente a unidades de diseño

Una aplicación puede recuperar las métricas de fuente de una fuente física solo después de que se haya seleccionado la fuente en un contexto de dispositivo. Cuando se selecciona una fuente en un contexto de dispositivo, se escala para el dispositivo. Las métricas de fuente específicas del dispositivo se conocen como unidades de dispositivo.

Las métricas portátiles en fuentes se conocen como unidades de diseño. Para aplicar a un dispositivo especificado, las unidades de diseño deben convertirse en unidades de dispositivo. Utilice la siguiente fórmula para convertir las unidades de diseño en unidades de dispositivo.

*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*puntuación*/72) \* *DeviceResolution*

Las variables de esta fórmula tienen los significados siguientes.



| Variable           | Descripción                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DeviceUnits*      | Especifica la métrica de fuente *DesignUnits* convertida en unidades de dispositivo. Este valor se encuentra en las mismas unidades que el valor especificado para *DeviceResolution*.                          |
| *DesignUnits*      | Especifica la métrica de fuente que se va a convertir en unidades de dispositivo. Este valor puede ser cualquier métrica de fuente, incluido el ancho de un carácter o el valor ascendente de una fuente completa. |
| *unitsPerEm*       | Especifica el tamaño del cuadrado em de la fuente.                                                                                                                                 |
| *PointSize*        | Especifica el tamaño de la fuente, en puntos. (Un punto es igual a 1/72 de pulgada).                                                                                                 |
| *DeviceResolution* | Especifica el número de unidades de dispositivo (píxeles) por pulgada. Los valores típicos pueden ser 300 para una impresora láser o 96 para una pantalla VGA.                                                |



 

Esta fórmula no debe utilizarse para volver a convertir las unidades de dispositivo en unidades de diseño. Las unidades de dispositivo siempre se redondean al píxel más cercano. El error de redondeo propagado puede llegar a ser muy grande, sobre todo cuando una aplicación trabaja con tamaños de pantalla.

Para solicitar unidades de diseño, cree una fuente lógica cuyo alto se especifique como *unitsPerEm*. Las aplicaciones pueden recuperar el valor de *unitsPerEm* llamando a la función [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) y comprobando el miembro **ntmSizeEM** de la estructura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .

 

 



