---
title: función glIsEnabled (GL. h)
description: La función gllsEnabled comprueba si una funcionalidad está habilitada.
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- glIsEnabled (función) OpenGL
topic_type:
- apiref
api_name:
- glIsEnabled
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdb2ba206e0a026aef118b06d66097ade9ba9ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803494"
---
# <a name="glisenabled-function"></a>glIsEnabled función)

La función **gllsEnabled** comprueba si una funcionalidad está habilitada.

## <a name="syntax"></a>Sintaxis


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*punto* 
</dt> <dd>

Una constante simbólica que indica una capacidad de OpenGL. Se aceptan las siguientes capacidades.



| Value                                                                                                                                                                                                    | Significado                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**prueba de GL \_ alpha \_**</dt> </dl>                                           | Consulte [ **glAlphaFunc**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**libro de contabilidad \_ automática \_ normal**</dt> </dl>                                        | Consulte [ **glEvalCoord**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**fusión de contabilidad \_**</dt> </dl>                                                           | Consulte [ **glBlendFunc**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>* * Plano de clip de contabilidad \_ * i * * * \_</dt> </dl> | Consulte [ **glClipPlane**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_matriz de colores de GL \_**</dt> </dl>                                        | Consulte [ **glColorPointer**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**\_OP de \_ lógica de color de GL \_**</dt> </dl>                              | Consulte [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**\_material de color GL \_**</dt> </dl>                               | Consulte [ **glColorMaterial**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**\_cara de selección de contabilidad \_**</dt> </dl>                                              | Consulte [ **glCullFace**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**\_prueba de profundidad de GL \_**</dt> </dl>                                           | Vea [**glDepthFunc**](gldepthfunc.md) y [**glDepthRange**](gldepthrange.md)<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**interpolación en contab. \_**</dt> </dl>                                                        | Consulte [ **glEnable**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**niebla de contabilidad \_**</dt> </dl>                                                                 | Consulte [ **glFog**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_matriz de índice de GL \_**</dt> </dl>                                        | Consulte [ **glIndexPointer**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**\_OP de \_ lógica de índice de GL \_**</dt> </dl>                              | Consulte [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>* * Luz de contabilidad * * * * * \_</dt> </dl>                      | Vea [**glLightModel**](gllightmodel-functions.md) y [**glLight**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**iluminación de GL \_**</dt> </dl>                                                  | Vea [**glMaterial**](glmaterial-functions.md), [**glLightModel**](gllightmodel-functions.md)y [**glLight**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**\_suavizado de línea de contabilidad \_**</dt> </dl>                                        | Consulte [ **glLineWidth**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**línea de contabilidad \_ \_ punteada**</dt> </dl>                                     | Consulte [ **glLineStipple**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1, \_ color \_ 4**</dt> </dl>                                    | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**Índice de GL \_ MAP1 \_**</dt> </dl>                                           | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ normal**</dt> </dl>                                        | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ coordenadas \_ 1**</dt> </dl>           | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**MAP1 de la textura de GL \_ \_ \_ \_ 2**</dt> </dl>           | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**MAP1 de textura de GL \_ \_ \_ \_ 3**</dt> </dl>           | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ \_ 4**</dt> </dl>           | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**\_ \_ Vértice \_ 3 de GL MAP1**</dt> </dl>                                 | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**\_ \_ Vértice \_ 4 de GL MAP1**</dt> </dl>                                 | Consulte [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 (, \_ color \_ 4**</dt> </dl>                                    | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**Índice de GL \_ MAP2 ( \_**</dt> </dl>                                           | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 ( \_ normal**</dt> </dl>                                        | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1**</dt> </dl>           | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**MAP2 (de la textura de GL \_ \_ \_ \_ 2**</dt> </dl>           | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**MAP2 (de textura de GL \_ \_ \_ \_ 3**</dt> </dl>           | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 ( \_ Texture \_ \_ 4**</dt> </dl>           | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**\_ \_ Vértice \_ 3 de GL MAP2 (**</dt> </dl>                                 | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**\_ \_ Vértice \_ 4 de GL MAP2 (**</dt> </dl>                                 | Consulte [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**\_matriz normal de contabilidad general \_**</dt> </dl>                                     | Consulte [ **glNormalPointer**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**normalizar libro de contabilidad \_**</dt> </dl>                                               | Consulte [ **glNormal**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**\_suavidad de punto de contabilidad \_**</dt> </dl>                                     | Consulte [ **glPointSize**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**\_relleno de \_ desplazamiento de polígono de GL \_**</dt> </dl>               | Consulte [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**\_línea de \_ desplazamiento de polígono de GL \_**</dt> </dl>               | Consulte [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**\_punto de \_ desplazamiento de polígono de GL \_**</dt> </dl>            | Consulte [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**retorno de polígono de GL \_ \_**</dt> </dl>                               | Consulte [ **glPolygonMode**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**punteado de cont. \_ \_**</dt> </dl>                            | Consulte [ **glPolygonStipple**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**\_prueba de tijeras GL \_**</dt> </dl>                                     | Consulte [ **glScissor**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**\_prueba de galería de símbolos GL \_**</dt> </dl>                                     | Vea [**glStencilFunc**](glstencilfunc.md) y [**glStencilOp**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**Textura de GL \_ \_ 1D**</dt> </dl>                                           | Consulte [ **glTexImage1D**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**Textura de GL \_ \_ 2D**</dt> </dl>                                           | Consulte [ **glTexImage2D**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**\_matriz de \_ coordenadas de textura de GL \_**</dt> </dl>               | Consulte [ **glTexCoordPointer**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**GL \_ Texture \_ gen \_ p**</dt> </dl>                                 | Consulte [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**GL \_ Texture \_ gen \_ R**</dt> </dl>                                 | Consulte [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**GL \_ Texture \_ gen \_ S**</dt> </dl>                                 | Consulte [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**GL \_ Texture \_ gen \_ T**</dt> </dl>                                 | Consulte [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_matriz de vértices de GL \_**</dt> </dl>                                     | Consulte [ **glVertexPointer**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *Cap* no era un valor aceptado.<br/>                                                                                           |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **gllsEnabled** devuelve GL \_ true si *Cap* es una capacidad habilitada y devuelve GL \_ false en caso contrario.

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





