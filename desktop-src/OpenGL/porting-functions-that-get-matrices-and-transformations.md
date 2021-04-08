---
title: Portabilidad de funciones que obtienen matrices y transformaciones
description: En la tabla siguiente se enumeran las funciones de contabilidad de IRIS que obtienen el estado de las matrices y transformaciones y sus equivalentes de OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Puerto de GL de IRIS, matrices
- portabilidad de IRIS GL, matrices
- trasladar a OpenGL desde IRIS GL, matrices
- Exportación de OpenGL desde IRIS GL, matrices
- matrices
- Migración de la contabilidad de IRIS, transformaciones
- portabilidad de IRIS GL, transformaciones
- trasladar a OpenGL desde IRIS GL, transformaciones
- Exportación de OpenGL desde IRIS GL, transformaciones
- transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994334"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Portabilidad de funciones que obtienen matrices y transformaciones

En la tabla siguiente se enumeran las funciones de contabilidad de IRIS que obtienen el estado de las matrices y transformaciones y sus equivalentes de OpenGL.



| Consulta de matriz de GL de IRIS                  | Consulta de matriz OpenGL glGet         | Significado                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | \_modo de matriz de contabilidad general \_                  | Devuelve el modo de matriz actual.                                |
| **getmatrix** en modo **MVIEWING**    | \_matriz MODELVIEW de GL \_             | Devuelve una copia de la matriz de vista de modelo actual.                |
| **getmatrix** en modo **MPROJECTION** | \_matriz de proyección de contabilidad \_            | Devuelve una copia de la matriz de proyección actual.                |
| **getmatrix** en modo **MTEXTURE**    | \_matriz de textura de GL \_               | Devuelve una copia de la matriz de textura actual.                   |
| No es aplicable.                       | \_profundidad máxima de la \_ \_ pila MODELVIEW \_ de GL  | Devuelve la profundidad máxima admitida de la pila de matrices de la vista de modelo. |
| No es aplicable.                       | \_profundidad máxima de la \_ pila de proyección de \_ GL \_ | Devuelve la profundidad máxima admitida de la pila de la matriz de proyección. |
| No es aplicable.                       | \_profundidad máxima de la \_ pila de textura de \_ GL \_    | Devuelve la profundidad máxima admitida de la pila de la matriz de textura.    |
| No es aplicable.                       | profundidad de la pila de GL \_ MODELVIEW \_ \_       | Devuelve el número de matrices en la pila de vistas de modelo.             |
| No es aplicable.                       | profundidad de la pila de proyección de contabilidad \_ \_ \_      | Devuelve el número de matrices en la pila de proyección.             |
| No es aplicable.                       | profundidad de la pila de textura de GL \_ \_ \_         | Devuelve el número de matrices de la pila de textura.                |



 

??

 

 




