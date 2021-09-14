---
description: Las siguientes funciones se usan para crear, modificar o dibujar rutas de acceso.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Funciones de ruta de acceso (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168334"
---
# <a name="path-functions-windows-gdi"></a>Funciones de ruta de acceso (Windows GDI)

Las siguientes funciones se usan para crear, modificar o dibujar rutas de acceso.



| Función                                       | Descripción                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Cierra y descarta las rutas de acceso en el contexto de dispositivo especificado.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Abre un corchete de ruta de acceso en el contexto de dispositivo especificado.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Cierra una figura abierta en una ruta de acceso.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Cierra un corchete de ruta de acceso y selecciona la ruta de acceso definida por el corchete en el contexto de dispositivo especificado.                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Cierra las figuras abiertas en la ruta de acceso actual y rellena el interior del trazado mediante el uso del pincel actual y el modo de relleno de polígonos.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Transforma las curvas del trazado seleccionado en el contexto del dispositivo (DC) actual, convirtiendo cada curva en una secuencia de líneas.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Recupera el límite de inglete para el contexto de dispositivo especificado.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Recupera las coordenadas que definen los puntos de conexión de las líneas y los puntos de control de las curvas que se encuentran en la ruta de acceso seleccionada en el contexto de dispositivo especificado. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Crea una región a partir de la ruta de acceso seleccionada en el contexto de dispositivo especificado.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Establece el límite de la longitud de las combinaciones de mitro para el contexto de dispositivo especificado.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Cierra las figuras abiertas de un trazado, acaricia el contorno del trazado mediante el lápiz actual y rellena su interior mediante el pincel actual.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Representa la ruta de acceso especificada mediante el lápiz actual.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Vuelve a definir la ruta de acceso actual como el área que se pintaría si la ruta de acceso se acariciase con el lápiz seleccionado actualmente en el contexto del dispositivo especificado.            |



 

 

 



