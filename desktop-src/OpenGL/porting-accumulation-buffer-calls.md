---
title: Trasladar llamadas del búfer de acumulación
description: Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con la función auxInitDisplayMode o ChoosePixelFormat de OpenGL.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Migración de la contabilidad de IRIS, búferes de acumulación
- portabilidad de IRIS GL, búferes de acumulación
- portabilidad a OpenGL desde IRIS GL, búferes de acumulación
- Exportación de OpenGL desde IRIS GL, búferes de acumulación
- búferes de acumulación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269427"
---
# <a name="porting-accumulation-buffer-calls"></a>Trasladar llamadas del búfer de acumulación

Debe asignar el búfer de acumulación solicitando el formato de píxel adecuado con la función **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) de OpenGL. En la tabla siguiente se enumeran las funciones de contabilidad de IRIS que afectan al búfer de acumulación y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS       | Función OpenGL                                       | Significado                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             | **auxInitDisplayMode** o **ChoosePixelFormat**       | Especifica el número de bitplanes por componente de color en el búfer de acumulación. |
| **acbuf**              | [**glAccum**](glaccum.md)                            | Funciona en el búfer de acumulación.                                          |
|                        | [**glClearAccum**](glclearaccum.md)                  | Establece valores claros para el búfer de acumulación.                                    |
| **acbuf**(AC \_ claro) | [**glClear**](glclear.md) (bit de búfer de la acumulación de GL \_ \_ \_ ) | Borra el búfer de acumulación.                                               |



 

En la tabla siguiente se enumeran los parámetros de **acbuf** de la contabilidad de iris junto con los parámetros de [**glAccum**](glaccum.md) de OpenGL equivalentes.



| Parámetro de GL de IRIS     | Parámetro de OpenGL |
|-----------------------|------------------|
| acumulación de AC \_        | LIBRO \_ acumulado        |
| acumulación de AC \_ Clear \_ | carga en contab. \_         |
| retorno de CA \_            | devolución de GL \_       |
| AC \_ mult              | \_mult         |
| \_Agregar AC               | \_Agregar GL          |



 

 

 




