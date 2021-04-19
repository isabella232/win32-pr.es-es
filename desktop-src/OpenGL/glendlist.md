---
title: función glEndList (GL. h)
description: Las funciones glNewList y glEndList crean o reemplazan una lista de visualización. | función glEndList (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- glEndList (función) OpenGL
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
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689804"
---
# <a name="glendlist-function"></a>glEndList función)

Las funciones [**glNewList**](glnewlist.md) y **glEndList** crean o reemplazan una lista de visualización.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | se llamó a **glEndList** sin un **glNewList** anterior, o si se llamó a **glNewList** mientras se estaba definiendo una lista de visualización.<br/> |



## <a name="remarks"></a>Observaciones

Las listas de visualización son grupos de comandos OpenGL que se han almacenado para su posterior ejecución. Las listas de visualización se crean con [**glNewList**](glnewlist.md). Todos los comandos subsiguientes se colocan en la lista de visualización, en el orden emitido, hasta que se llame a **glEndList** .

La función [**glNewList**](glnewlist.md) tiene dos parámetros. El primer parámetro, *List*, es un entero positivo que se convierte en el nombre único de la lista de visualización. Los nombres se pueden crear y reservar con [**glGenLists**](glgenlists.md) y probar la unicidad con [**glIsList**](glislist.md). El segundo parámetro, *mode*, es una constante simbólica que puede suponer uno de los dos valores anteriores.

Algunos comandos no se compilan en la lista de visualización, pero se ejecutan inmediatamente, independientemente del modo de la lista de visualización. Estos comandos son [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**GlIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)y todas las rutinas de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .

De forma similar, [**glTexImage2D**](glteximage2d.md) y [**glTexImage1D**](glteximage1d.md) se ejecutan inmediatamente y no se compilan en la lista de visualización cuando su primer argumento es la textura de proxy \_ de contabilidad \_ \_ 2D o la \_ \_ textura de proxy de GL \_ 1D, respectivamente.

Cuando se encuentra la función **glEndList** , la definición de la lista de visualización se completa mediante la Asociación de la lista con la *lista* de nombres únicos (especificada en el comando [**glNewList**](glnewlist.md) ). Si ya existe una lista de visualización con la *lista* de nombres, solo se reemplaza cuando se llama a **glEndList** .

Las funciones [**glCallList**](glcalllist.md) y [**glCallLists**](glcalllists.md) se pueden especificar en las listas de visualización. Los comandos de la lista de visualización o las listas ejecutadas por **glCallList** o **glCallLists** no se incluyen en la lista de visualización que se está creando, incluso si el modo de creación de lista es GL \_ compile \_ y \_ Execute.

La siguiente función recupera información relacionada con [**glNewList**](glnewlist.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_

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

 

 





