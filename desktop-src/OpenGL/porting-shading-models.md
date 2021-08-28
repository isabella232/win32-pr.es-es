---
title: Porting Shading Models
description: Al igual que IRIS GL, OpenGL le permite cambiar entre sombreado suave (Gouraud) y sombreado plano. En la tabla siguiente se enumeran las funciones de sombreado y dithering de IRIS GL y sus funciones OpenGL equivalentes.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Porte de IRIS GL, sombreado
- porting from IRIS GL,shading
- porte a OpenGL desde IRIS GL, sombreado
- Porte de OpenGL desde IRIS GL, sombreado
- sombreado suave
- Sombreado de Gouraud
- sombreado plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee4265341e17843dbe4752bb51e5728aa54914ec5670c08b6b7921537050a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012043"
---
# <a name="porting-shading-models"></a>Porting Shading Models

Al igual que IRIS GL, OpenGL le permite cambiar entre sombreado suave (Gouraud) y sombreado plano. En la tabla siguiente se enumeran las funciones de sombreado y dithering de IRIS GL y sus funciones OpenGL equivalentes.



| Función IRIS GL                                   | Función OpenGL                                                                                    | Significado                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(FLAT)                               | [**glShadeModel**](glshademodel.md) ( GL \_ FLAT )                                                  | Realiza sombreado plano.           |
| **shademodel**(GOURAUD)                            | **glShadeModel**( GL \_ SMOOTH )                                                                     | Realiza un sombreado suave.         |
| **getsm**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ SHADE \_ MODEL )      | Devuelve el modelo de sombreado actual. |
| **dither**(DT \_ ON) **dither**(DT \_ OFF) <br/> | [**glEnable**](glenable.md) ( GL \_ DITHER )[**glDisable**](gldisable.md)( GL \_ DITHER )<br/> | Activa o desactiva el dithering.      |



 

??

 

 





