---
title: Función glMap2f (Gl.h)
description: La función glMap2f define un evaluador bidimensional. | Función glMap2f (Gl.h)
ms.assetid: 804fbf65-98a8-41af-8c39-5b83f3d341b0
keywords:
- Función glMap2f OpenGL
topic_type:
- apiref
api_name:
- glMap2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152183ced46b55bcdf2038399583c1ecac8c5678
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272076"
---
# <a name="glmap2f-function"></a>Función glMap2f

Las [**funciones glMap2d**](glmap2d.md) **y glMap2f** definen un evaluador bidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMap2f(
         GLenum  target,
         GLfloat u1,
         GLfloat u2,
         GLint   ustride,
         GLint   uorder,
         GLfloat v1,
         GLfloat v2,
         GLint   vstride,
         GLint   vorder,
   const GLfloat *points
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Tipo de valores generados por el evaluador. Se aceptan las siguientes constantes simbólicas.



| Value                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 3**</dt> </dl>                       | Cada punto de control es tres valores de punto flotante que *representan x, y y* *z.* Los [**comandos glVertex3**](glvertex-functions.md) internos se generan cuando se evalúa el mapa.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 4**</dt> </dl>                       | Cada punto de control es de cuatro valores de punto flotante que *representan x, y, z y* *w.* Los [**comandos glVertex4**](glvertex-functions.md) internos se generan cuando se evalúa el mapa.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ MAP2 \_ INDEX**</dt> </dl>                                 | Cada punto de control es un valor de punto flotante único que representa un índice de color. Los [**comandos internos glIndex**](glindex-functions.md) se generan cuando se evalúa el mapa. Sin embargo, el índice actual no se actualiza con el valor de estos **comandos glIndex.**<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 \_ COLOR \_ 4**</dt> </dl>                          | Cada punto de control es de cuatro valores de punto flotante que representan rojo, verde, azul y alfa. Los [**comandos glColor4**](glcolor-functions.md) internos se generan cuando se evalúa el mapa. Sin embargo, el color actual no se actualiza con el valor de estos **comandos glColor4.**<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 \_ NORMAL**</dt> </dl>                              | Cada punto de control es tres valores de punto flotante que representan los *componentes x, y* y *z* de un vector normal. Los [**comandos glNormal**](glnormal-functions.md) internos se generan cuando se evalúa el mapa. Sin embargo, la normal actual no se actualiza con el valor de estos **comandos glNormal.**<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1**</dt> </dl> | Cada punto de control es un valor de punto flotante único que representa la *coordenada* de textura de . Los [**comandos internos glTexCoord1**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de **estos comandos glTexCoord.**<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2**</dt> </dl> | Cada punto de control es dos valores de punto flotante que representan las *coordenadas de* textura s y *t.* Los [**comandos internos glTexCoord2**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de **estos comandos glTexCoord.**<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3**</dt> </dl> | Cada punto de control es tres valores de punto flotante que representan las coordenadas de textura *s, t* y *r.* Los [**comandos internos glTexCoord3**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de **estos comandos glTexCoord.**<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4**</dt> </dl> | Cada punto de control son cuatro valores de punto flotante que representan las coordenadas de textura *s, t, r* y *q.* Los [**comandos internos glTexCoord4**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de **estos comandos glTexCoord.**<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Asignación lineal de *u*, como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*u2* 
</dt> <dd>

Asignación lineal de *u*, como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*ustride* 
</dt> <dd>

El número de flotantes o dobles entre el principio del punto de control **R** *ij* y el principio del punto de control **R** <sub>(i\ +1\ )\ j</sub>, donde *i* y *j* son los índices de punto de control *u* y *v,* respectivamente. Esto permite incrustar puntos de control en estructuras de datos arbitrarias. La única restricción es que los valores de un punto de control determinado deben ocupar ubicaciones de memoria contiguas.

</dd> <dt>

*uorder* 
</dt> <dd>

Dimensión de la matriz de puntos de control en *el eje u.* Debe ser positivo.

</dd> <dt>

*v1* 
</dt> <dd>

Una asignación lineal de *v*, como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*v2* 
</dt> <dd>

Una asignación lineal de *v*, como se presenta a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, una de las dos variables que se evalúan mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*vstride* 
</dt> <dd>

El número de flotantes o dobles entre el principio del punto de control **R** *ij* y el principio del punto de control **R** <sub>i(j\ +1\),</sub>donde *i* y *j* son los índices de punto de control *u* y *v,* respectivamente. Esto permite incrustar puntos de control en estructuras de datos arbitrarias. La única restricción es que los valores de un punto de control determinado deben ocupar ubicaciones de memoria contiguas.

</dd> <dt>

*vorder* 
</dt> <dd>

Dimensión de la matriz de puntos de control en *el eje v.* Debe ser positivo.

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
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *target* no era un valor aceptado.<br/>                                                                                        |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *u1* era igual a *u2* o *v1* era igual a *v2.*<br/>                                                                         |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *Ustride* o *vstride* era menor que el número de valores de un punto de control.<br/>                                       |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | Uorder *o* *vorder* era menor que uno o GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                     |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Los evaluadores proporcionan una manera de usar la asignación polinómica o polinómica racionalizada para generar vértices, normales, coordenadas de textura y colores. Los valores generados por un evaluador se envían a otras fases del procesamiento de OpenGL como si se hubieran presentado mediante los comandos [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)y [**glColor,**](glcolor-functions.md) salvo que los valores generados no actualizan las coordenadas normales, de textura o de color actuales.

Todas las spline polinómicas o polinómicas racionalizadas de cualquier grado (hasta el grado máximo admitido por la implementación de OpenGL) se pueden describir mediante evaluadores. Entre ellas se incluyen casi todas las superficies que se usan en los gráficos del equipo, incluidas las superficies B-spline, las superficies DE SPLINE, las superficies Bézier, entre otras.

Los evaluadores definen superficies basadas en polinomios bivariados de Bernstein. Defina **p** (*u*^,*v*^) como

![Ecuación que muestra la definición de p ().](images/map05.png)

donde **R** *ij* es un punto de control, () es *el polinómico de* grado i th De Bernstein

*n* (*uorder*  =  *n* + 1)

![Ecuación en la que se muestra el polinomial De grado n.](images/map06.png)

y () es el polinómico *j* th Bernstein de degree *m* (*vorder*  =  *m* + 1)

![Ecuación en la que se muestra el polinomial De grado m.](images/map07.png)

Recuerde que

![Ecuaciones que muestran equivalencia a 1.](images/map08.png)

La **función glMap2** se usa para definir la base y especificar qué tipo de valores se generan. Una vez definido, se puede habilitar y deshabilitar un mapa llamando a [**glEnable**](glenable.md) y **glDisable** con el nombre del mapa, uno de los nueve valores predefinidos para el destino *,* descrito anteriormente. Cuando [**glEvalCoord2**](glevalcoord-functions.md) presenta los valores *u* y *v*, los polinómicos bivariados de Bernstein se evalúan mediante *u*^ y *v*^, donde

![Ecuación que muestra la definición de you^.](images/map09.png)

y

![Ecuación que muestra la definición de v^.](images/map10.png)

El *parámetro* de destino es una constante simbólica que indica qué tipo de puntos de control se proporcionan en los puntos y qué salida se genera cuando se evalúa el mapa.

Los *parámetros ustride*, *uorder,* *vstride,* *vorder* y *points* definen el direccionamiento de matriz para acceder a los puntos de control. El *parámetro points* es la ubicación del primer punto de control, que ocupa una, dos, tres o cuatro ubicaciones de memoria contiguas, en función del mapa que se esté definindo. Hay puntos *de control uorder* x *vorder* en la matriz. El *parámetro ustride* indica cuántas ubicaciones float o double se omiten para avanzar el puntero de memoria interno del punto de control **R** *ij* al punto de control **R** <sub>(\ i+1\ )j</sub>. El *parámetro vstride* indica cuántas ubicaciones float o double se omiten para avanzar el puntero de memoria interno del punto de control **R** *ij* al punto de control **R**<sub>i(j\ +1\).</sub>

Como sucede con todos los comandos de OpenGL que aceptan punteros  a datos, es como si **glMap2** copiara el contenido de los puntos antes de devolverlo. Los cambios en el contenido de *los puntos* no tienen ningún efecto después de llamar **a glMap2.**

Las funciones siguientes recuperan información relacionada **con glMap2**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ VERTEX \_ 3

**glIsEnabled con** el argumento GL \_ MAP2 \_ VERTEX \_ 4

**glIsEnabled con** el argumento GL \_ MAP2 \_ INDEX

**glIsEnabled con** el argumento GL \_ MAP2 \_ COLOR \_ 4

**glIsEnabled con** el argumento GL \_ MAP2 \_ NORMAL

**glIsEnabled con** el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1

**glIsEnabled con** el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2

**glIsEnabled con** el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3

**glIsEnabled con** el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





