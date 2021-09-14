---
title: Porting Color, Shading, and Writemask Code
description: Porting Color, Shading, and Writemask Code
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Porte de IRIS GL, color
- porting from IRIS GL,color
- porte a OpenGL desde IRIS GL, color
- Porte de OpenGL desde IRIS GL, color
- Porte de IRIS GL, sombreado
- porting from IRIS GL,shading
- porte a OpenGL desde IRIS GL, sombreado
- Porte de OpenGL desde IRIS GL, sombreado
- Porte de IRIS GL, máscara de escritura
- porting from IRIS GL,writemask
- porting to OpenGL from IRIS GL,writemask
- Porte de OpenGL desde IRIS GL, máscara de escritura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169205"
---
# <a name="porting-color-shading-and-writemask-code"></a>Porting Color, Shading, and Writemask Code

Al portear el color, el sombreado y escribir código de máscara en OpenGL, tenga en cuenta los siguientes puntos:

-   Aunque puede establecer índices de mapa de colores con la función [glIndex](glindex-functions.md) de OpenGL, OpenGL no tiene una función para cargar índices de mapa de colores.
-   Los valores de color se normalizan con su tipo de datos. (Para obtener información sobre los valores de color, [vea glColor](glcolor-functions.md)).
-   No hay ningún equivalente simple para **cpack**.
-   Es posible que tenga que traducir el código que incluye las funciones **c** o **color** a [**glClearColor**](glclearcolor.md) o [**glClearIndex en**](glclearindex.md) lugar de **glColor** o **glIndex**.
-   La máscara de escritura RGBA se aplica a cada componente, pero no a cada bit.
-   IRIS GL proporciona constantes de color definidas: BLACK, BLUE, RED, GREEN, YELLOW, YELLOW y WHITE. OpenGL no proporciona estas constantes.

En este tema se incluye información sobre lo siguiente.

-   [Porte de llamadas de color](porting-color-calls.md)
-   [Porte de modelos de sombreado](porting-shading-models.md)

 

 




