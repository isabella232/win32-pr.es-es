---
title: Porte de funciones que obtienen matrices y transformaciones
description: En la tabla siguiente se enumeran las funciones GL de IRIS que obtienen el estado de matrices y transformaciones y sus equivalentes de OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Porte de IRIS GL, matrices
- porting from IRIS GL,matrices
- porte a OpenGL desde IRIS GL, matrices
- Porte de OpenGL desde IRIS GL, matrices
- matrices
- Porte de IRIS GL, transformaciones
- porte desde IRIS GL, transformaciones
- porte a OpenGL desde IRIS GL, transformaciones
- Porte de OpenGL desde IRIS GL, transformaciones
- transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169161"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Porte de funciones que obtienen matrices y transformaciones

En la tabla siguiente se enumeran las funciones GL de IRIS que obtienen el estado de matrices y transformaciones y sus equivalentes de OpenGL.



| Consulta de matriz DE IRIS GL                  | Consulta de matriz glGet de OpenGL         | Significado                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | MODO DE \_ MATRIZ \_ GL                  | Devuelve el modo de matriz actual.                                |
| **getmatrix** en **modo MVIEWING**    | GL \_ MODELVIEW \_ MATRIX             | Devuelve una copia de la matriz de vista de modelo actual.                |
| **getmatrix** en **modo MPROJECTION** | MATRIZ \_ DE PROYECCIÓN \_ GL            | Devuelve una copia de la matriz de proyección actual.                |
| **getmatrix** en **modo MTEXTURE**    | MATRIZ \_ DE TEXTURA \_ DE GL               | Devuelve una copia de la matriz de textura actual.                   |
| No aplicable.                       | GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH  | Devuelve la profundidad máxima admitida de la pila de matriz de vista de modelo. |
| No aplicable.                       | PROFUNDIDAD DE \_ PILA \_ DE \_ PROYECCIÓN MÁXIMA \_ DE GL | Devuelve la profundidad máxima admitida de la pila de matriz de proyección. |
| No aplicable.                       | PROFUNDIDAD \_ DE PILA DE TEXTURA MÁXIMA \_ \_ \_ DE GL    | Devuelve la profundidad máxima admitida de la pila de matriz de textura.    |
| No aplicable.                       | PROFUNDIDAD DE \_ PILA DE GL MODELVIEW \_ \_       | Devuelve el número de matrices en la pila de vistas del modelo.             |
| No aplicable.                       | PROFUNDIDAD DE \_ PILA \_ DE PROYECCIÓN DE \_ GL      | Devuelve el número de matrices en la pila de proyección.             |
| No aplicable.                       | PROFUNDIDAD DE \_ LA PILA DE TEXTURA DE \_ \_ GL         | Devuelve el número de matrices en la pila de texturas.                |



 

??

 

 




