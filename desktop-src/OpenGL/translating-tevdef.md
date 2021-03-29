---
title: Traducción de tevdef
description: El siguiente ejemplo de código es una definición de entorno de textura de la contabilidad de IRIS que especifica el \_ parámetro Decal Texture-Environment.
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
- Migración de la contabilidad de IRIS, tevdef
- portabilidad de IRIS GL, tevdef
- migración a OpenGL desde IRIS GL, tevdef
- Exportación de OpenGL desde IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994544"
---
# <a name="translating-tevdef"></a>Traducción de tevdef

El siguiente ejemplo de código es una definición de entorno de textura de la contabilidad de IRIS que especifica el \_ parámetro Decal Texture-Environment:


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



y el mismo código traducido a OpenGL:


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



En la tabla siguiente se enumeran los parámetros de entorno de textura GL de IRIS y sus parámetros de OpenGL equivalentes.



| Parámetro de GL de IRIS     | Parámetro de OpenGL             |
|-----------------------|------------------------------|
| TV \_ modular          | \_modular GL                 |
| Calcomanía de TV \_             | \_marcas GL                    |
| TV \_ Blend             | fusión de contabilidad \_                    |
| COLOR de TV \_             | \_color de textura de libro de contabilidad \_ \_      |
| TV \_ Alpha             | No es equivalente de OpenGL directo. |
| \_selección de componentes de TV \_ | No es equivalente de OpenGL directo. |



 

Para obtener más información sobre los parámetros de entorno de textura, vea [**glTexEnv**](gltexenv-functions.md).

 

 




