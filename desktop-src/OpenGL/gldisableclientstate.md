---
title: función glDisableClientState (GL. h)
description: Las funciones glEnableClientState y glDisableClientState habilitan y deshabilitan las matrices, respectivamente. | función glDisableClientState (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- glDisableClientState (función) OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 163a7c3b679c979e5c800d2aa41ba2abb00e11f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670199"
---
# <a name="gldisableclientstate-function"></a>glDisableClientState función)

Las funciones [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** habilitan y deshabilitan las matrices, respectivamente.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDisableClientState(
   GLenum array
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*array* 
</dt> <dd>

Constante simbólica de la matriz que desea habilitar o deshabilitar. Este parámetro puede suponer uno de los valores siguientes.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_matriz de colores de GL \_**</dt> </dl>                          | Si está habilitada, use matrices de color con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vea también [**glColorPointer**](glcolorpointer.md).<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**\_matriz de \_ marcas de borde de GL \_**</dt> </dl>             | Si está habilitada, use matrices de marca perimetral con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vea también [**glEdgeFlagPointer**](gledgeflagpointer.md).<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_matriz de índice de GL \_**</dt> </dl>                          | Si está habilitada, use matrices de índice con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vea también [**glIndexPointer**](glindexpointer.md).<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**\_matriz normal de contabilidad general \_**</dt> </dl>                       | Si está habilitada, use matrices normales con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vea también [**glNormalPointer**](glnormalpointer.md).<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**\_matriz de \_ coordenadas de textura de GL \_**</dt> </dl> | Si está habilitada, use matrices de coordenadas de textura con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vea también [**glTexCoordPointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_matriz de vértices de GL \_**</dt> </dl>                       | Si está habilitada, use matrices de vértices con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vea también [**glVertexPointer**](glvertexpointer.md).<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl> | la *matriz* no era un valor aceptado.<br/> |



## <a name="remarks"></a>Observaciones

Las funciones [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** habilitan y deshabilitan varias matrices individuales. Use [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar el valor actual de cualquier funcionalidad.

La llamada a [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** entre llamadas a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md) puede producir un error. Si no se genera ningún error, el comportamiento es indefinido.

> [!Note]  
> Las funciones [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** solo están disponibles en la versión 1,1 o posterior de OpenGL.

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
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

 

 





