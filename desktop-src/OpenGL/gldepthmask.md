---
title: Función glDepthMask (Gl.h)
description: La función glDepthMask habilita o deshabilita la escritura en el búfer de profundidad.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- Función GlDepthMask OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e774917d47cecdbb276b19dbc97a7c8c7620e04e0a044cf6932aa83167e325
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625725"
---
# <a name="gldepthmask-function"></a>Función glDepthMask

La **función glDepthMask** habilita o deshabilita la escritura en el búfer de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flag* 
</dt> <dd>

Especifica si el búfer de profundidad está habilitado para escritura. Si *la marca* es cero, la escritura en búfer de profundidad está deshabilitada. De lo contrario, está habilitado. Inicialmente, la escritura en búfer de profundidad está habilitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La función siguiente recupera información relacionada con **glDepthMask**:

**glGet con** el argumento GL \_ DEPTH \_ WRITEMASK

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





