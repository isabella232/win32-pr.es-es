---
title: Porte de llamadas de búfer de acumulación
description: Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con la función OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Porte de IRIS GL, búferes de acumulación
- porte desde IRIS GL, búferes de acumulación
- porte a OpenGL desde IRIS GL, búferes de acumulación
- Porte de OpenGL desde IRIS GL, búferes de acumulación
- búferes de acumulación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069304"
---
# <a name="porting-accumulation-buffer-calls"></a>Porte de llamadas de búfer de acumulación

Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con la función **OpenGL auxInitDisplayMode** o [**ChoosePixelFormat.**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) En la tabla siguiente se enumeran las funciones GL de IRIS que afectan al búfer de acumulación y sus funciones OpenGL equivalentes.



| Función IRIS GL       | Función OpenGL                                       | Significado                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             | **auxInitDisplayMode** o **ChoosePixelFormat**       | Especifica el número de planos de bits por componente de color en el búfer de acumulación. |
| **acbuf**              | [**glAccum**](glaccum.md)                            | Funciona en el búfer de acumulación.                                          |
|                        | [**glClearAccum**](glclearaccum.md)                  | Establece valores claros para el búfer de acumulación.                                    |
| **acbuf**( AC \_ CLEAR ) | [**glClear**](glclear.md) ( GL \_ ACCUM \_ BUFFER BIT \_ ) | Borra el búfer de acumulación.                                               |



 

En la tabla siguiente se enumeran los parámetros **acbuf** de IRIS GL junto con los parámetros [**glAccum de**](glaccum.md) OpenGL equivalentes.



| Parámetro GL de IRIS     | Parámetro OpenGL |
|-----------------------|------------------|
| ACUMULACIÓN \_ DE CA        | GL \_ ACCUM        |
| ACUMULACIÓN \_ DE AC CLEAR \_ | CARGA \_ DE GL         |
| AC \_ RETURN            | GL \_ RETURN       |
| AC \_ MULT              | GL \_ MULT         |
| AC \_ ADD               | GL \_ ADD          |



 

 

 




