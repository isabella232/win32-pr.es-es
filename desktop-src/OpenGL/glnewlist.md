---
title: Función glNewList (Gl.h)
description: Las funciones glNewList y glEndList crean o reemplazan una lista de visualización. | Función glNewList (Gl.h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- Función glNewList OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375162"
---
# <a name="glnewlist-function"></a>función glNewList

Las **funciones glNewList** [**y glEndList**](glendlist.md) crean o reemplazan una lista de visualización.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*list* 
</dt> <dd>

Nombre de la lista para mostrar.

</dd> <dt>

*mode* 
</dt> <dd>

Modo de compilación. Se aceptan los valores siguientes.



| Value                                                                                                                                                                                      | Significado                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <dt>**COMPILACIÓN \_ DE GL**</dt> </dl>                                       | Los comandos simplemente se compilan.<br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <dt>**COMPILACIÓN \_ \_ Y EJECUCIÓN DE \_ GL**</dt> </dl> | Los comandos se ejecutan a medida que se compilan en la lista de visualización.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *list* era cero.<br/>                                                                                                           |
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *mode* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Las listas para mostrar son grupos de comandos OpenGL que se han almacenado para su posterior ejecución. Las listas para mostrar se crean **con glNewList.** Todos los comandos posteriores se colocan en la lista de visualización, en el orden emitido, hasta que **se llama a glEndList.**

La **función glNewList** tiene dos parámetros. El primer parámetro, *list*, es un entero positivo que se convierte en el nombre único de la lista para mostrar. Los nombres se pueden crear y reservar [**con glGenLists**](glgenlists.md) y probar la [**unidad con glIsList.**](glislist.md) El segundo parámetro, *mode*, es una constante simbólica que puede asumir uno de los dos valores anteriores.

Algunos comandos no se compilan en la lista de visualización, pero se ejecutan inmediatamente, independientemente del modo de lista de presentación. Estos comandos son [**glColorPointer,**](glcolorpointer.md) [**glDeleteLists,**](gldeletelists.md) [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList,**](glislist.md) [**glNormalPointer,**](glnormalpointer.md) [**glPopClientAttrib,**](glpopclientattrib.md) [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib,**](glpushclientattrib.md) [**glReadPixels,**](glreadpixels.md) [**glRenderMode,**](glrendermode.md) [**glSelectBuffer,**](glselectbuffer.md) [**glTexCoordPointer,**](gltexcoordpointer.md) [**glVertexPointer**](glvertexpointer.md)y todas las rutinas [**glGet.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

Del mismo modo, [**glTexImage2D**](glteximage2d.md) y [**glTexImage1D**](glteximage1d.md) se ejecutan inmediatamente y no se compilan en la lista de presentación cuando su primer argumento es GL \_ PROXY TEXTURE 2D o GL PROXY TEXTURE \_ \_ \_ \_ \_ 1D, respectivamente.

Cuando se encuentra la función **glEndList,** la definición de la lista para mostrar se completa asociando la lista a la lista de nombres únicos *(especificada* en el **comando glNewList).** Si ya existe una lista para mostrar con la *lista* de nombres, solo se reemplaza cuando se llama **a glEndList.**

Las [**funciones glCallList**](glcalllist.md) y [**glCallLists**](glcalllists.md) se pueden especificar en listas para mostrar. Los comandos de la lista de visualización o las listas ejecutadas por **glCallList** o **glCallLists** no se incluyen en la lista de visualización que se va a crear, incluso si el modo de creación de la lista es GL \_ COMPILE AND \_ \_ EXECUTE.

La función siguiente recupera información relacionada con **glNewList**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**glEndList**](glendlist.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> </dl>

 

 





