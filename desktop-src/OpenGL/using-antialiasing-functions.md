---
title: Usar funciones de suavizado de contorno
description: En la tabla siguiente se enumeran las funciones de suavizado de contorno de IRIS y sus funciones de OpenGL equivalentes.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Migración de la contabilidad de IRIS y suavizado de contorno
- portabilidad de IRIS GL, antialiasing
- trasladar a OpenGL desde IRIS GL, suavizado de contorno
- Exportación de OpenGL desde IRIS GL, suavizado de contorno
- suavizado de contorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268578"
---
# <a name="using-antialiasing-functions"></a>Usar funciones de suavizado de contorno

En la tabla siguiente se enumeran las funciones de suavizado de contorno de IRIS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS | Función OpenGL                                      | Significado                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) (punto de contabilidad \_ \_ suave)   | Habilita el suavizado de contorno de los puntos.   |
| **linesmooth**   | **glEnable**(línea de contabilidad \_ \_ suave)                     | Habilita el suavizado de contorno de las líneas.    |
| **polismooth**   | [**glEnable**](glenable.md) (GL \_ polígono \_ Smooth) | Habilita el suavizado de contorno de polígonos. |



 

Use las llamadas [**glDisable**](gldisable.md) equivalentes para desactivar el suavizado de contorno.

En IRIS GL, puede controlar la calidad del suavizado de contorno llamando a:


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL proporciona controluse [**glHint**](glhint.md)similares:


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



donde *hintMode* es uno de los siguientes:

-   Libro \_ de contabilidad más agradable (use el suavizado de mayor calidad).
-   GL más \_ rápido (use el suavizado más eficaz).
-   no importa el libro de contabilidad \_ \_

IRIS GL también permite la corrección final mediante una llamada a:


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL no tiene ningún equivalente para esta función.

 

 




