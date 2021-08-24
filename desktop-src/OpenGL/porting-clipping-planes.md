---
title: Porte de planos de recorte
description: OpenGL implementa planos de recorte de forma similar a IRIS GL. Además, en OpenGL puede consultar planos de recorte. En la tabla siguiente se enumeran las funciones del plano de recorte de IRIS GL y sus funciones OpenGL equivalentes.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Porte de IRIS GL, planos de recorte
- porte desde IRIS GL, planos de recorte
- porte a OpenGL desde IRIS GL, planos de recorte
- Porte de OpenGL desde IRIS GL, planos de recorte
- planos de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314b7c6453de3b0933970b7d520a8c161d6eef4a9bb98ea891c73665fba4933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777125"
---
# <a name="porting-clipping-planes"></a>Porte de planos de recorte

OpenGL implementa planos de recorte de forma similar a IRIS GL. Además, en OpenGL puede consultar planos de recorte. En la tabla siguiente se enumeran las funciones del plano de recorte de IRIS GL y sus funciones OpenGL equivalentes.



| Función GL de IRIS                          | Función OpenGL                                                                               | Significado                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ ON,** params)     | [**glEnable**](glenable.md) ( GL \_ CLIP \_ PLANEi )                                             | Habilita el recorte en el plano i.             |
| **clipplane**( i, **CP \_ DEFINE**, plane ) | [**glClipPlane**](glclipplane.md) (GL \_ CLIP \_ PLANEi, plane )                                | Define el plano de recorte.                  |
|                                           | [**glGetClipPlane**](glgetclipplane.md)                                                      | Devuelve la ecuación del plano de recorte.         |
|                                           | [**glIsEnabled**](glisenabled.md) ( GL \_ CLIP \_ PLANEi )                                       | Devuelve true si el plano de recorte i está habilitado. |
| **scrmask**                               | [**glScissor**](glscissor.md)                                                                | Define el cuadro de verificación.                 |
| **getscrmask**                            | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ DESERTE \_ DE LA CAJA ) | Devuelve el cuadro actual de la torción.         |



 

Para activar la prueba de la estorba, llame **a glEnable** mediante GL \_ \_ LODO BOX como parámetro.

??

 

 




