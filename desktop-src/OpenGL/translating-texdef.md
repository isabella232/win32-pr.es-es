---
title: Traducción de texdef
description: El ejemplo de código siguiente es una definición de textura de la contabilidad de IRIS
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
- Migración de la contabilidad de IRIS, texdef
- portabilidad de IRIS GL, texdef
- migración a OpenGL desde IRIS GL, texdef
- Exportación de OpenGL desde IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903807"
---
# <a name="translating-texdef"></a>Traducción de texdef

El siguiente ejemplo de código es una definición de textura de GL de IRIS:


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



En el ejemplo anterior, **texdef** especifica el \_ filtro de punto TX como el filtro de ampliación y reducción, y TX \_ REPEAT como mecanismo de ajuste. También especifica la imagen de textura: **granito \_ Texture**.

En OpenGL, [**glTexImage**](glteximage1d.md) especifica la imagen y [glTexParameter](gltexparameter-functions.md) establece la propiedad. Para traducir las definiciones de textura de la contabilidad de IRIS, reemplace la función **textdef** por **glTexImage** y una o varias llamadas a **glTexParameter**.

El código de GL del IRIS anterior tiene este aspecto cuando se traduce a OpenGL:


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



En la tabla siguiente se enumeran los parámetros de textura de la contabilidad de IRIS y sus parámetros de OpenGL equivalentes.



| Parámetro de textura de GL de IRIS | Parámetro de textura OpenGL                                  |
|---------------------------|-----------------------------------------------------------|
| TX \_ MINFILTER             | \_ \_ filtro mínimo de textura de GL \_                                  |
| TX \_ MAGFILTER             | \_filtro de textura de GL \_ \_                                  |
| \_encapsulado de TX \_ , encapsulado de TX \_     | \_ajuste de textura de GL \_ \_                                      |
| \_encapsulado TX, \_ encapsulado de TX \_ T     | \_color de \_ \_ borde de textura de TGL de ajuste \_ de \_ textura de GL \_<br/> |



 

En la tabla siguiente se enumeran los posibles valores de los parámetros de textura GL de IRIS y sus parámetros de OpenGL equivalentes.



| Parámetro de textura de GL de IRIS | Parámetro de textura OpenGL     |
|---------------------------|------------------------------|
| punto de transmisión \_                 | libro de contabilidad \_ más próximo                  |
| TX \_ BIlineal              | CONTABILIDAD \_ lineal                   |
| \_punto de MIPMAP de TX \_         | \_MIP más cercano de GL \_ \_ más cercano |
| fotoline MIP de TX \_ \_      | \_MIP lineal de GL \_ \_ más cercano  |
| \_MIP \_ lineal de TX        | el \_ \_ MIP \_ lineal más cercano de contabilidad  |
| TX \_ TRIlineal             | MIP lineal de contabilidad general \_ \_ \_   |



 

 

 





