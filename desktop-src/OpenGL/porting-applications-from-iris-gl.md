---
title: Porting Applications from IRIS GL
description: Porting Applications from IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL on Windows,IRIS GL porting
- porting to OpenGL,IRIS GL
- Porte de OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68e218e5b6f57039e364ab4e6ebc29fb1f2b2fad2e8a679b35c1368367f5f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777235"
---
# <a name="porting-applications-from-iris-gl"></a>Porting Applications from IRIS GL

En esta sección se enumeran las diferencias importantes entre IRIS GL y OpenGL y se describen los pasos básicos para portear código de IRIS GL a OpenGL. Para obtener una lista completa de las diferencias entre IRIS GL y Open GL, consulte Diferencias de [IRIS GL y OpenGL.](iris-gl-and-opengl-differences.md)

La porción de programas GL de IRIS a OpenGL Windows requiere mucho más trabajo que convertir programas OpenGL desde el sistema de ventanas X. Aunque los programas IRIS GL están diseñados para ejecutarse con hardware y software específicos, OpenGL se diseñó para la portabilidad entre varios sistemas.

En la tabla siguiente se enumeran algunas de las principales diferencias entre los programas OpenGL e IRIS GL.



| Código OpenGL                                                                                                                                              | Código GL de IRIS                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Sistema operativo independiente; no contiene funciones para ventanas, control de eventos, asignación/administración de búferes, y así sucesivamente.                              | Dependiente del sistema operativo; Las funciones del sistema de ventanas se mezclan con las funciones de representación. No hay ningún administrador de ventanas en IRIS GL. |
| Usa una convención de nomenclatura estándar y común. Las funciones OpenGL y los tipos definidos comienzan con un prefijo "gl" para evitar conflictos con otras bibliotecas.        | No usa una convención de nomenclatura común para funciones y tipos definidos.                                                              |
| Administra las variables de estado (por ejemplo, color, color, textura, iluminación, entre otras) de forma directa y coherente. No usa tablas para cargar valores de variable de estado. | Usa tablas para administrar variables de estado y debe enlazar variables a valores de tabla.                                                        |
| Las listas para mostrar no se pueden editar.                                                                                                                          | Las listas para mostrar se pueden editar.                                                                                                          |
| No proporciona un formato de archivo para las fuentes.                                                                                                                | Proporciona funciones para controlar fuentes y cadenas de texto y un formato de archivo para las fuentes.                                                      |
| Incluye una biblioteca de la utilidad GL (GLU) que contiene funciones y rutinas adicionales (como LABS y las rutinas de representación cuadráticas).                    | No admite la biblioteca GLU.                                                                                                     |



 

**Use el siguiente procedimiento general para portabilidad de los programas DE IRIS GL a OpenGL.**

1.  Vuelva a escribir cualquier código que haga llamadas a un administrador de ventanas, configuración de ventana, dispositivo o evento, o donde cargue un mapa de colores en un código Windows equivalente. Volver a escribir una aplicación de un sistema operativo a otro puede ser compleja y difícil. Este tema está fuera del ámbito de esta sección.
2.  Busque cualquier código que use las funciones y rutinas de IRIS GL. Traduzca estas funciones a sus funciones openGL equivalentes. Para obtener una lista completa de las funciones y rutinas de IRIS GL y sus equivalentes de OpenGL equivalentes, vea Funciones OpenGL y [Sus equivalentes de IRIS GL](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Cambie el código GL de IRIS como se describe en Problemas de porte de [IRIS GL especiales.](special-iris-gl-porting-issues.md)

<!-- -->

1.  Vuelva a escribir cualquier código que haga llamadas a un administrador de ventanas, configuración de ventana, dispositivo o evento, o donde cargue un mapa de colores en un código Windows equivalente. Volver a escribir una aplicación de un sistema operativo a otro puede ser compleja y difícil. Este tema está fuera del ámbito de esta sección.
2.  Busque cualquier código que use las funciones y rutinas de IRIS GL. Traduzca estas funciones a sus funciones openGL equivalentes. Para obtener una lista completa de las funciones y rutinas de IRIS GL y sus equivalentes de OpenGL equivalentes, vea Funciones OpenGL y [Sus equivalentes de IRIS GL](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Cambie el código GL de IRIS como se describe en Problemas de porte de [IRIS GL especiales.](special-iris-gl-porting-issues.md)

 

 




