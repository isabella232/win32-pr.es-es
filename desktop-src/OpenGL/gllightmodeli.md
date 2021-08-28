---
title: Función glLightModeli (Gl.h)
description: La función glLightModeli establece los parámetros del modelo de iluminación.
ms.assetid: 49975166-b2b3-47f9-8305-aea2ba364546
keywords:
- Función glLightModeli OpenGL
topic_type:
- apiref
api_name:
- glLightModeli
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0985df04d77a606535d5791e52ea90784a34ed3ef38ac2810840353a68b67539
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493095"
---
# <a name="gllightmodeli-function"></a>Función glLightModeli

La [**función glLightModeli**](gllightf.md) establece los parámetros del modelo de iluminación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLightModeli(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pname* 
</dt> <dd>

Parámetro de modelo de iluminación de un solo valor. Se aceptan los valores siguientes.



| Valor                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**VISOR \_ LOCAL DE GL LIGHT \_ MODEL \_ \_**</dt> </dl> | El *parámetro param* es un valor entero único que especifica cómo se calculan los ángulos de reflexión especular. Si *param* es 0 (o 0,0), los ángulos de reflexión especular toman la dirección de la vista para que sea paralela y en la dirección del eje *- z,* independientemente de la ubicación del vértice en coordenadas de los ojos. De lo contrario, las reflexión especulares se calculan desde el origen del sistema de coordenadas oculares. El valor predeterminado es 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE**</dt> </dl>             | El *parámetro param* es un valor entero único que especifica si los cálculos de iluminación de una o dos lados se realizan para polígonos. No tiene ningún efecto en los cálculos de iluminación para puntos, líneas o mapas de bits. Si *el parámetro* es 0 (o 0,0), se especifica la iluminación de una cara y solo se usan los parámetros de material frontal en la ecuación de iluminación. De lo contrario, se especifica iluminación de dos lados. <br/> En este caso, los vértices de los polígonos orientados hacia atrás se encienden mediante los parámetros de material posterior y se invierten sus normales antes de evaluar la ecuación de iluminación. Los vértices de los polígonos orientados al frente siempre se encienden con los parámetros de material frontal, sin cambios en sus normales. El valor predeterminado es 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor en el que *se establecerá el* parámetro .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *pname* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glLightModeli** establece el parámetro del modelo de iluminación. El *parámetro pname* nombra un parámetro y *param* proporciona el nuevo valor.el valor o los valores de los parámetros de origen de luz individuales.

En el modo RGBA, el color claro de un vértice es la suma de la intensidad de emisión del material, el producto de la reflexión ambiental del material y la intensidad ambiental de la escena completa del modelo de iluminación, y la contribución de cada fuente de luz habilitada. Cada fuente de luz aporta la suma de tres términos: ambiente, difuso y especular.

-   La contribución de la fuente de luz ambiente es el producto de la reflexión ambiental material y la intensidad ambiente de la luz.
-   La contribución de la fuente de luz difusa es el producto de la reflectancia difusa del material, la intensidad difusa de la luz y el producto de punto de la normal del vértice con el vector normalizado desde el vértice hasta la fuente de luz.
-   La contribución de la fuente de luz especular es el producto de la reflectancia especular del material, la intensidad especular de la luz y el producto de punto de los vectores de vértice a ojo normalizados y de vértice a luz, elevados a la potencia de la intensidad del material.

Las tres contribuciones de la fuente de luz se atenuan igualmente en función de la distancia entre el vértice y la fuente de luz y en la dirección de la fuente de luz, el exponente de propagación y el ángulo de límite de propagación. Todos los productos de punto se reemplazan por cero si se evalúan como un valor negativo.

El componente alfa del color claro resultante se establece en el valor alfa de la reflectancia difusa del material.

En el modo de índice de color, el valor del índice claro de un vértice oscila entre el ambiente y los valores especulares pasados a [**glMaterial**](glmaterial-functions.md) mediante GL \_ COLOR \_ INDEXES. Los coeficientes difusos y especulares, calculados con una ponderación (.30, .59, .11) de los colores de la luz, la luminosidad del material y las mismas ecuaciones de reflexión y atenuación que en el caso RGBA, determinan cuánto por encima del ambiente se encuentra el índice resultante.

Las siguientes funciones recuperan información relacionada con **la función glLightModeli:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ LIGHT MODEL LOCAL \_ \_ \_ VIEWER

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ LIGHT MODEL TWO \_ \_ \_ SIDE

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ LIGHTING

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





