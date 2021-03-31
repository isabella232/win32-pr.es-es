---
title: Función glMap1d (Gl.h)
description: La función glMap1d define un evaluador unidimensional. | función glMap1d (GL. h)
ms.assetid: 65f8b099-597c-4300-a7d1-3dabdd19e6cb
keywords:
- glMap1d (función) OpenGL
topic_type:
- apiref
api_name:
- glMap1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35aee409ab814f9ec2f09add79a700fde4b43998
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820522"
---
# <a name="glmap1d-function"></a>glMap1d función)

Las funciones **glMap1d** y [**glMap1f**](glmap1f.md) definen un evaluador unidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMap1d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    stride,
         GLint    order,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Tipo de valores generados por el evaluador. Constantes simbólicas. El parámetro de *destino* es una constante simbólica que indica qué tipo de puntos de control se proporcionan en los *puntos* y qué resultado se genera cuando se evalúa la asignación. Puede suponer uno de los nueve valores predefinidos.



| Value                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**\_ \_ Vértice \_ 3 de GL MAP1**</dt> </dl>                       | Cada punto de control es tres valores de punto flotante que representan *x, y* y *z*. Los comandos internos de [**glVertex3**](glvertex-functions.md) se generan cuando se evalúa la asignación.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**\_ \_ Vértice \_ 4 de GL MAP1**</dt> </dl>                       | Cada punto de control es cuatro valores de punto flotante que representan *x, y, z* y *w*. Los comandos internos de [**glVertex4**](glvertex-functions.md) se generan cuando se evalúa la asignación.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**Índice de GL \_ MAP1 \_**</dt> </dl>                                 | Cada punto de control es un valor de punto flotante único que representa un índice de color. Los comandos internos de [**glIndex**](glindex-functions.md) se generan cuando se evalúa la asignación. Sin embargo, el índice actual no se actualiza con el valor de estos comandos **glIndex** .<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1, \_ color \_ 4**</dt> </dl>                          | Cada punto de control es cuatro valores de punto flotante que representan rojo, verde, azul y alfa. Los comandos internos de [**glColor4**](glcolor-functions.md) se generan cuando se evalúa la asignación. Sin embargo, el color actual no se actualiza con el valor de estos comandos **glColor4** .<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ normal**</dt> </dl>                              | Cada punto de control es tres valores de punto flotante que representan los componentes *x, y* y *z* de un vector normal. Los comandos internos de [**glNormal**](glnormal-functions.md) se generan cuando se evalúa la asignación. Sin embargo, la normal actual no se actualiza con el valor de estos comandos **glNormal** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ coordenadas \_ 1**</dt> </dl> | Cada punto de control es un valor de punto flotante único que representa la coordenada de textura *s* . Los comandos internos de [**glTexCoord1**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**MAP1 de la textura de GL \_ \_ \_ \_ 2**</dt> </dl> | Cada punto de control son dos valores de punto flotante que representan las coordenadas de textura *s* y *t* . Los comandos internos de [**glTexCoord2**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**MAP1 de textura de GL \_ \_ \_ \_ 3**</dt> </dl> | Cada punto de control son tres valores de punto flotante que representan las coordenadas de textura *s, t* y *r* . Los comandos internos de [**glTexCoord3**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ \_ 4**</dt> </dl> | Cada punto de control es cuatro valores de punto flotante que representan las coordenadas de textura *s, t, r* y *q* . Los comandos internos de [**glTexCoord4**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Una asignación lineal de *u*, tal y como se presenta a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, la variable que se evalúa mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*U2* 
</dt> <dd>

Una asignación lineal de *u*, tal y como se presenta a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, la variable que se evalúa mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*STRI* 
</dt> <dd>

Número de valores flotantes o dobles entre el principio de un punto de control y el principio del siguiente de la estructura de datos a la que se hace referencia en *puntos*. Esto permite que los puntos de control se incrusten en estructuras de datos arbitrarias. La única restricción es que los valores de un punto de control determinado deben ocupar ubicaciones de memoria contiguas.

</dd> <dt>

*order* 
</dt> <dd>

Número de puntos de control. Debe ser positivo.

</dd> <dt>

*puntos* 
</dt> <dd>

Puntero a la matriz de puntos de control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* no era un valor aceptado.<br/>                                                                                        |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *U1* era igual a *U2*.<br/>                                                                                                    |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *STRIDE* es menor que el número de valores de un punto de control.<br/>                                                            |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *orden* era menor que uno o el \_ orden de evaluación Max máx \_ \_ .<br/>                                                                         |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Los evaluadores proporcionan una manera de utilizar la asignación polinómica o racional para generar vértices, normales, coordenadas de textura y colores. Los valores generados por un evaluador se envían a otras fases del procesamiento de OpenGL como si se hubieran presentado mediante los comandos [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)y [**glColor**](glcolor-functions.md) , con la excepción de que los valores generados no actualizan el color normal, las coordenadas de textura o el color actual.

Todas las curvas spline polinómicas o racionales de cualquier grado (hasta el máximo admitido por la implementación de OpenGL) se pueden describir mediante evaluadores. Entre ellas se incluyen casi todas las splines utilizadas en los gráficos de los equipos, incluidas las splines B, curvas Bézier, splines Hermite, etc.

Los evaluadores definen curvas basadas en polinómicos Bernstein. Definir **p** () como

![Ecuación que muestra la definición de p ().](images/map01.png)

donde **R**_i_ es un punto de control y () es *el* polinómico Bernstein de degree *n* (*orden*  = *n* + 1):

![Ecuación que muestra el polinómico Bernstein de degree n.](images/map02.png)

Recuerde que

![Ecuaciones que muestran la equivalencia en 1.](images/map03.png)

La función **glMap1** se usa para definir la base y para especificar qué tipo de valores se generan. Una vez definido, se puede habilitar y deshabilitar un mapa llamando a [**glEnable**](glenable.md) y **glDisable** con el nombre de asignación, uno de los nueve valores predefinidos para el *destino* descrito anteriormente. La función [glEvalCoord1](glevalcoord-functions.md) evalúa las asignaciones unidimensionales que están habilitadas. Cuando **glEvalCoord1** presenta un valor *u*, las funciones Bernstein se evalúan mediante *u*^, donde

![Ecuación que muestra la definición de ^.](images/map04.png)

Los parámetros *STRIDE*, *Order* y *Points* definen el direccionamiento de la matriz para tener acceso a los puntos de control. El parámetro *Points* es la ubicación del primer punto de control, que ocupa una, dos, tres o cuatro ubicaciones de memoria contiguas, dependiendo de la asignación que se está definiendo. El parámetro *Order* es el número de puntos de control de la matriz. El parámetro *STRIDE* indica el número de ubicaciones float o Double para avanzar el puntero de memoria interna hasta alcanzar el siguiente punto de control.

Como ocurre con todos los comandos de OpenGL que aceptan punteros a datos, es como si el contenido de los *puntos* se copiara mediante **glMap1** antes de devolverse. Los cambios en el contenido de los *puntos* no tienen ningún efecto después de llamar a **glMap1** .

Las siguientes funciones recuperan información relacionada con **glMap1**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ orden de evaluación Max Max \_

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 3

**glIsEnabled** con el argumento GL \_ MAP1 \_ Vertex \_ 4

**glIsEnabled** con el argumento GL \_ MAP1 \_ index

**glIsEnabled** con el argumento GL \_ MAP1 \_ color \_ 4

**glIsEnabled** con el argumento GL \_ MAP1 \_ normal

**glIsEnabled** con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 1

**glIsEnabled** con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 2

**glIsEnabled** con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 3

**glIsEnabled** con el argumento \_ GL \_ MAP1 \_ Texture \_ 4

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





