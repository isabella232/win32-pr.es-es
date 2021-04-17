---
title: Traducción de texgen
description: La función de GL de IRIS texgen se traduce en glTexGen para OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
- Migración de la contabilidad de IRIS, texgen
- portabilidad de IRIS GL, texgen
- migración a OpenGL desde IRIS GL, texgen
- Exportación de OpenGL desde IRIS GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665727"
---
# <a name="translating-texgen"></a>Traducción de texgen

La función de GL de IRIS **texgen** se traduce en [glTexGen](gltexgen-functions.md) para OpenGL.

Con IRIS GL, se llama a **texgen** dos veces: una vez para establecer la ecuación de modo y plano simultáneamente, y otra para habilitar la generación de coordenadas de textura. Por ejemplo:


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



Con OpenGL, realiza tres llamadas: dos a **glTexGen** (una vez para establecer el modo y otra para establecer la ecuación de plano) y una a [**glEnable**](glenable.md). Por ejemplo, el equivalente de OpenGL al código de GL de IRIS anterior es:


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



En la tabla siguiente se enumeran los nombres de coordenadas de textura del IRIS y sus equivalentes de OpenGL.



| Coordenada de textura de la contabilidad de IRIS | Coordenadas de textura de OpenGL | argumento glEnable   |
|----------------------------|---------------------------|---------------------|
| TX \_ S                      | GL \_ S                     | GL \_ Texture \_ gen \_ S |
| TX \_ T                      | GL \_ T                     | GL \_ Texture \_ gen \_ T |
| TRANSMISIÓN \_ R                      | GL \_ R                     | GL \_ Texture \_ gen \_ R |
| TX \_ Q                      | libro \_ de contabilidad                     | GL \_ Texture \_ gen \_ p |



 

En la tabla siguiente se enumeran los modos de generación de texturas de IRIS GL y sus nombres de plano y modos de textura OpenGL equivalentes.



| Modo de textura de GL de IRIS | Modo de textura de OpenGL | Nombre del plano OpenGL |
|----------------------|---------------------|-------------------|
| TG \_ lineal           | \_objeto GL \_ lineal  | \_plano del objeto GL \_ |
| Perfil de TG \_          | \_ojo \_ lineal de contabilidad     | \_plano de ojo de contabilidad \_    |
| \_SPHEREMAP TG        | \_mapa de esfera de GL \_     |                   |



 

 

 




