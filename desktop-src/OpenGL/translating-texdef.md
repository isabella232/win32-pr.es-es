---
title: Traducción de la definición de la definición
description: El ejemplo de código siguiente es una definición de textura DE IRIS GL
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Porte de IRIS GL, textura
- porting from IRIS GL,texture
- porting to OpenGL from IRIS GL,texture
- Porte de OpenGL desde IRIS GL, textura
- textura
- Porte de IRIS GL,def
- porting from IRIS GL,def
- porting to OpenGL from IRIS GL,def
- Porte de OpenGL desde IRIS GL,def
- defdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361995"
---
# <a name="translating-texdef"></a>Traducción de la definición de la definición

El ejemplo de código siguiente es una definición de textura IRIS GL:


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



En el ejemplo **anterior,def** especifica el filtro TX POINT como filtro de ampliación y minimización, y TX REPEAT como \_ mecanismo de \_ ajuste. También especifica la imagen de textura: textura **de \_ graní.**

En OpenGL, [**glTexImage**](glteximage1d.md) especifica la imagen y [glTexParameter](gltexparameter-functions.md) establece la propiedad . Para traducir definiciones de textura de IRIS GL, reemplace la función **textdef** por **glTexImage** y una o varias llamadas **a glTexParameter**.

El código GL de IRIS anterior tiene este aspecto cuando se traduce a OpenGL:


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



En la tabla siguiente se enumeran los parámetros de textura IRIS GL y sus parámetros OpenGL equivalentes.



| Parámetro de textura IRIS GL | Parámetro de textura OpenGL                                  |
|---------------------------|-----------------------------------------------------------|
| TX \_ MINFILTER             | FILTRO \_ DE TEXTURA MÍNIMA DE \_ \_ GL                                  |
| TX \_ MAGFILTER             | FILTRO GL \_ TEXTURE \_ MAG \_                                  |
| TX \_ WRAP, TX \_ WRAP \_ S     | GL \_ TEXTURE \_ WRAP \_ S                                      |
| TX \_ WRAP, TX \_ WRAP \_ T     | COLOR DEL \_ BORDE DE TEXTURA GL TEXTURE WRAP \_ \_ TGL \_ \_ \_<br/> |



 

En la tabla siguiente se enumeran los valores posibles de los parámetros de textura GL de IRIS y sus parámetros OpenGL equivalentes.



| Parámetro de textura IRIS GL | Parámetro de textura OpenGL     |
|---------------------------|------------------------------|
| TX \_ POINT                 | GL \_ NEAREST                  |
| TX \_ BILINEAR              | GL \_ LINEAR                   |
| TX \_ MIPMAP \_ POINT         | GL \_ NEAREST \_ MIPMAP \_ NEAREST |
| TX \_ MIPMAP \_ BILINEAR      | GL \_ LINEAR \_ MIPMAP \_ NEAREST  |
| TX \_ MIPMAP \_ LINEAR        | GL \_ NEAREST \_ MIPMAP \_ LINEAR  |
| TX \_ TRILINEAR             | GL \_ LINEAR \_ MIPMAP \_ LINEAR   |



 

 

 





