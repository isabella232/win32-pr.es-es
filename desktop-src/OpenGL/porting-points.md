---
title: Puntos de portabilidad
description: OpenGL no tiene ningún comando para dibujar un único punto. De lo contrario, las funciones de punto de portabilidad son sencillas. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para los puntos de dibujo y sus funciones de OpenGL equivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Migración de la contabilidad de IRIS, puntos
- trasladar de IRIS GL, puntos
- trasladar a OpenGL desde IRIS GL, puntos
- Exportación de OpenGL desde IRIS GL, puntos
- dibujar funciones, puntos
- puntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665690"
---
# <a name="porting-points"></a>Puntos de portabilidad

OpenGL no tiene ningún comando para dibujar un único punto. De lo contrario, las funciones de punto de portabilidad son sencillas. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para los puntos de dibujo y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS           | Función OpenGL                                                   | Significado                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PNT**                    |                                                                   | Dibuja un solo punto.                                                                                                                                |
| **bgnpoint**, **extremo** | [**glBegin**](glbegin.md) ( \_ puntos de contabilidad), [ **glEnd**](glend.md) | Interpreta los vértices como puntos.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Establece el tamaño del punto en píxeles.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) (punto de contabilidad \_ \_ suave)                | Activa el suavizado de contorno de punto. (Para obtener más información sobre el suavizado de contorno de punto, vea [portar funciones de suavizado de contorno](porting-antialiasing-functions.md)). |



 

Para obtener información sobre las funciones Get relacionadas, vea [**glPointSize**](glpointsize.md).

??

 

 




