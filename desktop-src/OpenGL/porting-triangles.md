---
title: Porte de triángulos
description: Puede dibujar tres tipos de triángulos en triángulos independientes de OpenGL, franjas de triángulos y ventiladores de triángulo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Porte de IRIS GL, triángulos
- porting from IRIS GL,triangles
- porte a OpenGL desde IRIS GL, triángulos
- Porte de OpenGL desde IRIS GL, triángulos
- funciones de dibujo, triángulos
- triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362037"
---
# <a name="porting-triangles"></a>Porte de triángulos

Puede dibujar tres tipos de triángulos en OpenGL: triángulos independientes, franjas de triángulos y ventiladores de triángulo.

OpenGL no tiene ningún equivalente para la función **swaptmesh** de IRIS GL. Puede lograr el mismo efecto mediante una combinación de triángulos, franjas de triángulo y ventiladores de triángulo.

En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar triángulos y sus funciones OpenGL equivalentes.



| Función IRIS GL           | Parámetro glBegin equivalente | Significado                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | TRIÁNGULOS \_ GL                | Triples de vértices interpretados como triángulos. |
| **bgntmesh**, **endtmesh** | FRANJA \_ DE \_ TRIÁNGULOS GL          | Franjas vinculadas de triángulos.                   |
|                            | VENTILADOR \_ DE TRIÁNGULO \_ GL            | Ventiladores vinculados de triángulos.                     |



 

??

 

 




