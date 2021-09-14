---
title: Porte de puntos
description: OpenGL no tiene ningún comando para dibujar un único punto. De lo contrario, las funciones de punto de porte son sencillas. En la tabla siguiente se enumeran las funciones GL de IRIS para los puntos de dibujo y sus funciones OpenGL equivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Porte de IRIS GL, puntos
- porte desde IRIS GL, puntos
- porte a OpenGL desde IRIS GL, puntos
- Porte de OpenGL desde IRIS GL, puntos
- funciones de dibujo, puntos
- puntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074001"
---
# <a name="porting-points"></a>Porte de puntos

OpenGL no tiene ningún comando para dibujar un único punto. De lo contrario, las funciones de punto de porte son sencillas. En la tabla siguiente se enumeran las funciones GL de IRIS para los puntos de dibujo y sus funciones OpenGL equivalentes.



| Función GL de IRIS           | Función OpenGL                                                   | Significado                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pnt**                    |                                                                   | Dibuja un único punto.                                                                                                                                |
| **bgnpoint**, **endpoint** | [**glBegin**](glbegin.md) ( GL \_ POINTS ), [ **glEnd**](glend.md) | Interpreta los vértices como puntos.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Establece el tamaño del punto en píxeles.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( GL \_ POINT \_ SMOOTH )                | Activa el suavizado de contorno de punto. (Para obtener más información sobre el suavizado de contorno de punto, vea [Porting Antialiasing Functions](porting-antialiasing-functions.md)). |



 

Para obtener información sobre las funciones get relacionadas, [**vea glPointSize**](glpointsize.md).

??

 

 




