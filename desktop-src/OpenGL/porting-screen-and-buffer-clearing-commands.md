---
title: Comandos de borrado de búfer y pantalla de porte
description: OpenGL reemplaza una variedad de funciones claras de IRIS GL (como zclear, aclear, sclear, entre otras) por una sola función, glClear. Especifique exactamente lo que desea borrar pasando las máscaras a glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Porte de IRIS GL, funciones clear
- porting from IRIS GL,clear functions
- porte a OpenGL desde IRIS GL, funciones clear
- Porte de OpenGL desde IRIS GL, funciones clear
- funciones clear
- Porte de IRIS GL, comandos de borrado de pantalla
- porte desde IRIS GL, comandos de borrado de pantalla
- porte a OpenGL desde IRIS GL, comandos de borrado de pantalla
- Porte de OpenGL desde IRIS GL, comandos de borrado de pantalla
- comandos de borrado de pantalla
- Porte de IRIS GL, comandos de borrado de búfer
- porting from IRIS GL,buffer clearing commands
- porte a OpenGL desde IRIS GL, comandos de borrado de búfer
- Porte de OpenGL desde IRIS GL, comandos de borrado de búfer
- comandos de borrado de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073989"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Comandos de borrado de búfer y pantalla de porte

OpenGL reemplaza una variedad de funciones claras **de** IRIS GL (como **zclear**, **aclear,** **sclear,** y así sucesivamente) por una sola función, [**glClear**](glclear.md). Especifique exactamente lo que desea borrar pasando las máscaras **a glClear.**

Tenga en cuenta los siguientes puntos al portear comandos de pantalla y búfer:

-   OpenGL mantiene los colores de borrado por separado de los colores de dibujo, con llamadas como [**glClearColor**](glclearcolor.md) y [**glClearIndex.**](glclearindex.md) Asegúrese de establecer el color claro para cada búfer antes de borrar.
-   En lugar de usar una de las distintas llamadas sin nombre, ahora se borran varios búferes con una llamada, [**glClear**](glclear.md), mediante **LA** agrupación de máscaras de búfer. Por ejemplo, **se reemplaza por:**

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL hace referencia a latippla de polígono y a la máscara de escritura de color. OpenGL omite latippla del polígono, pero hace referencia a la máscara de escritura de color. (La **funciónclear** no tiene en cuenta latippla de polígono y la máscara de escritura de color).

En la tabla siguiente se enumeran las distintas funciones clear de IRIS GL con sus funciones OpenGL equivalentes.



| Llamada a IRIS GL         | Llamada a OpenGL                                                               | Significado                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ CLEAR) | **glClear**( GL \_ ACCUM \_ BUFFER BIT \_ )                                     | Borre el búfer de acumulación.                    |
|                      | **glClearColor**                                                          | Establezca el color claro RGBA.                         |
|                      | **glClearIndex**                                                          | Establezca el índice de color claro.                        |
| **clear**            | **glClear**( GL \_ COLOR BUFFER BIT \_ \_ )                                     | Borre el búfer de color.                           |
|                      | **glClearDepth**                                                          | Especifique el valor sin borrar para el búfer de profundidad.     |
| **zclear**           | **glClear**( GL \_ DEPTH BUFFER BIT \_ \_ )                                     | Borre el búfer de profundidad.                           |
| **clear**          | **glClear**(GL \_ COLOR BUFFER BIT GL DEPTH BUFFER BIT \_ \_ \| \_ \_ \_ )<br/> | Borre el búfer de color y el búfer de profundidad.      |
|                      | **glClearAccum**                                                          | Especifique valores no válidos para el búfer de acumulación. |
|                      | **glClearStencil**                                                        | Especifique el valor sin borrar para el búfer de galería de símbolos.   |
| **sclear**           | **glClear**( GL \_ STENCIL \_ BUFFER BIT \_ )                                   | Borre el búfer de galería de símbolos.                         |



 

Cuando el código GL de IRIS usa **gclear** y **sclear,** puede combinarlos en una única **llamada glClear;** puede mejorar el rendimiento del programa.

 

 





