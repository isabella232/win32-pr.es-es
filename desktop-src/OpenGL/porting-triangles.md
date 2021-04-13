---
title: Trasladar triángulos
description: Puede dibujar tres tipos de triángulos en OpenGL independientes triángulos, franjas de triángulo y ventiladores de triángulo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Migración de la contabilidad de IRIS, triángulos
- trasladar de IRIS GL, triángulos
- trasladar a OpenGL desde IRIS GL, triángulos
- Exportación de OpenGL desde IRIS GL, triángulos
- dibujar funciones, triángulos
- triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357350"
---
# <a name="porting-triangles"></a>Trasladar triángulos

Puede dibujar tres tipos de triángulos en OpenGL: triángulos, tiras de triángulo y ventiladores de triángulo independientes.

OpenGL no tiene equivalente a la función **swaptmesh** de la contabilidad de iris. Puede lograr el mismo efecto mediante una combinación de triángulos, tiras de triángulo y ventiladores de triángulo.

En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar triángulos y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS           | Parámetro glBegin equivalente | Significado                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | triángulos de contabilidad \_                | Las tripas de los vértices se interpretan como triángulos. |
| **bgntmesh**, **endtmesh** | \_franja de triángulo de GL \_          | Bandas de triángulos vinculadas.                   |
|                            | \_ventilador de triángulo GL \_            | Ventiladores vinculados de triángulos.                     |



 

??

 

 




