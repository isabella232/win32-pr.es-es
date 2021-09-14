---
title: Uso de funciones de suavizado de contorno
description: En la tabla siguiente se enumeran las funciones de suavizado de contorno de IRIS GL y sus funciones OpenGL equivalentes.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Porte de IRIS GL, suavizado de contorno
- porting from IRIS GL,antialiasing
- porting to OpenGL from IRIS GL,antialiasing
- Porte de OpenGL desde IRIS GL, suavizado de contorno
- suavizado de contorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361985"
---
# <a name="using-antialiasing-functions"></a>Uso de funciones de suavizado de contorno

En la tabla siguiente se enumeran las funciones de suavizado de contorno de IRIS GL y sus funciones OpenGL equivalentes.



| Función IRIS GL | Función OpenGL                                      | Significado                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) ( GL \_ POINT \_ SMOOTH )   | Habilita el suavizado de contorno de puntos.   |
| **linesmooth**   | **glEnable**( GL \_ LINE \_ SMOOTH )                     | Habilita el suavizado de contorno de líneas.    |
| **polysmooth**   | [**glEnable**](glenable.md) ( GL \_ POLYGON \_ SMOOTH ) | Habilita el suavizado de contorno de polígonos. |



 

Use las llamadas [**glDisable**](gldisable.md) equivalentes para desactivar el suavizado de contorno.

En IRIS GL, puede controlar la calidad del suavizado de contorno llamando a:


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL proporciona un control similar [**glHint:**](glhint.md)


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



donde *hintMode* es uno de los siguientes:

-   GL \_ NICEST (Use el suavizado de mayor calidad).
-   GL \_ FASTEST (use el suavizado más eficaz).
-   GL \_ DONT \_ CARE

IRIS GL también permite la corrección final mediante una llamada a:


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL no tiene ningún equivalente para esta función.

 

 




