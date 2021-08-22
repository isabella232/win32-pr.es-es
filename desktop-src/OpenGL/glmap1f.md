---
title: Función glMap1f (Gl.h)
description: La función glMap1f define un evaluador unidimensional. | Función glMap1f (Gl.h)
ms.assetid: c016ad80-b507-4e21-829f-f173d5c8dee6
keywords:
- Función glMap1f OpenGL
topic_type:
- apiref
api_name:
- glMap1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7547e465f940942333c3bcff3e543e77c404ced289471ccff08924da83bfc2af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359313"
---
# <a name="glmap1f-function"></a>Función glMap1f

Las [**funciones glMap1d**](glmap1d.md) **y glMap1f** definen un evaluador unidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMap1f(
         GLenum  target,
         GLfloat u1,
         GLfloat u2,
         GLint   stride,
         GLint   order,
   const GLfloat *points
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Tipo de valores generados por el evaluador. Constantes simbólicas. El *parámetro de* destino es una constante simbólica que indica qué tipo de puntos de control se proporcionan en los puntos y qué salida se genera cuando se evalúa el mapa. Puede suponer uno de los nueve valores predefinidos.



| Valor                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 3**</dt> </dl>                       | Cada punto de control es tres valores de punto flotante que *representan x, y y* *z.* Los [**comandos glVertex3**](glvertex-functions.md) internos se generan cuando se evalúa el mapa.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 4**</dt> </dl>                       | Cada punto de control es cuatro valores de punto flotante que *representan x, y, z* y *w*. Los [**comandos glVertex4**](glvertex-functions.md) internos se generan cuando se evalúa el mapa.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ MAP1 \_ INDEX**</dt> </dl>                                 | Cada punto de control es un valor de punto flotante único que representa un índice de color. Los [**comandos glIndex**](glindex-functions.md) internos se generan cuando se evalúa el mapa. Sin embargo, el índice actual no se actualiza con el valor de estos **comandos glIndex.**<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ COLOR \_ 4**</dt> </dl>                          | Cada punto de control es cuatro valores de punto flotante que representan rojo, verde, azul y alfa. Los [**comandos glColor4**](glcolor-functions.md) internos se generan cuando se evalúa el mapa. Sin embargo, el color actual no se actualiza con el valor de estos **comandos glColor4.**<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ NORMAL**</dt> </dl>                              | Cada punto de control es tres valores de punto flotante que representan los *componentes x, y* *y z* de un vector normal. Los [**comandos glNormal**](glnormal-functions.md) internos se generan cuando se evalúa el mapa. Sin embargo, la normal actual no se actualiza con el valor de estos **comandos glNormal.**<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1**</dt> </dl> | Cada punto de control es un valor de punto flotante único que representa la *coordenada de* textura de la . Los [**comandos internos glTexCoord1**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos **comandos glTexCoord.**<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2**</dt> </dl> | Cada punto de control es dos valores de punto flotante que representan las coordenadas de textura *s* y *t.* Los [**comandos internos glTexCoord2**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos **comandos glTexCoord.**<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3**</dt> </dl> | Cada punto de control es tres valores de punto flotante que representan las coordenadas *de textura s, t* y *r.* Los [**comandos internos glTexCoord3**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos **comandos glTexCoord.**<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4**</dt> </dl> | Cada punto de control es cuatro valores de punto flotante que representan las coordenadas de textura *s, t, r* y *q.* Los [**comandos internos glTexCoord4**](gltexcoord-functions.md) se generan cuando se evalúa el mapa. Sin embargo, las coordenadas de textura actuales no se actualizan con el valor de estos **comandos glTexCoord.**<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Asignación lineal de *u*, como se presenta a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, la variable que se evalúa mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*u2* 
</dt> <dd>

Asignación lineal de *u*, como se presenta a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, la variable que se evalúa mediante las ecuaciones especificadas por este comando.

</dd> <dt>

*Paso* 
</dt> <dd>

Número de flotantes o dobles entre el principio de un punto de control y el principio del siguiente en la estructura de datos a la que se hace referencia en *puntos*. Esto permite incrustar puntos de control en estructuras de datos arbitrarias. La única restricción es que los valores de un punto de control determinado deben ocupar ubicaciones de memoria contiguas.

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
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* no era un valor aceptado.<br/>                                                                                        |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *u1* era igual a *u2.*<br/>                                                                                                    |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *stride* era menor que el número de valores de un punto de control.<br/>                                                            |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *order* era menor que uno o GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Los evaluadores proporcionan una manera de usar la asignación polinómica o polinómica racionalizada para generar vértices, normales, coordenadas de textura y colores. Los valores generados por un evaluador se envían a otras fases del procesamiento openGL como si se hubieran presentado mediante los comandos [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)y [**glColor,**](glcolor-functions.md) salvo que los valores generados no actualizan la normal actual, las coordenadas de textura o el color.

Todas las spline polinómicas o polinómicas racionalizas de cualquier grado (hasta el grado máximo admitido por la implementación de OpenGL) se pueden describir mediante evaluadores. Estos incluyen casi todas las curvas spline usadas en gráficos de equipo, incluidas las curvas B, curvas Bézier, curvas spline de Hermite, entre otras.

Los evaluadores definen curvas basadas en polinómicos de Bernstein. Definir **p** () como

![Ecuación que muestra la definición de p ().](images/map01.png)

donde **R**_i_ es un punto de control y () es el polinómico *i* del grado *n* (*orden*  = *n* + 1):

![Ecuación que muestra el polinómico de Grado n.](images/map02.png)

Recuerde que

![Ecuaciones que muestran la equivalencia a 1.](images/map03.png)

La **función glMap1** se usa para definir la base y especificar qué tipo de valores se generan. Una vez definido, un mapa se puede habilitar y deshabilitar llamando a [**glEnable**](glenable.md) y  **glDisable** con el nombre del mapa, uno de los nueve valores predefinidos para el destino descrito anteriormente. La [función glEvalCoord1](glevalcoord-functions.md) evalúa los mapas unidimensionales que están habilitados. Cuando **glEvalCoord1** presenta un valor *u*, las funciones de Bern booleano se evalúan mediante *u*^, donde

![Ecuación que muestra la definición de you^.](images/map04.png)

Los *parámetros stride*, *order* y *points* definen el direccionamiento de la matriz para acceder a los puntos de control. El *parámetro points* es la ubicación del primer punto de control, que ocupa una, dos, tres o cuatro ubicaciones de memoria contiguas, en función de qué mapa se esté definindo. El *parámetro order* es el número de puntos de control de la matriz. El *parámetro stride* indica cuántas ubicaciones float o double tienen que avanzar el puntero de memoria interno para llegar al siguiente punto de control.

Como sucede con todos los comandos de OpenGL que aceptan punteros  a datos, es como si **glMap1** copiara el contenido de los puntos antes de devolverlo. Los cambios en el contenido de *los puntos* no tienen ningún efecto después de llamar **a glMap1.**

Las funciones siguientes recuperan información relacionada **con glMap1**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ VERTEX \_ 3

**glIsEnabled con** el argumento GL \_ MAP1 \_ VERTEX \_ 4

**glIsEnabled con** el argumento GL \_ MAP1 \_ INDEX

**glIsEnabled con** el argumento GL \_ MAP1 \_ COLOR \_ 4

**glIsEnabled con** el argumento GL \_ MAP1 \_ NORMAL

**glIsEnabled con** el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

**glIsEnabled con** el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

**glIsEnabled con** el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

**glIsEnabled con** el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





