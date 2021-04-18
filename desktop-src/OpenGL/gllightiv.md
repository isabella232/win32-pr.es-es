---
title: función glLightiv (GL. h)
description: La función glLightiv devuelve los valores de los parámetros de origen de la luz.
ms.assetid: 927f6a7e-be42-46ab-9c23-6ce87f96bd8a
keywords:
- glLightiv (función) OpenGL
topic_type:
- apiref
api_name:
- glLightiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c70e991cf96ed5d3565e1b6c9522693786cca80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685859"
---
# <a name="gllightiv-function"></a>glLightiv función)

La función **glLightiv** devuelve los valores de los parámetros de origen de la luz.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLightiv(
         GLenum light,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*light* 
</dt> <dd>

Identificador de una luz. El número de posibles luces depende de la implementación, pero se admiten al menos ocho luces. Se identifican por nombres simbólicos con el formato GL \_ Light *i* , donde *i* es un valor: 0 a las \_ \_ luces Max de GL-1.

</dd> <dt>

*PName* 
</dt> <dd>

Parámetro de origen de luz para *Light*. Se aceptan los siguientes nombres simbólicos.



| Value                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**ambiente de contabilidad general \_**</dt> </dl>                                                                                                                                                                                                | El parámetro *params* contiene cuatro valores enteros que especifican la intensidad RGBA ambiente de la luz. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los valores de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. La intensidad de luz ambiente predeterminada es (0,0, 0,0, 0,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**difusión en contab. \_**</dt> </dl>                                                                                                                                                                                                | El parámetro *params* contiene cuatro valores enteros que especifican la intensidad RGBA difusa de la luz. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los valores de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. La intensidad difusa predeterminada es (0,0, 0,0, 0,0, 1,0) para todas las luces distintas de la luz cero. La intensidad difusa predeterminada del cero claro es (1,0, 1,0, 1,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_especular GL**</dt> </dl>                                                                                                                                                                                             | El parámetro *params* contiene cuatro valores enteros que especifican la intensidad del RGBA especular de la luz. Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a 1,0. Los valores de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. La intensidad especular predeterminada es (0,0, 0,0, 0,0, 1,0) para todas las luces distintas de la luz cero. La intensidad especular predeterminada del cero claro es (1,0, 1,0, 1,0, 1,0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**posición de contabilidad \_**</dt> </dl>                                                                                                                                                                                             | El parámetro *params* contiene cuatro valores enteros que especifican la posición de la luz en coordenadas de objeto homogéneas. Los valores enteros y de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. <br/> La matriz MODELVIEW transforma la posición cuando se llama a [**glLightiv**](gllightfv.md) (al igual que si fuera un punto) y se almacena en coordenadas de ojo. Si el componente *w* de la posición es 0,0, la luz se trata como un origen direccional. Los cálculos de iluminación difusa y especular toman la dirección de la luz, pero no su posición real, en cuenta, y la atenuación está deshabilitada. De lo contrario, los cálculos de iluminación difusa y especular se basan en la ubicación real de la luz en coordenadas de ojo y la atenuación está habilitada. La posición predeterminada es (0, 0, 1, 0); por lo tanto, la fuente de luz predeterminada es direccional, paralela a y en la dirección del eje-*z* .<br/> |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**Dirección de la zona de contabilidad \_ \_**</dt> </dl>                                                                                                                                                                          | El parámetro *params* contiene tres valores enteros que especifican la dirección de la luz en coordenadas de objeto homogéneas. Los valores enteros y de punto flotante se asignan directamente. Ninguno de los valores enteros ni de punto flotante está fijado. <br/> La dirección del punto se transforma por el inverso de la matriz de MODELVIEW cuando se llama a **glLightiv** (como si fuera un normal) y se almacena en coordenadas de ojo. Solo es importante cuando \_ el límite de la zona de contabilidad \_ no es 180, que es el valor predeterminado. La dirección predeterminada es (0, 0, 1).<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**exponente de la zona de contabilidad \_ \_**</dt> </dl>                                                                                                                                                                             | El parámetro *params* es un valor entero único que especifica la distribución de la intensidad de la luz. Los valores enteros y de punto flotante se asignan directamente. Solo se aceptan los valores del intervalo comprendido entre \[ 0 y 128 \] . <br/> La intensidad de la luz efectiva se atenúa por el coseno del ángulo entre la dirección de la luz y la dirección de la luz hasta el vértice que se ilumina, elevado a la potencia del exponente del punto. Por lo tanto, los exponentes más altos producen una fuente de luz más enfocada, independientemente del ángulo de corte puntual. El exponente de color predeterminado es 0, lo que da lugar a una distribución ligera uniforme.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**límite de la zona de contabilidad \_ \_**</dt> </dl>                                                                                                                                                                                   | El parámetro *params* es un valor entero único que especifica el ángulo de propagación máximo de una fuente de luz. Los valores enteros y de punto flotante se asignan directamente. Solo se aceptan los valores del intervalo \[ 0, 90 \] y el valor especial 180. <br/> Si el ángulo entre la dirección de la luz y la dirección desde la luz hasta el vértice que se ilumina es mayor que el ángulo límite de la zona, la luz se enmascara completamente. De lo contrario, su intensidad se controla mediante el exponente puntual y los factores de atenuación. El límite de la luz predeterminada es 180, lo que da lugar a una distribución ligera uniforme.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**\_ \_ atenuación de constantes de contabilidad \_ , \_ atenuación lineal de contabilidad, \_ atenuación cuadrática de GL \_**</dt> </dl> | El parámetro *params* es un valor entero único que especifica uno de los tres factores de atenuación de luz. Los valores enteros y de punto flotante se asignan directamente. Solo se aceptan valores no negativos. <br/> Si la luz es posicional, en lugar de direccional, su intensidad se atenúa por el recíproco de la suma de: el factor constante, el factor lineal multiplicado por la distancia entre la luz y el vértice que se está iluminando, y el factor cuadrático multiplicado por el cuadrado de la misma distancia. Los factores de atenuación predeterminados son (1, 0, 0), lo que da lugar a no atenuación.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Especifica el valor en el que se establecerá el parámetro *PName* de *luz* de origen de luz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *Light* o *PName* no era un valor aceptado.<br/>                                                                                                                                                                  |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | Se especificó un valor de exponente puntual fuera del intervalo \[ 0, 128 \] o el límite de la zona se especificó fuera del intervalo comprendido entre \[ 0 y 90 \] (excepto el valor especial 180), o bien se especificó un factor de atenuación negativo.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                                                                     |



## <a name="remarks"></a>Observaciones

La función **glLightiv** establece el valor o los valores de los parámetros individuales de origen de la luz. El parámetro de *luz* asigna un nombre a la luz y es un nombre simbólico con el formato GL \_ Light *i*, donde 0 = *i* < las luces de contab \_ \_ .

El parámetro *PName* especifica uno de los parámetros de origen de la luz, de nuevo por nombre simbólico. El parámetro *params* es un valor único o un puntero a una matriz que contiene los nuevos valores.

El cálculo de iluminación está habilitado y deshabilitado mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con iluminación de contabilidad de argumentos \_ . Cuando está habilitada la iluminación, las fuentes de luz que están habilitadas contribuyen al cálculo de iluminación. La fuente de luz *i* está habilitada y deshabilitada mediante **glEnable** y **glDisable** con el argumento GL \_ Light *i*.

Siempre es el caso de GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Las siguientes funciones recuperan información relacionada con la función **glLightiv** :

[**glGetLight**](glgetlight.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





