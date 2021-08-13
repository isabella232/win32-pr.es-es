---
title: Función glDeleteTextures (Gl.h)
description: La función glDeleteTextures elimina texturas con nombre.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- Función glDeleteTextures OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408019d3bfe226c9e7ecdc2ea00182a0b11c78fa64a0210be658ded4556850cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617051"
---
# <a name="gldeletetextures-function"></a>Función glDeleteTextures

La **función glDeleteTextures** elimina texturas con nombre.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Número de texturas que se eliminarán.

</dd> <dt>

*Texturas* 
</dt> <dd>

Matriz de texturas que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *n* era un valor negativo.<br/>                                                                                                  |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glDeleteTextures** elimina *n texturas* denominadas por los elementos de las *texturas de matriz*. Después de eliminar una textura, no tiene contenido ni dimensionalidad, y su nombre es libre para su reutilización (por ejemplo, **por glGenTextures**). La **función glDeleteTextures** omite los ceros y los nombres que no corresponden a las texturas existentes.

Si se elimina una textura enlazada actualmente, el enlace se revierte a cero (la textura predeterminada).

No se pueden incluir llamadas **a glDeleteTextures en** listas para mostrar.

> [!Note]  
> La **función glDeleteTextures** solo está disponible en OpenGL versión 1.1 o posterior.

 

La función siguiente recupera información relacionada con **glDeleteTextures**:

-   [**glIsTexture**](glistexture.md)

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





