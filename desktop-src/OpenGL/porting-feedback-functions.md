---
title: Trasladar funciones de comentarios
description: Con IRIS GL, el modo en que se trata la información se diferencia según el equipo que ejecuta IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Migración de la contabilidad de IRIS, comentarios
- portabilidad de IRIS GL, comentarios
- trasladar a OpenGL desde IRIS GL, comentarios
- Exportación de OpenGL desde IRIS GL, comentarios
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269168"
---
# <a name="porting-feedback-functions"></a>Trasladar funciones de comentarios

Con IRIS GL, el modo en que se trata la información se diferencia según el equipo que ejecuta IRIS GL. OpenGL normaliza las funciones de comentarios para que pueda confiar en la información coherente entre varias plataformas de hardware. En la tabla siguiente se enumeran las funciones de comentarios de la contabilidad de IRIS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS | Función OpenGL                                                                                            | Significado                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **los**     | [**glRenderMode**](glrendermode.md) (comentarios de contabilidad \_ )                                                      | Cambia al modo de comentarios.                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) (representación en GL \_ )[**glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | Cambia al modo de representación.                   |
| **acceso directo**  | [**glPassThrough**](glpassthrough.md)                                                                     | Coloca un marcador de token en el búfer de comentarios. |



 

 

 





