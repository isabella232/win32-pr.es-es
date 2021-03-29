---
title: Trasladar los planos de recorte
description: OpenGL implementa los planos de recorte de forma similar a IRIS GL. Además, en OpenGL puede consultar los planos de recorte. En la tabla siguiente se enumeran las funciones de plano de recorte del IRIS GL y sus funciones de OpenGL equivalentes.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Migración de GL de IRIS, planos de recorte
- portabilidad de IRIS GL, planos de recorte
- portabilidad a OpenGL desde IRIS GL, planos de recorte
- Exportación de OpenGL desde IRIS GL, planos de recorte
- planos de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779117"
---
# <a name="porting-clipping-planes"></a>Trasladar los planos de recorte

OpenGL implementa los planos de recorte de forma similar a IRIS GL. Además, en OpenGL puede consultar los planos de recorte. En la tabla siguiente se enumeran las funciones de plano de recorte del IRIS GL y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                          | Función OpenGL                                                                               | Significado                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ on**, params)     | [**glEnable**](glenable.md) (plano de clip de contabilidad \_ \_ )                                             | Habilita el recorte en el plano i.             |
| **clipplane**(i, **\_ definición de CP**, plano) | [**glClipPlane**](glclipplane.md) ( \_ \_ plano de clip de contabilidad general, plano)                                | Define el plano de recorte.                  |
|                                           | [**glGetClipPlane**](glgetclipplane.md)                                                      | Devuelve la ecuación del plano de recorte.         |
|                                           | [**glIsEnabled**](glisenabled.md) (plano de clip de contabilidad \_ \_ )                                       | Devuelve true si está habilitado el plano de recortes. |
| **scrmask**                               | [**glScissor**](glscissor.md)                                                                | Define el cuadro de tijeras.                 |
| **getscrmask**                            | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ cuadro de tijeras de contabilidad \_ ) | Devuelve el rectángulo de tijeras actual.         |



 

Para activar la prueba de tijeras, llame a **glEnable** con \_ el cuadro con tijeras de GL \_ como parámetro.

??

 

 




