---
title: Porting Feedback Functions
description: Con IRIS GL, la forma en que se administran los comentarios difiere en función del equipo que ejecuta IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Porte de IRIS GL, comentarios
- porting from IRIS GL,feedback
- porting to OpenGL from IRIS GL,feedback
- Porte de OpenGL desde IRIS GL, comentarios
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f4ab584dfbd9038d45e7d24c006857f278a9239fc6f9da4d38a75363f0d585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132637"
---
# <a name="porting-feedback-functions"></a>Porting Feedback Functions

Con IRIS GL, la forma en que se administran los comentarios difiere en función del equipo que ejecuta IRIS GL. OpenGL estandariza las funciones de comentarios para que pueda confiar en comentarios coherentes entre varias plataformas de hardware. En la tabla siguiente se enumeran las funciones de comentarios de IRIS GL y sus funciones openGL equivalentes.



| Función IRIS GL | Función OpenGL                                                                                            | Significado                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **Comentarios**     | [**glRenderMode**](glrendermode.md) ( GL \_ FEEDBACK )                                                      | Cambia al modo de comentarios.                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) ( GL \_ RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | Cambia al modo de representación.                   |
| **Passthrough**  | [**glPassThrough**](glpassthrough.md)                                                                     | Coloca un marcador de token en el búfer de comentarios. |



 

 

 





