---
description: Las siguientes funciones se usan para crear, modificar o dibujar rutas de acceso.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Funciones de ruta de acceso (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984883"
---
# <a name="path-functions-windows-gdi"></a>Funciones de ruta de acceso (Windows GDI)

Las siguientes funciones se usan para crear, modificar o dibujar rutas de acceso.



| Función                                       | Descripción                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Cierra y descarta cualquier ruta de acceso en el contexto de dispositivo especificado.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Abre un corchete de ruta de acceso en el contexto de dispositivo especificado.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Cierra una figura abierta en una ruta de acceso.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Cierra un corchete de ruta de acceso y selecciona la ruta de acceso definida por el corchete en el contexto de dispositivo especificado.                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Cierra las figuras abiertas en la ruta de acceso actual y rellena el interior del trazado mediante el pincel actual y el modo de relleno de polígonos.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Transforma cualquier curva del trazado seleccionado en el contexto de dispositivo actual (DC), y convierte cada curva en una secuencia de líneas.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Recupera el límite angular para el contexto de dispositivo especificado.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Recupera las coordenadas que definen los extremos de las líneas y los puntos de control de las curvas que se encuentran en la ruta de acceso que está seleccionada en el contexto de dispositivo especificado. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Crea una región a partir de la ruta de acceso que está seleccionada en el contexto de dispositivo especificado.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Establece el límite para la longitud de las combinaciones en ángulo para el contexto de dispositivo especificado.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Cierra las figuras abiertas en un trazado, traza el contorno del trazado mediante el lápiz actual y rellena su interior con el pincel actual.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Representa la ruta de acceso especificada utilizando el lápiz actual.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Vuelve a definir la ruta de acceso actual como área que se va a pintar si la ruta de acceso se traza con el lápiz seleccionado actualmente en el contexto de dispositivo determinado.            |



 

 

 



