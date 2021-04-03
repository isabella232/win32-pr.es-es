---
title: Trasladar el código de color, sombreado y Writemask
description: Trasladar el código de color, sombreado y Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Puerto de GL de IRIS, color
- portabilidad de IRIS GL, color
- trasladar a OpenGL desde IRIS GL, color
- Exportación de OpenGL desde IRIS GL, color
- Migración de la contabilidad de IRIS, sombreado
- portabilidad de IRIS GL, sombreado
- trasladar a OpenGL desde IRIS GL, sombreado
- Exportación de OpenGL desde IRIS GL, sombreado
- Migración de la contabilidad de IRIS, writemask
- portabilidad de IRIS GL, writemask
- migración a OpenGL desde IRIS GL, writemask
- Exportación de OpenGL desde IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774004"
---
# <a name="porting-color-shading-and-writemask-code"></a>Trasladar el código de color, sombreado y Writemask

Al migrar el código de color, sombreado y writemask a OpenGL, tenga en cuenta los puntos siguientes:

-   Aunque puede establecer índices de mapa de colores con la función [glIndex](glindex-functions.md) de OpenGL, OpenGL no tiene una función para cargar índices de mapa de colores.
-   Los valores de color se normalizan en su tipo de datos. (Para obtener información sobre los valores de color, vea [glColor](glcolor-functions.md)).
-   No hay ningún equivalente simple para **cpack**.
-   Es posible que tenga que traducir el código que incluye las funciones de **c** o **color** a [**glClearColor**](glclearcolor.md) o [**glClearIndex**](glclearindex.md) en lugar de **glColor** o **glIndex**.
-   El writemask RGBA se aplica a cada componente, pero no a cada bit.
-   IRIS GL proporciona constantes de color definidas: negro, azul, rojo, verde, MAGENTA, aguamarina, amarillo y blanco. OpenGL no proporciona estas constantes.

En este tema se incluye información sobre lo siguiente.

-   [Trasladar llamadas de color](porting-color-calls.md)
-   [Trasladar modelos de sombreado](porting-shading-models.md)

 

 




