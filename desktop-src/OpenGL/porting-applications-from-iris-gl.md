---
title: Trasladar aplicaciones de IRIS GL
description: Trasladar aplicaciones de IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL en Windows, migración de la contabilidad de IRIS
- trasladar a OpenGL, IRIS GL
- Portabilidad de OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9e739b40f63bb2fd00bb62b4e5ec5566df3c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665735"
---
# <a name="porting-applications-from-iris-gl"></a>Trasladar aplicaciones de IRIS GL

En esta sección se enumeran las diferencias importantes entre IRIS GL y OpenGL y se describen los pasos básicos para portar el código de IRIS GL a OpenGL. Para obtener una lista completa de las diferencias entre IRIS GL y Open GL, consulte [diferencias de iris GL y OpenGL](iris-gl-and-opengl-differences.md).

La migración de programas de la contabilidad de IRIS a OpenGL para Windows requiere mucho más trabajo que la conversión de programas OpenGL del sistema de ventanas X. Aunque los programas de la contabilidad de IRIS están diseñados para ejecutarse con hardware y software específicos, OpenGL se diseñó para la portabilidad entre varios sistemas.

En la tabla siguiente se enumeran algunas de las diferencias principales entre los programas OpenGL y IRIS GL.



| Código OpenGL                                                                                                                                              | Código de GL de IRIS                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Independiente del sistema operativo; no contiene funciones para la ventana, el control de eventos, la asignación y administración de búfer, etc.                              | Depende del sistema operativo; ventana: las funciones del sistema se mezclan con las funciones de representación. No hay ningún administrador de Windows en IRIS GL. |
| Utiliza una Convención de nomenclatura común estándar. Las funciones OpenGL y los tipos definidos comienzan con un prefijo "GL" para evitar conflictos con otras bibliotecas.        | No utiliza una Convención de nomenclatura común para las funciones y los tipos definidos.                                                              |
| Administra las variables de estado (por ejemplo, color, niebla, textura, iluminación, etc.) de forma directa y coherente. No utiliza tablas para cargar valores de variables de estado. | Utiliza tablas para administrar variables de estado y debe enlazar variables a valores de tabla.                                                        |
| No se pueden editar las listas de visualización.                                                                                                                          | Las listas de visualización se pueden editar.                                                                                                          |
| No proporciona un formato de archivo para las fuentes.                                                                                                                | Proporciona funciones para controlar las fuentes y las cadenas de texto y un formato de archivo para las fuentes.                                                      |
| Incluye una biblioteca de utilidades GL (GLU) que contiene funciones y rutinas adicionales (como las rutinas de representación de NURBS y cuadrática).                    | No admite la biblioteca GLU.                                                                                                     |



 

**Utilice el siguiente procedimiento general para trasladar los programas de la contabilidad de IRIS a OpenGL**

1.  Vuelva a escribir el código que realiza llamadas a un administrador de ventanas, una configuración de ventana, un dispositivo o un evento, o dónde se carga un mapa de colores en el código de Windows equivalente. Volver a escribir una aplicación de un sistema operativo a otro puede ser complejo y difícil. Este asunto está fuera del ámbito de esta sección.
2.  Busque cualquier código que use las funciones y rutinas de la contabilidad de IRIS. Traduzca estas funciones a sus funciones de OpenGL equivalentes. Para obtener una lista completa de las funciones y rutinas de la contabilidad de IRIS y sus homólogos de OpenGL equivalentes, consulte [funciones de OpenGL y sus equivalentes de contabilidad de iris](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Cambie el código de la contabilidad de IRIS tal y como se describe en [problemas especiales de portabilidad de iris](special-iris-gl-porting-issues.md).

<!-- -->

1.  Vuelva a escribir el código que realiza llamadas a un administrador de ventanas, una configuración de ventana, un dispositivo o un evento, o dónde se carga un mapa de colores en el código de Windows equivalente. Volver a escribir una aplicación de un sistema operativo a otro puede ser complejo y difícil. Este asunto está fuera del ámbito de esta sección.
2.  Busque cualquier código que use las funciones y rutinas de la contabilidad de IRIS. Traduzca estas funciones a sus funciones de OpenGL equivalentes. Para obtener una lista completa de las funciones y rutinas de la contabilidad de IRIS y sus homólogos de OpenGL equivalentes, consulte [funciones de OpenGL y sus equivalentes de contabilidad de iris](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Cambie el código de la contabilidad de IRIS tal y como se describe en [problemas especiales de portabilidad de iris](special-iris-gl-porting-issues.md).

 

 




