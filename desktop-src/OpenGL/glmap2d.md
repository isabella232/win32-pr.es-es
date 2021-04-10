---
title: Función glMap2d (Gl.h)
description: La función glMap2d define un evaluador bidimensional. | función glMap2d (GL. h)
ms.assetid: d8645d19-bec1-4efd-a657-6e7d52d706a9
keywords:
- glMap2d (función) OpenGL
topic_type:
- apiref
api_name:
- glMap2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e072635c411c7a3e28977316c388a9b1597fcd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279946"
---
# <a name="glmap2d-function"></a>glMap2d función)

Las funciones **glMap2d** y [**glMap2f**](glmap2f.md) definen un evaluador bidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMap2d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    ustride,
         GLint    uorder,
         GLdouble v1,
         GLdouble v2,
         GLint    vstride,
         GLint    vorder,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Tipo de valores generados por el evaluador. Se aceptan las siguientes constantes simbólicas.



| Value                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**\_ \_ Vértice \_ 3 de GL MAP2 (**</dt> </dl>                       | Cada punto de control es tres valores de punto flotante que representan *x, y* y *z*. Los comandos internos de [**glVertex3**](glvertex-functions.md) se generan cuando se evalúa la asignación.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**\_ \_ Vértice \_ 4 de GL MAP2 (**</dt> </dl>                       | Cada punto de control es cuatro valores de punto flotante que representan *x, y, z* y *w*. Los comandos internos de [**glVertex4**](glvertex-functions.md) se generan cuando se evalúa la asignación.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**Índice de GL \_ MAP2 ( \_**</dt> </dl>                                 | Cada punto de control es un valor de punto flotante único que representa un índice de color. Los comandos internos de [**glIndex**](glindex-functions.md) se generan cuando se evalúa la asignación. Sin embargo, el índice actual no se actualiza con el valor de estos comandos **glIndex** .<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 (, \_ color \_ 4**</dt> </dl>                          | Cada punto de control es cuatro valores de punto flotante que representan rojo, verde, azul y alfa. Los comandos internos de [**glColor4**](glcolor-functions.md) se generan cuando se evalúa la asignación. Sin embargo, el color actual no se actualiza con el valor de estos comandos **glColor4** .<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 ( \_ normal**</dt> </dl>                              | Cada punto de control es tres valores de punto flotante que representan los componentes *x, y* y *z* de un vector normal. Los comandos internos de [**glNormal**](glnormal-functions.md) se generan cuando se evalúa la asignación. Sin embargo, la normal actual no se actualiza con el valor de estos comandos **glNormal** .<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1**</dt> </dl> | Cada punto de control es un valor de punto flotante único que representa la coordenada de textura *s* . Los comandos internos de [**glTexCoord1**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**MAP2 (de la textura de GL \_ \_ \_ \_ 2**</dt> </dl> | Cada punto de control son dos valores de punto flotante que representan las coordenadas de textura *s* y *t* . Los comandos internos de [**glTexCoord2**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**MAP2 (de textura de GL \_ \_ \_ \_ 3**</dt> </dl> | Cada punto de control son tres valores de punto flotante que representan las coordenadas de textura *s, t* y *r* . Los comandos internos de [**glTexCoord3**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 ( \_ Texture \_ \_ 4**</dt> </dl> | Cada punto de control es cuatro valores de punto flotante que representan las coordenadas de textura *s, t, r* y *q* . Los comandos internos de [**glTexCoord4**](gltexcoord-functions.md) se generan cuando se evalúa la asignación. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos comandos **glTexCoord** .<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Una asignación lineal de *u*, tal y como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*U2* 
</dt> <dd>

Una asignación lineal de *u*, tal y como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*ustride* 
</dt> <dd>

El número de valores float o Double entre el principio del punto de control **r** *ij* y el principio del punto de **control r** <sub>(i \ + 1 \) \ j</sub>, donde *i* y *j* son los índices de punto de control *u* y *v* , respectivamente. Esto permite que los puntos de control se incrusten en estructuras de datos arbitrarias. La única restricción es que los valores de un punto de control determinado deben ocupar ubicaciones de memoria contiguas.

</dd> <dt>

*uorder* 
</dt> <dd>

La dimensión de la matriz de puntos de control en el eje *u*. Debe ser positivo.

</dd> <dt>

*v1* 
</dt> <dd>

Una asignación lineal de *v*, tal y como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*v2* 
</dt> <dd>

Una asignación lineal de *v*, tal y como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*vstride* 
</dt> <dd>

El número de valores float o Double entre el principio del punto de control **r** *ij* y el principio del punto de **control r** <sub>i (j \ + 1 \)</sub>, donde *i* y *j* son los índices de punto de control *u* y *v* , respectivamente. Esto permite que los puntos de control se incrusten en estructuras de datos arbitrarias. La única restricción es que los valores de un punto de control determinado deben ocupar ubicaciones de memoria contiguas.

</dd> <dt>

*vorder* 
</dt> <dd>

La dimensión de la matriz de puntos de control en el eje *v*. Debe ser positivo.

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
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *U1* era igual a *U2* o *v1* era igual a *V2*.<br/>                                                                         |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *Ustride* o *vstride* era menor que el número de valores de un punto de control.<br/>                                       |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *Uorder* o *Vorder* era menor que uno o el \_ orden Max Max \_ eval \_ .<br/>                                                     |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Los evaluadores proporcionan una manera de utilizar la asignación polinómica o racional para generar vértices, normales, coordenadas de textura y colores. Los valores generados por un evaluador se envían a otras fases del procesamiento de OpenGL como si se hubieran presentado con los comandos [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)y [**glColor**](glcolor-functions.md) , con la excepción de que los valores generados no actualizan el color normal, las coordenadas de textura o el color actual.

Todas las curvas spline polinómicas o racionales de cualquier grado (hasta el máximo admitido por la implementación de OpenGL) se pueden describir mediante evaluadores. Entre ellas se incluyen casi todas las superficies utilizadas en los gráficos de los equipos, incluidas las superficies de spline B, las superficies de NURBS, las superficies de Bézier, etc.

Los evaluadores definen superficies basadas en polinomiales de Bernstein de bivariate. Definir **p** (*u*^,*v*^) como

![Ecuación que muestra la definición de p ().](images/map05.png)

donde **R** *ij* es un punto de control, () es *el polinomio* Bernstein de degree

*n* (*uorder*  =  *n* + 1)

![Ecuación que muestra el polinómico Bernstein de degree n.](images/map06.png)

y () *es el polinomio* Bernstein de degree *m* (*Vorder*  =  *m* + 1)

![Ecuación que muestra el polinómico Bernstein de degree m.](images/map07.png)

Recuerde que

![Ecuaciones que muestran la equivalencia en 1.](images/map08.png)

La función **glMap2** se usa para definir la base y para especificar qué tipo de valores se generan. Una vez definido, una asignación se puede habilitar y deshabilitar llamando a [**glEnable**](glenable.md) y **glDisable** con el nombre de la asignación, uno de los nueve valores predefinidos para el *destino*, descrito anteriormente. Cuando [**glEvalCoord2**](glevalcoord-functions.md) presenta los valores *u* y *v*, los polinómicos Bernstein de bivariate se evalúan usando *u*^ y *v*^, donde

![Ecuación que muestra la definición de ^.](images/map09.png)

y

![Ecuación que muestra la definición de v ^.](images/map10.png)

El parámetro de *destino* es una constante simbólica que indica qué tipo de puntos de control se proporcionan en los *puntos* y qué resultado se genera cuando se evalúa la asignación.

Los parámetros *ustride*, *uorder*, *vstride*, *Vorder* y *Points* definen el direccionamiento de la matriz para tener acceso a los puntos de control. El parámetro *Points* es la ubicación del primer punto de control, que ocupa una, dos, tres o cuatro ubicaciones de memoria contiguas, dependiendo de la asignación que se está definiendo. Hay puntos de control *uorder* x *Vorder* en la matriz. El parámetro *ustride* indica el número de ubicaciones float o Double que se omiten para avanzar el puntero de memoria interno desde el punto de control **r** *ij* hasta el punto de control **r** <sub>(\ i + 1 \) j</sub>. El parámetro *vstride* indica el número de ubicaciones float o Double que se omiten para avanzar el puntero de memoria interno desde el punto de control **r** *ij* hasta el punto de control **r**<sub>i (j \ + 1 \)</sub>.

Como ocurre con todos los comandos de OpenGL que aceptan punteros a datos, es como si el contenido de los *puntos* se copiara mediante **glMap2** antes de devolverse. Los cambios en el contenido de los *puntos* no tienen ningún efecto después de llamar a **glMap2** .

Las siguientes funciones recuperan información relacionada con **glMap2**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ orden de evaluación Max Max \_

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 3

**glIsEnabled** con el argumento GL \_ MAP2 ( \_ Vertex \_ 4

**glIsEnabled** con el argumento GL \_ MAP2 ( \_ index

**glIsEnabled** con el argumento GL \_ MAP2 ( \_ color \_ 4

**glIsEnabled** con el argumento GL \_ MAP2 ( \_ normal

**glIsEnabled** con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1

**glIsEnabled** con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2

**glIsEnabled** con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 3

**glIsEnabled** con el argumento \_ GL \_ MAP2 ( \_ Texture \_ 4

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

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





