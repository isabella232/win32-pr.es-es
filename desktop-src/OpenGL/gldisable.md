---
title: Función glDisable (Gl.h)
description: Las funciones glEnable y glDisable habilitan o deshabilitan las funcionalidades OpenGL. | Función glDisable (Gl.h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- Función glDisable OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362072"
---
# <a name="gldisable-function"></a>Función glDisable

Las [**funciones glEnable**](glenable.md) **y glDisable** habilitan o deshabilitan las funcionalidades OpenGL.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tapa* 
</dt> <dd>

Constante simbólica que indica una funcionalidad OpenGL.

Para obtener información sobre el límite *de* valores, consulte la sección Comentarios siguiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *cap* no era uno de los valores enumerados en la sección Comentarios anterior.<br/>                                                   |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Las [**funciones glEnable**](glenable.md) y **glDisable** habilitan y deshabilitan varias funcionalidades de gráficos OpenGL. Use [**glIsEnabled**](glisenabled.md) o [**glGet para**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) determinar la configuración actual de cualquier funcionalidad.

Tanto [**glEnable**](glenable.md) como **glDisable** toman un solo argumento, *cap*, que puede suponer uno de los valores siguientes:



| Value                       | Significado                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ ALPHA \_ TEST             | Si está habilitada, realice pruebas alfa. Vea [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| GL \_ AUTO \_ NORMAL            | Si está habilitada, los vectores normales de la superficie de proceso se calculan analíticamente cuando GL MAP2 VERTEX 3 o GL MAP2 VERTEX 4 han generado \_ \_ \_ \_ \_ \_ vértices. Vea [**glMap2.**](glmap2.md)                                                                                        |
| GL \_ BLEND                   | Si está habilitada, combine los valores de color RGBA entrantes con los valores de los búferes de color. Vea [**glBlendFunc.**](glblendfunc.md)                                                                                                                              |
| GL \_ CLIP \_ PLANE *i*          | Si está habilitada, recorte la geometría en el plano de recorte definido por el *usuario i*. Vea [**glClipPlane**](glclipplane.md).                                                                                                                                                  |
| GL \_ COLOR \_ LOGIC \_ OP        | Si está habilitada, aplique la operación lógica actual a los valores entrantes de color RGBA y búfer de color. Vea [**glLogicOp**](gllogicop.md).                                                                                                                     |
| \_MATERIAL DE COLOR \_ GL         | Si está habilitada, haga que uno o varios parámetros de material realicen un seguimiento del color actual. Vea [**glColorMaterial.**](glcolormaterial.md)                                                                                                                                   |
| GL \_ CULL \_ FACE              | Si está habilitada, los polígonos cull se basan en su sinuoso en coordenadas de ventana. Vea [**glCullFace**](glcullface.md).                                                                                                                                               |
| PRUEBA \_ DE PROFUNDIDAD DE \_ GL             | Si está habilitada, realice comparaciones de profundidad y actualice el búfer de profundidad. Vea [**glDepthFunc**](gldepthfunc.md) y [**glDepthRange**](gldepthrange.md).                                                                                                              |
| GL \_ DITHER                  | Si está habilitada, dither color components or indexes before they are written to the color buffer.                                                                                                                                                                 |
| GL \_ FOG                     | Si está habilitada, combine un color de color rojo en el color posterior a la texturización. Vea [**glFog**](glfog.md).                                                                                                                                                                    |
| GL \_ INDEX \_ LOGIC \_ OP        | Si está habilitada, aplique la operación lógica actual a los índices de índice y búfer de color entrantes. Vea [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ LIGHT *i*                | Si está habilitada, incluya la *luz i en* la evaluación de la ecuación de iluminación. Vea [**glLightModel**](gllightmodel-functions.md) y [**glLight**](gllight-functions.md).                                                                                      |
| ILUMINACIÓN \_ DE GL                | Si está habilitada, use los parámetros de iluminación actuales para calcular el color o índice del vértice. Si está deshabilitado, asocie el color o índice actual a cada vértice. Vea [**glMaterial,**](glmaterial-functions.md) **glLightModel** y **glLight.**                |
| GL \_ LINE \_ SMOOTH            | Si está habilitada, dibuje líneas con el filtrado correcto. Si está deshabilitado, dibuje líneas con alias. Vea [**glLineWidth.**](gllinewidth.md)                                                                                                                                     |
| GL \_ LINE \_ STIPPLE           | Si está habilitada, use el patrón detippla de línea actual al dibujar líneas. Consulte [**glLineStipple.**](gllinestipple.md)                                                                                                                                            |
| GL \_ LOGIC \_ OP               | Si está habilitada, aplique la operación lógica seleccionada actualmente a los índices entrantes y de búfer de color. Vea [**glLogicOp**](gllogicop.md).                                                                                                                    |
| GL \_ MAP1 \_ COLOR \_ 4          | Si está habilitada, las llamadas [**a glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan valores RGBA. Consulte también [**glMap1.**](glmap1.md)                                           |
| GL \_ MAP1 \_ INDEX             | Si está habilitada, las llamadas **a glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** generan índices de color. Consulte también **glMap1.**                                                                                                                                   |
| GL \_ MAP1 \_ NORMAL            | Si está habilitada, las llamadas [**a glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan normales. Consulte también [**glMap1.**](glmap1.md)                                               |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1 | Si está habilitada, las llamadas **a glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** *generan* coordenadas de textura de s. Consulte también **glMap1.**                                                                                                                         |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2 | Si está habilitada, las llamadas [**a glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan *coordenadas* de textura s y *t.* Consulte también [**glMap1.**](glmap1.md)                       |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3 | Si está habilitada, las llamadas **a glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** generan coordenadas de textura *s*, *t* y *r.* Consulte también **glMap1.**                                                                                                           |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4 | Si está habilitada, las llamadas [a glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan las coordenadas de textura *s*, *t*, *r* y *q.* Consulte también [**glMap1.**](glmap1.md)                    |
| GL \_ MAP1 \_ VERTEX \_ 3         | Si está habilitada, las llamadas **a glEvalCoord1**, **glEvalMesh1** y **glEvalPoint1** generan coordenadas de vértice *x,* *y* *y z.* Consulte también **glMap1.**                                                                                                            |
| GL \_ MAP1 \_ VERTEX \_ 4         | Si está habilitada, las llamadas [**a glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)y [**glEvalPoint1**](glevalpoint.md) generan coordenadas de vértice *x,* *y,* *z* y *w* homogéneos. Consulte también [**glMap1.**](glmap1.md) |
| GL \_ MAP2 \_ COLOR \_ 4          | Si está habilitada, las llamadas [**a glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan valores RGBA. Consulte también [**glMap2.**](glmap2.md)                                           |
| GL \_ MAP2 \_ INDEX             | Si está habilitada, las llamadas **a glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** generan índices de color. Consulte también **glMap2.**                                                                                                                                   |
| GL \_ MAP2 \_ NORMAL            | Si está habilitada, las llamadas [**a glEvalCoord2,**](glevalcoord-functions.md) [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan normales. Consulte también [**glMap2.**](glmap2.md)                                               |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1 | Si está habilitada, las llamadas **a glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** *generan* coordenadas de textura de s. Consulte también **glMap2.**                                                                                                                         |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2 | Si está habilitada, las llamadas [**a glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan coordenadas de textura *s* y *t.* Consulte también [**glMap2.**](glmap2.md)                       |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3 | Si está habilitada, las llamadas **a glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** generan coordenadas de textura *s*, *t* *y r.* Consulte también **glMap2.**                                                                                                           |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4 | Si está habilitada, las llamadas [**a glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan coordenadas de textura *s*, *t,* *r* y *q.* Consulte también [**glMap2.**](glmap2.md)            |
| GL \_ MAP2 \_ VERTEX \_ 3         | Si está habilitada, las llamadas **a glEvalCoord2**, **glEvalMesh2** y **glEvalPoint2** generan coordenadas de vértice *x,* *y* *y z.* Consulte también **glMap2.**                                                                                                            |
| GL \_ MAP2 \_ VERTEX \_ 4         | Si está habilitada, las llamadas [**a glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)y [**glEvalPoint2**](glevalpoint.md) generan coordenadas de vértice *x,* *y,* *z* y *w* homogéneos. Consulte también [**glMap2.**](glmap2.md) |
| \_NORMALIZACIÓN DE GL               | Si está habilitada, los vectores normales especificados **con glNormal** se escalan a la longitud de unidad después de la transformación. Vea [**glNormal**](glnormal-functions.md).                                                                                                          |
| GL \_ POINT \_ SMOOTH           | Si está habilitada, dibuje puntos con el filtrado adecuado. Si está deshabilitado, dibuje puntos con alias. Vea [**glPointSize.**](glpointsize.md)                                                                                                                                    |
| RELLENO DE \_ DESPLAZAMIENTO \_ DE POLÍGONO \_ GL   | Si está habilitado y el polígono se representa en el modo GL FILL, se agrega un desplazamiento a los valores de profundidad de los fragmentos de un polígono antes de realizar la comparación \_ de profundidad. Vea [**glPolygonOffset.**](glpolygonoffset.md)                                      |
| LÍNEA DE \_ DESPLAZAMIENTO \_ DEL POLÍGONO \_ GL   | Si está habilitado, y si el polígono se representa en modo GL LINE, se agrega un desplazamiento a los valores de profundidad de los fragmentos de un polígono antes de realizar la comparación \_ de profundidad. Vea **glPolygonOffset.**                                                                 |
| PUNTO DE \_ DESPLAZAMIENTO \_ DE POLÍGONO \_ GL  | Si está habilitada, se agrega un desplazamiento a los valores de profundidad de los fragmentos de un polígono antes de realizar la comparación de profundidad, si el polígono se representa en modo \_ GL POINT. Vea [**glPolygonOffset.**](glpolygonoffset.md)                                             |
| GL \_ POLYGON \_ SMOOTH         | Si está habilitada, dibuje polígonos con el filtrado adecuado. Si está deshabilitado, dibuje polígonos con alias. Vea [**glPolygonMode.**](glpolygonmode.md)                                                                                                                            |
| GL \_ POLYGON \_ STIPPLE        | Si está habilitada, use el patrón detippla de polígono actual al representar polígonos. Consulte [**glPolygonStipple.**](glpolygonstipple.md)                                                                                                                              |
| GL \_ LA PRUEBA DE LA \_ RESERCIÓN           | Si está habilitada, descarte los fragmentos que están fuera del rectángulo de rectángulos. Vea [**glScissor**](glscissor.md).                                                                                                                                                   |
| GL \_ STENCIL \_ TEST           | Si está habilitada, realice pruebas de galería de símbolos y actualice el búfer de galería de símbolos. Vea [**glStencilFunc**](glstencilfunc.md) y [**glStencilOp.**](glstencilop.md)                                                                                                            |
| TEXTURA \_ GL \_ 1D             | Si está habilitada, se realiza la texturización unidimensional (a menos que también esté habilitada la texturización bidimensional). Vea [**glTexImage1D.**](glteximage1d.md)                                                                                                            |
| GL \_ TEXTURE \_ 2D             | Si está habilitada, se realiza el texturizado bidimensional. Vea [**glTexImage2D.**](glteximage2d.md)                                                                                                                                                               |
| GL \_ TEXTURE \_ GEN \_ Q         | Si está habilitada, la *coordenada* de textura q se calcula mediante la función de generación de textura definida con [**glTexGen**](gltexgen-functions.md). De lo contrario, se *usa la coordenada* de textura q actual.                                                        |
| GL \_ TEXTURE \_ GEN \_ R         | Si está habilitada, la coordenada de textura *r* se calcula mediante la función de generación de textura definida con [**glTexGen**](gltexgen-functions.md). Si está deshabilitada, se usa la coordenada de textura *r* actual.                                                      |
| GL \_ TEXTURE \_ GEN \_ S         | Si está habilitada, la *coordenada* de textura se calcula mediante la función de generación de textura definida con **glTexGen**. Si está deshabilitada, se *usa la coordenada* de textura actual.                                                                                |
| GL \_ TEXTURE \_ GEN \_ T         | Si está habilitada, la *coordenada* de textura t se calcula mediante la función de generación de textura definida con [**glTexGen**](gltexgen-functions.md). Si está deshabilitada, se usa la coordenada de textura *t* actual.                                                      |



 

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
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

 

 





