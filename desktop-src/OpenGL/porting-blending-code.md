---
title: Porting Blending Code
description: En IRIS GL, al dibujar en los búferes frontal y posterior, la combinación se realiza mediante la lectura de uno de los búferes, la combinación con ese color y, a continuación, la escritura del resultado en ambos búferes. Sin embargo, en OpenGL, cada búfer se lee a su vez, se combina y, a continuación, se escribe.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Porte de IRIS GL, combinación
- porting from IRIS GL,blending
- porting to OpenGL from IRIS GL,blending
- Porte de OpenGL desde IRIS GL, blending
- combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13548a2f08821e4f80bf63230077f9a39540ba9b8a37763e7935d211ef0dcdc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485915"
---
# <a name="porting-blending-code"></a>Porting Blending Code

En IRIS GL, al dibujar en los búferes frontal y posterior, la combinación se realiza mediante la lectura de uno de los búferes, la combinación con ese color y, a continuación, la escritura del resultado en ambos búferes. Sin embargo, en OpenGL, cada búfer se lee a su vez, se combina y, a continuación, se escribe.

En la tabla siguiente se enumeran las funciones de combinación de IRIS GL y sus funciones OpenGL equivalentes.



| Función GL de IRIS  | Función OpenGL                            | Significado                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) ( GL \_ BLEND ) | Activa la combinación.          |
| **blendfunction** | [**glBlendFunc**](glblendfunc.md)         | Especifica una función blend. |



 

La función **GlBlendFunc** de OpenGL y la función **blendfunction de** IRIS GL son casi idénticas. En la tabla siguiente se enumeran los factores de combinación de IRIS GL y sus equivalentes de OpenGL.



| IRIS GL          | Opengl                     | Notas             |
|------------------|----------------------------|-------------------|
| BF \_ ZERO         | GL \_ ZERO                   |                   |
| BF \_ ONE          | GL \_ ONE                    |                   |
| BF \_ SA           | GL \_ SRC \_ ALPHA             |                   |
| BF \_ MSA          | GL \_ ONE \_ MENOS \_ SRC \_ ALPHA |                   |
| BF \_ DA           | GL \_ DST \_ ALPHA             |                   |
| MDA de \_ BF          | GL \_ ONE \_ MENOS \_ DST \_ ALPHA |                   |
| BF \_ SC           | GL \_ SRC \_ COLOR             |                   |
| MSC \_ de BF          | GL \_ ONE MENOS COLOR \_ \_ SRC \_ | Solo destino. |
| Controlador de dominio de BF \_           | GL \_ DST \_ COLOR             | Solo origen.      |
| MDC \_ de BF          | GL \_ ONE MENOS COLOR \_ \_ DST \_ | Solo origen.      |
| BF \_ MIN \_ SA \_ MDA | SATURACIÓN ALFA de GL \_ SRC \_ \_   |                   |



 

??

 

 




