---
title: Traducción de texgen
description: La función IRIS GL texgen se traduce a glTexGen para OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Porte de IRIS GL, textura
- porting from IRIS GL,texture
- porte a OpenGL desde IRIS GL, textura
- Porte de OpenGL desde IRIS GL, textura
- textura
- Porte de IRIS GL,texgen
- porting from IRIS GL,texgen
- porting to OpenGL from IRIS GL,texgen
- Porte de OpenGL desde IRIS GL,texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361994"
---
# <a name="translating-texgen"></a>Traducción de texgen

La función IRIS GL **texgen** se traduce [a glTexGen](gltexgen-functions.md) para OpenGL.

Con IRIS GL, se llama a **texgen** dos veces: una vez para establecer el modo y la ecuación de plano simultáneamente, y una vez para habilitar la generación de coordenadas de textura. Por ejemplo:


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



Con OpenGL, realiza tres llamadas: dos a **glTexGen** (una para establecer el modo y otra para establecer la ecuación del plano) y otra para [**glEnable**](glenable.md). Por ejemplo, el equivalente de OpenGL al código GL de IRIS anterior es:


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



En la tabla siguiente se enumeran los nombres de coordenada de textura de IRIS GL y sus equivalentes de OpenGL.



| Coordenada de textura DE IRIS GL | Coordenada de textura OpenGL | glEnable argument   |
|----------------------------|---------------------------|---------------------|
| TX \_ S                      | GL \_ S                     | GL \_ TEXTURE \_ GEN \_ S |
| TX \_ T                      | GL \_ T                     | GL \_ TEXTURE \_ GEN \_ T |
| TX \_ R                      | GL \_ R                     | GL \_ TEXTURE \_ GEN \_ R |
| TX \_ Q                      | GL \_ Q                     | GL \_ TEXTURE \_ GEN \_ Q |



 

En la tabla siguiente se enumeran los modos de generación de textura de IRIS GL y sus modos de textura OpenGL equivalentes y nombres de plano.



| Modo de textura IRIS GL | Modo de textura OpenGL | Nombre del plano OpenGL |
|----------------------|---------------------|-------------------|
| TG \_ LINEAR           | GL \_ OBJECT \_ LINEAR  | GL \_ OBJECT \_ PLANE |
| CONTORNO \_ DE TG          | GL \_ EYE \_ LINEAR     | GL \_ EYE \_ PLANE    |
| TG \_ SPHEREMAP        | MAPA \_ DE GL SPHERE \_     |                   |



 

 

 




