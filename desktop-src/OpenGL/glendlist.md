---
title: Función glEndList (Gl.h)
description: Las funciones glNewList y glEndList crean o reemplazan una lista de visualización. | Función glEndList (Gl.h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- Función glEndList OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad75f62b3b049f2244b6e701f69654d110c559b337c0d4bb72da75af93f954f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081525"
---
# <a name="glendlist-function"></a>función glEndList

Las [**funciones glNewList**](glnewlist.md) **y glEndList** crean o reemplazan una lista de visualización.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | **Se llamó a glEndList** sin un **glNewList** anterior, o si se llamó a **glnewlist** mientras se definió una lista para mostrar.<br/> |



## <a name="remarks"></a>Comentarios

Las listas para mostrar son grupos de comandos OpenGL que se han almacenado para su posterior ejecución. Las listas para mostrar se crean [**con glNewList**](glnewlist.md). Todos los comandos posteriores se colocan en la lista de visualización, en el orden emitido, hasta que **se llama a glEndList.**

La [**función glNewList**](glnewlist.md) tiene dos parámetros. El primer parámetro, *list*, es un entero positivo que se convierte en el nombre único de la lista para mostrar. Los nombres se pueden crear y reservar [**con glGenLists**](glgenlists.md) y probar la unidad [**con glIsList.**](glislist.md) El segundo parámetro, *mode*, es una constante simbólica que puede asumir uno de los dos valores anteriores.

Algunos comandos no se compilan en la lista de visualización, pero se ejecutan inmediatamente, independientemente del modo de lista de presentación. Estos comandos son [**glColorPointer,**](glcolorpointer.md) [**glDeleteLists,**](gldeletelists.md) [**glDisableClientState,**](gldisableclientstate.md) [**glEdgeFlagPointer,**](gledgeflagpointer.md) [**glEnableClientState,**](glenableclientstate.md) [**glFeedbackBuffer,**](glfeedbackbuffer.md) [**glFinish,**](glfinish.md) [**glFlush,**](glflush.md) [**glGenLists,**](glgenlists.md) [**glIndexPointer,**](glindexpointer.md) [**glInterleavedArrays,**](glinterleavedarrays.md) [**glIsEnabled**](glisenabled.md), [**glIsList,**](glislist.md) [**glNormalPointer,**](glnormalpointer.md) [**glPopClientAttrib,**](glpopclientattrib.md) [**glPixelStore,**](glpixelstore-functions.md) [**glPushClientAttrib,**](glpushclientattrib.md) [**glReadPixels,**](glreadpixels.md) [**glRenderMode,**](glrendermode.md) [**glSelectBuffer,**](glselectbuffer.md) [**glTexCoordPointer,**](gltexcoordpointer.md) [**glVertexPointer y**](glvertexpointer.md)todas las [**rutinas glGet.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

De forma similar, [**glTexImage2D**](glteximage2d.md) y [**glTexImage1D**](glteximage1d.md) se ejecutan inmediatamente y no se compilan en la lista de presentación cuando su primer argumento es GL \_ PROXY TEXTURE 2D o GL PROXY TEXTURE \_ \_ \_ \_ \_ 1D, respectivamente.

Cuando se encuentra la función **glEndList,** la definición de la lista para mostrar se completa asociando la lista a la lista de nombres *únicos* (especificada en el [**comando glNewList).**](glnewlist.md) Si ya existe una lista para mostrar *con* una lista de nombres, solo se reemplaza cuando se llama **a glEndList.**

Las [**funciones glCallList**](glcalllist.md) y [**glCallLists**](glcalllists.md) se pueden especificar en listas para mostrar. Los comandos de la lista de visualización o listas ejecutadas por **glCallList** o **glCallLists** no se incluyen en la lista de visualización que se va a crear, incluso si el modo de creación de la lista es GL \_ COMPILE AND \_ \_ EXECUTE.

La función siguiente recupera información relacionada con [**glNewList**](glnewlist.md):

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





