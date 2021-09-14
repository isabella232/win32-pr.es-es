---
title: Función glColorMaterial (Gl.h)
description: La función glColorMaterial hace que un color de material realice un seguimiento del color actual.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- Función glColorMaterial OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362100"
---
# <a name="glcolormaterial-function"></a>Función glColorMaterial

La **función glColorMaterial** hace que un color de material realice un seguimiento del color actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cara* 
</dt> <dd>

Especifica si los parámetros front, back o front y back material deben realizar un seguimiento del color actual. Los valores aceptados \_ son GL FRONT, GL \_ BACK y GL FRONT AND \_ \_ \_ BACK. El valor predeterminado es GL \_ FRONT \_ AND \_ BACK.

</dd> <dt>

*mode* 
</dt> <dd>

Especifica cuál de varios parámetros de material realiza un seguimiento del color actual. Los valores aceptados \_ son GL EMISSION, GL \_ AMBIENT, GL \_ DIFUSO, GL \_ SPECULAR y GL AMBIENT AND \_ \_ \_ DIFFUSE. El valor predeterminado es GL \_ AMBIENT \_ AND \_ DIFFUSE.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *face* o *mode* no era un valor aceptado.<br/>                                                                                |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glColorMaterial** especifica qué parámetros de material realiza un seguimiento del color actual. Al habilitar GL COLOR MATERIAL, para cada uno de los materiales o materiales especificados por la cara , el parámetro de material o los parámetros especificados por el modo realizarán un seguimiento del \_ color actual en todo \_ momento.   Habilite y deshabilite GL COLOR MATERIAL con las funciones \_ \_ [**glEnable**](glenable.md) y [**glDisable**](gldisable.md), a las que se llama con \_ GL COLOR MATERIAL como \_ argumento. De forma predeterminada, GL \_ COLOR \_ MATERIAL está deshabilitado.

Con **glColorMaterial,** puede cambiar un subconjunto de parámetros de material para cada vértice usando solo la función [**glColor,**](glcolor-functions.md) sin llamar a [**glMaterial**](glmaterial-functions.md). Si va a especificar solo este subconjunto de parámetros para cada vértice, es mejor hacerlo con **glColorMaterial** que con **glMaterial.**

Las siguientes funciones recuperan información relacionada **con glColorMaterial**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ COLOR \_ MATERIAL \_ PARAMETER

**glGet** con el argumento GL \_ COLOR \_ MATERIAL \_ FACE

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ COLOR \_ MATERIAL

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





