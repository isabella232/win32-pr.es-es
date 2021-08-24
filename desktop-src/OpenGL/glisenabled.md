---
title: Función glIsEnabled (Gl.h)
description: La función gllsEnabled comprueba si una funcionalidad está habilitada.
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- Función GlIsEnabled OpenGL
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
ms.openlocfilehash: 3237cedc1daeffa3fd47fd50b9b19d79ebad3acbf53bdd7929b70dad4093a7a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493405"
---
# <a name="glisenabled-function"></a>Función glIsEnabled

La **función gllsEnabled** comprueba si una funcionalidad está habilitada.

## <a name="syntax"></a>Sintaxis


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tapa* 
</dt> <dd>

Constante simbólica que indica una funcionalidad OpenGL. Se aceptan las siguientes funcionalidades.



| Valor                                                                                                                                                                                                    | Significado                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**GL \_ ALPHA \_ TEST**</dt> </dl>                                           | Consulte [ **glAlphaFunc**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**GL \_ AUTO \_ NORMAL**</dt> </dl>                                        | Consulte [ **glEvalCoord**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**GL \_ BLEND**</dt> </dl>                                                           | Consulte [ **glBlendFunc**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>**GL \_ CLIP \_ PLANE *i**</dt> </dl> | Consulte [ **glClipPlane.**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ COLOR \_ ARRAY**</dt> </dl>                                        | Vea [ **glColorPointer.**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**GL \_ COLOR \_ LOGIC \_ OP**</dt> </dl>                              | Consulte [ **glLogicOp.**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**\_MATERIAL DE COLOR \_ GL**</dt> </dl>                               | Consulte [ **glColorMaterial.**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**GL \_ CULL \_ FACE**</dt> </dl>                                              | Consulte [ **glCullFace.**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**PRUEBA \_ DE PROFUNDIDAD DE \_ GL**</dt> </dl>                                           | Consulte [**glDepthFunc**](gldepthfunc.md) y [**glDepthRange.**](gldepthrange.md)<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**GL \_ DITHER**</dt> </dl>                                                        | Consulte [ **glEnable**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**GL \_ FOG**</dt> </dl>                                                                 | Consulte [ **glFog.**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL \_ INDEX \_ ARRAY**</dt> </dl>                                        | Consulte [ **glIndexPointer.**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**GL \_ INDEX \_ LOGIC \_ OP**</dt> </dl>                              | Consulte [ **glLogicOp.**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>**GL \_ LIGHT *i**</dt> </dl>                      | Consulte [**glLightModel**](gllightmodel-functions.md) y [**glLight**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**ILUMINACIÓN \_ DE GL**</dt> </dl>                                                  | Consulte [**glMaterial,**](glmaterial-functions.md) [**glLightModel**](gllightmodel-functions.md)y [**glLight**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**GL \_ LINE \_ SMOOTH**</dt> </dl>                                        | Consulte [ **glLineWidth.**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**GL \_ LINE \_ STIPPLE**</dt> </dl>                                     | Consulte [ **glLineStipple.**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ COLOR \_ 4**</dt> </dl>                                    | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ MAP1 \_ INDEX**</dt> </dl>                                           | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ NORMAL**</dt> </dl>                                        | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1**</dt> </dl>           | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2**</dt> </dl>           | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3**</dt> </dl>           | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4**</dt> </dl>           | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 3**</dt> </dl>                                 | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 4**</dt> </dl>                                 | Consulte [ **glMap1.**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 \_ COLOR \_ 4**</dt> </dl>                                    | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ MAP2 \_ INDEX**</dt> </dl>                                           | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 \_ NORMAL**</dt> </dl>                                        | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1**</dt> </dl>           | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2**</dt> </dl>           | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3**</dt> </dl>           | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4**</dt> </dl>           | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 3**</dt> </dl>                                 | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 4**</dt> </dl>                                 | Consulte [ **glMap2.**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL \_ NORMAL \_ ARRAY**</dt> </dl>                                     | Consulte [ **glNormalPointer**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**\_NORMALIZACIÓN DE GL**</dt> </dl>                                               | Consulte [ **glNormal**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**GL \_ POINT \_ SMOOTH**</dt> </dl>                                     | Vea [ **glPointSize.**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**RELLENO DE \_ DESPLAZAMIENTO \_ DE POLÍGONO \_ GL**</dt> </dl>               | Consulte [ **glPolygonOffset.**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**LÍNEA DE \_ DESPLAZAMIENTO \_ DEL POLÍGONO \_ GL**</dt> </dl>               | Consulte [ **glPolygonOffset.**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**PUNTO DE \_ DESPLAZAMIENTO \_ DE POLÍGONO \_ GL**</dt> </dl>            | Consulte [ **glPolygonOffset.**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**GL \_ POLYGON \_ SMOOTH**</dt> </dl>                               | Consulte [ **glPolygonMode.**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**GL \_ POLYGON \_ STIPPLE**</dt> </dl>                            | Consulte [ **glPolygonStipple.**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**GL \_ LA PRUEBA DE LA \_ RESERCIÓN**</dt> </dl>                                     | Consulte [ **glScissor.**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**GL \_ STENCIL \_ TEST**</dt> </dl>                                     | Consulte [**glStencilFunc**](glstencilfunc.md) y [**glStencilOp.**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**TEXTURA \_ GL \_ 1D**</dt> </dl>                                           | Consulte [ **glTexImage1D.**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**GL \_ TEXTURE \_ 2D**</dt> </dl>                                           | Consulte [ **glTexImage2D.**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL \_ TEXTURE \_ COORD \_ ARRAY**</dt> </dl>               | Consulte [ **glTexCoordPointer**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ Q**</dt> </dl>                                 | Consulte [ **glTexGen.**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ R**</dt> </dl>                                 | Consulte [ **glTexGen.**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ S**</dt> </dl>                                 | Consulte [ **glTexGen.**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ T**</dt> </dl>                                 | Consulte [ **glTexGen.**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL \_ VERTEX \_ ARRAY**</dt> </dl>                                     | Vea [ **glVertexPointer**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *cap* no era un valor aceptado.<br/>                                                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función gllsEnabled** devuelve GL TRUE si cap es una funcionalidad habilitada y devuelve GL FALSE en caso \_  \_ contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





