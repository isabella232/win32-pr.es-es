---
title: Función glEnableClientState (Gl.h)
description: Las funciones glEnableClientState y glDisableClientState habilitan y deshabilitan matrices, respectivamente. | Función glEnableClientState (Gl.h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- Función glEnableClientState OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1ebb9b0278ca6a696183da54c40a6463880a24f6a29a7cca3c2fdd9dd1213a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360422"
---
# <a name="glenableclientstate-function"></a>función glEnableClientState

Las **funciones glEnableClientState** y [**glDisableClientState**](gldisableclientstate.md) habilitan y deshabilitan matrices, respectivamente.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*array* 
</dt> <dd>

Constante simbólica para la matriz que desea habilitar o deshabilitar. Este parámetro puede suponer uno de los siguientes valores.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ COLOR \_ ARRAY**</dt> </dl>                          | Si está habilitada, use matrices de colores con llamadas [**a glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)o [**glDrawArrays.**](gldrawarrays.md)<br/> Vea también [**glColorPointer**](glcolorpointer.md).<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**GL \_ EDGE \_ FLAG \_ ARRAY**</dt> </dl>             | Si está habilitada, use matrices de marcas perimetrales con llamadas [**a glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)o [**glDrawArrays.**](gldrawarrays.md)<br/> Vea también [**glEdgeFlagPointer**](gledgeflagpointer.md).<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL \_ INDEX \_ ARRAY**</dt> </dl>                          | Si está habilitada, use matrices de índices con llamadas [**a glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)o [**glDrawArrays.**](gldrawarrays.md)<br/> Vea también [**glIndexPointer**](glindexpointer.md).<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL \_ NORMAL \_ ARRAY**</dt> </dl>                       | Si está habilitada, use matrices normales con llamadas [**a glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)o [**glDrawArrays.**](gldrawarrays.md)<br/> Vea también [**glNormalPointer**](glnormalpointer.md).<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL \_ TEXTURE \_ COORD \_ ARRAY**</dt> </dl> | Si está habilitada, use matrices de coordenadas de textura con llamadas [**a glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)o [**glDrawArrays.**](gldrawarrays.md)<br/> Vea también [**glTexCoordPointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL \_ VERTEX \_ ARRAY**</dt> </dl>                       | Si está habilitada, use matrices de vértices con llamadas [**a glArrayElement,**](glarrayelement.md) [**glDrawElements**](gldrawelements.md)o [**glDrawArrays.**](gldrawarrays.md)<br/> Vea también [**glVertexPointer**](glvertexpointer.md).<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl> | *Array* no era un valor aceptado.<br/> |



## <a name="remarks"></a>Comentarios

Las **funciones glEnableClientState** y **glDisableClientState** habilitan y deshabilitan varias matrices individuales. Use [**glIsEnabled**](glisenabled.md) o [**glGet para**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) determinar la configuración actual de cualquier funcionalidad.

Llamar **a glEnableClientState** y **glDisableClientState** entre llamadas a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md) puede producir un error. Si no se genera ningún error, el comportamiento es indefinido.

> [!Note]  
> Las **funciones glEnableClientState** y **glDisableClientState** solo están disponibles en OpenGL versión 1.1 o posterior.

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





