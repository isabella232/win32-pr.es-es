---
title: Traducción de tevdef
description: El ejemplo de código siguiente es una definición de entorno de textura DECAL de IRIS que especifica el parámetro de textura y entorno \_ DECAL de TV.
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Porte de IRIS GL, textura
- porting from IRIS GL,texture
- porte a OpenGL desde IRIS GL, textura
- Porte de OpenGL desde IRIS GL, textura
- textura
- Porte de IRIS GL, tevdef
- porting from IRIS GL,tevdef
- porting to OpenGL from IRIS GL,tevdef
- Porte de OpenGL desde IRIS GL,tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361996"
---
# <a name="translating-tevdef"></a>Traducción de tevdef

El ejemplo de código siguiente es una definición de entorno de textura DECAL de IRIS que especifica el parámetro \_ texture-environment de TV DECAL:


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



y el mismo código traducido a OpenGL:


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



En la tabla siguiente se enumeran los parámetros de entorno de textura DE IRIS GL y sus parámetros de OpenGL equivalentes.



| Parámetro GL de IRIS     | Parámetro OpenGL             |
|-----------------------|------------------------------|
| \_TVMODULTE          | \_GLMODULTE                 |
| DECAL \_ DE TV             | GL \_ DECAL                    |
| TV \_ BLEND             | GL \_ BLEND                    |
| COLOR DE \_ TELEVISIÓN             | COLOR DE \_ \_ ENV DE TEXTURA \_ GL      |
| TV \_ ALPHA             | No hay equivalente directo de OpenGL. |
| SELECCIÓN \_ DE COMPONENTE DE \_ TELEVISIÓN | No hay equivalente directo de OpenGL. |



 

Para obtener más información sobre los parámetros de entorno de textura, [**vea glTexEnv**](gltexenv-functions.md).

 

 




