---
title: función glLightModelf (GL. h)
description: La función glLightModelf establece los parámetros del modelo de iluminación.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- glLightModelf (función) OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2c17f7dc82080544a9055805cf62726227c200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078894"
---
# <a name="gllightmodelf-function"></a>glLightModelf función)

La función **glLightModelf** establece los parámetros del modelo de iluminación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PName* 
</dt> <dd>

Un parámetro de modelo de iluminación de un solo valor. Se aceptan los siguientes valores.



| Value                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**\_ \_ \_ visor local del modelo \_ de contabilidad solar**</dt> </dl> | El parámetro *param* es un valor de punto flotante único que especifica cómo se calculan los ángulos de reflexión especular. Si *param* es 0 (o 0,0), los ángulos de reflexión especular toman la dirección de la vista para que sea paralela a y en la dirección del eje-*z* , independientemente de la ubicación del vértice en coordenadas de ojo. De lo contrario, las reflexiones especulares se calculan a partir del origen del sistema de coordenadas ocular. El valor predeterminado es 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**modelo de la luz de contabilidad \_ \_ \_ dos \_ lados**</dt> </dl>             | El parámetro *param* es un valor de punto flotante único que especifica si se realizan cálculos de iluminación de un lado o dos lados para los polígonos. No tiene ningún efecto en los cálculos de iluminación de puntos, líneas o mapas de bits. Si *param* es 0 (o 0,0), se especifica una iluminación de un lado y solo se usan los parámetros de material frontal en la ecuación de iluminación. De lo contrario, se especifica la iluminación a dos caras. <br/> En este caso, los vértices de los polígonos hacia delante se iluminan con los parámetros del material de fondo y se invierten sus normales antes de que se evalúe la ecuación de iluminación. Los vértices de los polígonos frontales siempre se iluminan mediante los parámetros de material frontal, sin cambiar sus normales. El valor predeterminado es 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor en el que se establecerá el *parámetro* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *PName* no era un valor aceptado.<br/>                                                                                         |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glLightModelf** establece el parámetro del modelo de iluminación. El parámetro *PName* nombra un parámetro y *param* proporciona el nuevo valor. el valor o los valores de los parámetros individuales de origen de la luz.

En el modo RGBA, el color claro de un vértice es la suma de la intensidad de la emisión material, el producto de la reflectancia ambiente material y el modelo de iluminación intensidad de ambiente completo de la escena y la contribución de cada fuente de luz habilitada. Cada fuente de luz contribuye a la suma de tres términos: ambiente, difuso y especular.

-   La contribución de origen de luz ambiente es el producto de la reflectancia ambiente material y la intensidad ambiente de la luz.
-   La contribución de fuente de luz difusa es el producto de la reflectancia difusa del material, la intensidad difusa de la luz y el producto de punto del vértice normal con el vector normalizado del vértice al origen de la luz.
-   La contribución de origen de la luz especular es el producto de la reflexión especular de material, la intensidad especular de la luz y el producto de punto de los vectores de vértice a ojo y de vértice a luz normalizados, elevados a la potencia del brillo del material.

Las tres contribuciones de fuente luminosa se atenúan equitativamente en función de la distancia entre el vértice y el origen de la luz y en la dirección de la fuente de luz, el exponente y el ángulo límite de propagación. Todos los productos dot se sustituyen por cero si se evalúan como un valor negativo.

El componente alfa del color claro resultante se establece en el valor alfa del reflejo difuso de material.

En el modo de índice de color, el valor del índice claro de un vértice varía entre el ambiente y los valores especulares pasados a [**glMaterial**](glmaterial-functions.md) con los índices de color de GL \_ \_ . Los coeficientes difusos y especulares, calculados con una ponderación de (. 30,. 59, .11) de los colores de la luz, el brillo del material y las mismas ecuaciones de reflexión y atenuación que en el caso RGBA, determinan la cantidad de ambiente más allá del que se encuentra el índice resultante.

Las siguientes funciones recuperan información relacionada con la función **glLightModelf** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ \_ visor local del modelo de contabilidad solar \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ del modelo \_ \_ de la vista de contabilidad

[**glIsEnabled**](glisenabled.md) con iluminación de GL de argumento \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
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

 

 





