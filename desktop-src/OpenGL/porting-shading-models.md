---
title: Trasladar modelos de sombreado
description: Al igual que IRIS GL, OpenGL permite cambiar entre el sombreado suave (Gouraud) y el sombreado plano. En la tabla siguiente se enumeran las funciones de sombreado y interpolación de la contabilidad de IRIS y sus funciones de OpenGL equivalentes.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Migración de la contabilidad de IRIS, sombreado
- portabilidad de IRIS GL, sombreado
- trasladar a OpenGL desde IRIS GL, sombreado
- Exportación de OpenGL desde IRIS GL, sombreado
- sombreado suave
- Sombreado Gouraud
- sombreado plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357354"
---
# <a name="porting-shading-models"></a>Trasladar modelos de sombreado

Al igual que IRIS GL, OpenGL permite cambiar entre el sombreado suave (Gouraud) y el sombreado plano. En la tabla siguiente se enumeran las funciones de sombreado y interpolación de la contabilidad de IRIS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                                   | Función OpenGL                                                                                    | Significado                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(plano)                               | [**glShadeModel**](glshademodel.md) (GL \_ plano)                                                  | Realiza un sombreado plano.           |
| **shademodel**(GOURAUD)                            | **glShadeModel**(GL \_ Smooth)                                                                     | Suaviza el sombreado.         |
| **getsm**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modelo de sombreado de contabilidad \_ )      | Devuelve el modelo de sombra actual. |
| interpolación de **interpolación (DT** \_ en) (DT  \_ OFF) <br/> | [**glEnable**](glenable.md) (interpolación en contab. \_ )[**glDisable**](gldisable.md)( \_ interpolación de contabilidad)<br/> | Activa o desactiva el tramado.      |



 

??

 

 





