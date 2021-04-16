---
title: función glEnable (GL. h)
description: Las funciones glEnable y glDisable habilitan o deshabilitan las capacidades de OpenGL. | función glEnable (GL. h)
ms.assetid: cd4590dd-ae41-47c9-9861-10d72318840f
keywords:
- glEnable (función) OpenGL
topic_type:
- apiref
api_name:
- glEnable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bc2d13233afec956c798805295c44c96df45d04
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670183"
---
# <a name="glenable-function"></a>glEnable función)

Las funciones **glEnable** y [**glDisable**](gldisable.md) habilitan o deshabilitan las capacidades de OpenGL.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEnable(
   GLenum cap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*punto* 
</dt> <dd>

Una constante simbólica que indica una capacidad de OpenGL.

Para obtener información sobre los valores que puede tomar el *Cap* , consulte la sección Comentarios siguiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *Cap* no era uno de los valores enumerados en la sección comentarios anteriores.<br/>                                                   |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Las funciones **glEnable** y **glDisable** habilitan y deshabilitan diversas funciones de gráficos de OpenGL. Use [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar el valor actual de cualquier funcionalidad.

Tanto **glEnable** como **glDisable** toman un único argumento, *Cap*, que puede suponer uno de los siguientes valores:



| Value                       | Significado                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| prueba de GL \_ alpha \_             | Si está habilitada, realice pruebas alfa. Vea [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| libro de contabilidad \_ automática \_ normal            | Si está habilitada, los vectores normales de superficie de proceso se componen de forma analítica cuando el vértice \_ \_ 3 de GL MAP2 (o el \_ \_ vértice 4 de GL MAP2 ( \_ \_ ha generado vértices. Vea [**glMap2**](glmap2.md).                                                                                        |
| fusión de contabilidad \_                   | Si está habilitada, mezcle los valores de color RGBA entrantes con los valores de los búferes de color. Vea [**glBlendFunc**](glblendfunc.md).                                                                                                                              |
| \_Plano de clip de contabilidad \_           | Si está habilitado, recorte la geometría en el plano de recorte definido por el usuario *i*. Vea [**glClipPlane**](glclipplane.md).                                                                                                                                                  |
| \_OP de \_ lógica de color de GL \_        | Si está habilitada, aplique la operación lógica actual a los valores de búfer de color y color RGBA entrantes. Vea [**glLogicOp**](gllogicop.md).                                                                                                                     |
| \_material de color GL \_         | Si está habilitada, tiene uno o más parámetros de material que realizan el seguimiento del color actual. Vea [**glColorMaterial**](glcolormaterial.md).                                                                                                                                   |
| \_cara de selección de contabilidad \_              | Si está habilitado, los polígonos de selección se basan en el bobinado en las coordenadas de la ventana. Vea [**glCullFace**](glcullface.md).                                                                                                                                               |
| \_prueba de profundidad de GL \_             | Si está habilitada, realice comparaciones de profundidad y actualice el búfer de profundidad. Vea [**glDepthFunc**](gldepthfunc.md) y [**glDepthRange**](gldepthrange.md).                                                                                                              |
| interpolación en contab. \_                  | Si está habilitado, la interpolación de componentes de color o índices antes de que se escriban en el búfer de color.                                                                                                                                                                 |
| niebla de contabilidad \_                     | Si está habilitada, mezcle un color de niebla en el color posterior a la texturización. Vea [**glFog**](glfog.md).                                                                                                                                                                    |
| \_OP de \_ lógica de índice de GL \_        | Si está habilitada, aplique la operación lógica actual a los índices de índice de entrada y de búfer de color. Vea [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ claro *i*                | Si está habilitada, incluya la opción Light *i* en la evaluación de la ecuación de iluminación. Vea [**glLightModel**](gllightmodel-functions.md) y [**glLight**](gllight-functions.md).                                                                                      |
| iluminación de GL \_                | Si está habilitada, use los parámetros de iluminación actuales para calcular el color o el índice del vértice. Si está deshabilitado, asocie el color o índice actual con cada vértice. Vea [**glMaterial**](glmaterial-functions.md), **glLightModel** y **glLight**.                |
| \_suavizado de línea de contabilidad \_            | Si está habilitada, dibuje líneas con el filtrado correcto. Si está deshabilitada, dibuje líneas con alias. Vea [**glLineWidth**](gllinewidth.md).                                                                                                                                     |
| línea de contabilidad \_ \_ punteada           | Si está habilitada, use el patrón punteado de línea actual al dibujar líneas. Vea [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| \_OP lógica de contabilidad \_               | Si está habilitada, aplique la operación lógica seleccionada actualmente a los índices de búfer de color y entrantes. Vea [**glLogicOp**](gllogicop.md).                                                                                                                    |
| GL \_ MAP1, \_ color \_ 4          | Si está habilitada, las llamadas a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan valores RGBA. Vea también [**glMap1**](glmap1.md).                                           |
| Índice de GL \_ MAP1 \_             | Si está habilitada, las llamadas a **glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** generan índices de color. Vea también **glMap1**.                                                                                                                                   |
| GL \_ MAP1 \_ normal            | Si está habilitada, las llamadas a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan normales. Vea también [**glMap1**](glmap1.md).                                               |
| GL \_ MAP1 \_ Texture \_ coordenadas \_ 1 | Si está habilitada, las llamadas a **glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** *generan coordenadas* de textura. Vea también **glMap1**.                                                                                                                         |
| MAP1 de la textura de GL \_ \_ \_ \_ 2 | Si está habilitada, las llamadas a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan coordenadas de textura *s* y *t* . Vea también [**glMap1**](glmap1.md).                       |
| MAP1 de textura de GL \_ \_ \_ \_ 3 | Si está habilitada, las llamadas a **glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** generan coordenadas de textura *s*, *t* y *r* . Vea también **glMap1**.                                                                                                           |
| GL \_ MAP1 \_ Texture \_ \_ 4 | Si está habilitada, las llamadas a [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan coordenadas de textura *s*, *t*, *r* y *q* . Vea también [**glMap1**](glmap1.md).                    |
| \_ \_ Vértice \_ 3 de GL MAP1         | Si está habilitada, las llamadas a **glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** generan coordenadas de vértice *x*, *y* y *z* . Vea también **glMap1**.                                                                                                            |
| \_ \_ Vértice \_ 4 de GL MAP1         | Si está habilitada, las llamadas a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan coordenadas de vértices *x*, *y*, *z* y *w* homogéneas. Vea también [**glMap1**](glmap1.md). |
| GL \_ MAP2 (, \_ color \_ 4          | Si está habilitada, las llamadas a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan valores RGBA. Vea también [**glMap2**](glmap2.md).                                           |
| Índice de GL \_ MAP2 ( \_             | Si está habilitada, las llamadas a **glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** generan índices de color. Vea también **glMap2**.                                                                                                                                   |
| GL \_ MAP2 ( \_ normal            | Si está habilitada, las llamadas a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan normales. Vea también [**glMap2**](glmap2.md).                                               |
| GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1 | Si está habilitada, las llamadas a **glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** *generan coordenadas* de textura. Vea también **glMap2**.                                                                                                                         |
| MAP2 (de la textura de GL \_ \_ \_ \_ 2 | Si está habilitada, las llamadas a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan coordenadas de textura *s* y *t* . Vea también [**glMap2**](glmap2.md).                       |
| MAP2 (de textura de GL \_ \_ \_ \_ 3 | Si está habilitada, las llamadas a **glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** generan coordenadas de textura *s*, *t* y *r* . Vea también **glMap2**.                                                                                                           |
| GL \_ MAP2 ( \_ Texture \_ \_ 4 | Si está habilitada, las llamadas a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan coordenadas de textura *s*, *t*, *r* y *q* . Vea también [**glMap2**](glmap2.md).            |
| \_ \_ Vértice \_ 3 de GL MAP2 (         | Si está habilitada, las llamadas a **glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** generan coordenadas de vértice *x*, *y* y *z* . Vea también **glMap2**.                                                                                                            |
| \_ \_ Vértice \_ 4 de GL MAP2 (         | Si está habilitada, las llamadas a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan coordenadas de vértices *x*, *y*, *z* y *w* homogéneas. Vea también [**glMap2**](glmap2.md). |
| normalizar libro de contabilidad \_               | Si está habilitado, los vectores normales especificados con **glNormal** se escalan a la longitud de la unidad después de la transformación. Vea [**glNormal**](glnormal-functions.md).                                                                                                          |
| \_suavidad de punto de contabilidad \_           | Si está habilitado, dibuje puntos con un filtrado adecuado. Si está deshabilitado, dibuje puntos con alias. Vea [**glPointSize**](glpointsize.md).                                                                                                                                    |
| \_relleno de \_ desplazamiento de polígono de GL \_   | Si está habilitado, y si el polígono se representa en el modo de relleno de contabilidad \_ , se agrega un desplazamiento a los valores de profundidad de los fragmentos de un polígono antes de que se realice la comparación de profundidad. Vea [**glPolygonOffset**](glpolygonoffset.md)**.**                                      |
| \_línea de \_ desplazamiento de polígono de GL \_   | Si está habilitado y el polígono se representa en modo de \_ línea de contabilidad, se agrega un desplazamiento a los valores de profundidad de los fragmentos de un polígono antes de que se realice la comparación de profundidad. Vea **glPolygonOffset**.                                                                 |
| \_punto de \_ desplazamiento de polígono de GL \_  | Si está habilitado, se agrega un desplazamiento a los valores de profundidad de los fragmentos de un polígono antes de que se realice la comparación de profundidad, si el polígono se representa en el modo de punto de contabilidad \_ . Vea [**glPolygonOffset**](glpolygonoffset.md).                                             |
| retorno de polígono de GL \_ \_         | Si está habilitada, dibuje polígonos con el filtrado adecuado. Si está deshabilitado, dibuje polígonos con alias. Vea [**glPolygonMode**](glpolygonmode.md).                                                                                                                            |
| punteado de cont. \_ \_        | Si está habilitada, use el patrón punteado de polígono actual al representar polígonos. Vea [**glPolygonStipple**](glpolygonstipple.md).                                                                                                                              |
| \_prueba de tijeras GL \_           | Si está habilitada, descartar fragmentos que están fuera del rectángulo de tijeras. Vea [**glScissor**](glscissor.md).                                                                                                                                                   |
| \_prueba de galería de símbolos GL \_           | Si está habilitada, realice una prueba de estarcido y actualice el búfer de estarcido. Vea [**glStencilFunc**](glstencilfunc.md) y [**glStencilOp**](glstencilop.md).                                                                                                            |
| Textura de GL \_ \_ 1D             | Si está habilitada, se realiza una textura de una dimensión (a menos que también esté habilitada la texturización bidimensional). Vea [**glTexImage1D**](glteximage1d.md).                                                                                                            |
| Textura de GL \_ \_ 2D             | Si está habilitada, se realiza la texturización bidimensional. Vea [**glTexImage2D**](glteximage2d.md).                                                                                                                                                               |
| GL \_ Texture \_ gen \_ p         | Si está habilitada, la coordenada de textura *q* se calcula con la función de generación de texturas definida con [**glTexGen**](gltexgen-functions.md). De lo contrario, se utiliza la coordenada de textura *q* actual.                                                        |
| GL \_ Texture \_ gen \_ R         | Si está habilitada, la coordenada de textura de *r* se calcula con la función de generación de textura definida con [**glTexGen**](gltexgen-functions.md). Si está deshabilitada, se usa la coordenada de textura actual de *r* .                                                      |
| GL \_ Texture \_ gen \_ S         | Si está habilitada, la coordenada de textura *s* se calcula utilizando la función de generación de textura definida con **glTexGen**. Si se deshabilita, se usa la coordenada de textura *s* actual.                                                                                |
| GL \_ Texture \_ gen \_ T         | Si está habilitada, la coordenada de textura *t* se calcula utilizando la función de generación de textura definida con [**glTexGen**](gltexgen-functions.md). Si está deshabilitada, se usa la coordenada de textura *t* actual.                                                      |



 

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord1**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh1**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint1**](glevalpoint.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





