---
title: Porte de triángulos
description: Puede dibujar tres tipos de triángulos en triángulos independientes de OpenGL, franjas de triángulos y ventiladores de triángulo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Porte de IRIS GL, triángulos
- porte desde IRIS GL, triángulos
- porte a OpenGL desde IRIS GL, triángulos
- Porte de OpenGL desde IRIS GL, triángulos
- funciones de dibujo, triángulos
- triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85acc650a709650495b93cdd00176400f00168cc8fe6445a23505f12b332abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012003"
---
# <a name="porting-triangles"></a>Porte de triángulos

Puede dibujar tres tipos de triángulos en OpenGL: triángulos independientes, franjas de triángulos y ventiladores de triángulo.

OpenGL no tiene ningún equivalente para la función **swaptmesh** de IRIS GL. Puede lograr el mismo efecto mediante una combinación de triángulos, franjas de triángulos y ventiladores de triángulo.

En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar triángulos y sus funciones OpenGL equivalentes.



| Función GL de IRIS           | Parámetro glBegin equivalente | Significado                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | TRIÁNGULOS \_ GL                | Triples de vértices interpretados como triángulos. |
| **bgntmesh**, **endtmesh** | FRANJA \_ DE TRIÁNGULO \_ GL          | Franjas vinculadas de triángulos.                   |
|                            | GL \_ TRIANGLE \_ FAN            | Ventiladores vinculados de triángulos.                     |



 

??

 

 




