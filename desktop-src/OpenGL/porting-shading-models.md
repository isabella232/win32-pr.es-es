---
title: Porte de modelos de sombreado
description: Al igual que IRIS GL, OpenGL permite cambiar entre sombreado suave (Gouraud) y sombreado plano. En la tabla siguiente se enumeran las funciones de sombreado y dithering de IRIS GL y sus funciones OpenGL equivalentes.
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
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073988"
---
# <a name="porting-shading-models"></a>Porte de modelos de sombreado

Al igual que IRIS GL, OpenGL permite cambiar entre sombreado suave (Gouraud) y sombreado plano. En la tabla siguiente se enumeran las funciones de sombreado y dithering de IRIS GL y sus funciones OpenGL equivalentes.



| Función GL de IRIS                                   | Función OpenGL                                                                                    | Significado                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(FLAT)                               | [**glShadeModel**](glshademodel.md) ( GL \_ FLAT )                                                  | Realiza sombreado plano.           |
| **shademodel**(GOURAUD)                            | **glShadeModel**( GL \_ SMOOTH )                                                                     | Realiza sombreado suave.         |
| **getsm**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ SHADE \_ MODEL )      | Devuelve el modelo de sombreado actual. |
| **dither**(DT \_ ON) **dither**(DT \_ OFF) <br/> | [**glEnable**](glenable.md) ( GL \_ DITHER )[**glDisable**](gldisable.md)( GL \_ DITHER )<br/> | Activa o desactiva la dithering.      |



 

??

 

 





