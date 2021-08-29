---
title: Porte de llamadas de búfer de acumulación
description: Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con las funciones OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Porte de IRIS GL, búferes de acumulación
- porte desde IRIS GL, búferes de acumulación
- porte a OpenGL desde IRIS GL, búferes de acumulación
- Porte de OpenGL desde IRIS GL, búferes de acumulación
- búferes de acumulación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a9e1999da2d76f19f6cc0a4c86072f68a1aa239829edcb3f22bf8c873ed181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936244"
---
# <a name="porting-accumulation-buffer-calls"></a>Porte de llamadas de búfer de acumulación

Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con las funciones **OpenGL auxInitDisplayMode** [**o ChoosePixelFormat.**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) En la tabla siguiente se enumeran las funciones GL de IRIS que afectan al búfer de acumulación y sus funciones openGL equivalentes.



| Función GL de IRIS       | Función OpenGL                                       | Significado                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             | **auxInitDisplayMode** o **ChoosePixelFormat**       | Especifica el número de planos de bits por componente de color en el búfer de acumulación. |
| **acbuf**              | [**glAccum**](glaccum.md)                            | Funciona en el búfer de acumulación.                                          |
|                        | [**glClearAccum**](glclearaccum.md)                  | Establece valores no válidos para el búfer de acumulación.                                    |
| **acbuf**( AC \_ CLEAR ) | [**glClear**](glclear.md) ( GL \_ ACCUM \_ BUFFER BIT \_ ) | Borra el búfer de acumulación.                                               |



 

En la tabla siguiente se enumeran los parámetros **acbuf** de IRIS GL junto con los parámetros [**glAccum de**](glaccum.md) OpenGL equivalentes.



| Parámetro GL de IRIS     | Parámetro OpenGL |
|-----------------------|------------------|
| ACUMULACIÓN \_ DE CA        | GL \_ ACCUM        |
| AC \_ CLEAR \_ ACCUMULATE | GL \_ LOAD         |
| AC \_ RETURN            | GL \_ RETURN       |
| AC \_ MULT              | GL \_ MULT         |
| AC \_ ADD               | GL \_ ADD          |



 

 

 




