---
title: Trasladar código de fusión
description: En la contabilidad de IRIS, al dibujar en los búferes frontal y posterior, la combinación se realiza mediante la lectura de uno de los búferes, la fusión con ese color y la posterior escritura del resultado en ambos búferes. En OpenGL, sin embargo, cada búfer se lee a su vez, se mezcla y se escribe.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Migración de la contabilidad de IRIS, fusión
- portabilidad de IRIS GL, fusión
- trasladar a OpenGL desde IRIS GL, fusión
- Exportación de OpenGL desde IRIS GL, fusión
- combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665719"
---
# <a name="porting-blending-code"></a>Trasladar código de fusión

En la contabilidad de IRIS, al dibujar en los búferes frontal y posterior, la combinación se realiza mediante la lectura de uno de los búferes, la fusión con ese color y la posterior escritura del resultado en ambos búferes. En OpenGL, sin embargo, cada búfer se lee a su vez, se mezcla y se escribe.

En la tabla siguiente se enumeran las funciones de fusión en GL de IRIS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS  | Función OpenGL                            | Significado                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) (GL \_ Blend) | Activa la fusión.          |
| **blendfunction** | [**glBlendFunc**](glblendfunc.md)         | Especifica una función de Blend. |



 

La función **glBlendFunc** de OpenGL y la función **BLENDFUNCTION** de la contabilidad de iris son casi idénticas. En la tabla siguiente se enumeran los factores de mezcla de IRIS GL y sus equivalentes de OpenGL.



| IRIS GL          | OpenGL                     | Notas             |
|------------------|----------------------------|-------------------|
| BF \_ cero         | GL \_ cero                   |                   |
| BF \_ uno          | GL \_ uno                    |                   |
| SA de BF \_           | CC \_ src \_ alfa             |                   |
| BF \_ MSA          | GL \_ uno \_ menos \_ src \_ Alpha |                   |
| BF \_ da           | GL \_ DST \_ Alpha             |                   |
| MDA de BF \_          | GL \_ uno \_ menos \_ DST \_ Alpha |                   |
| BF \_ SC           | \_color de origen del libro de contabilidad \_             |                   |
| BF \_ MSC          | GL \_ uno \_ menos \_ el \_ color src | Solo destino. |
| BF \_ DC           | \_color de DST de GL \_             | Solo origen.      |
| MDC de BF \_          | GL \_ uno \_ menos \_ el \_ color de DST | Solo origen.      |
| \_MDA del mínimo \_ SA \_ de BF | libro de contabilidad \_ orig \_ alfa \_ saturado   |                   |



 

??

 

 




