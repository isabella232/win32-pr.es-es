---
title: Función glCullFace (Gl.h)
description: La función glCullFace especifica si se pueden realizar facetas orientadas al frente o hacia atrás.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- Función glCullFace OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362085"
---
# <a name="glcullface-function"></a>función glCullFace

La **función glCullFace** especifica si se pueden realizar facetas orientadas al frente o hacia atrás.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Especifica si las facetas orientadas hacia delante o hacia atrás son candidatas para la selección. Se aceptan las constantes simbólicas \_ GL FRONT, GL \_ BACK y GL FRONT AND \_ \_ \_ BACK. El valor predeterminado es GL \_ BACK.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *el modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glCullFace** especifica si las facetas orientadas hacia delante o hacia atrás se completan (tal y como especifica el modo *)* cuando está habilitada la selección de facetas. Habilite y deshabilite la selección de facetas mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ CULL \_ FACE. Las facetas incluyen triángulos, cuadránteros, polígonos y rectángulos.

La [**función glFrontFace**](glfrontface.md) especifica cuáles de las facetas en el sentido de las agujas del reloj y en el sentido contrario a las agujas del reloj son orientadas hacia delante y hacia atrás.

Si *el modo* es GL FRONT Y BACK, no se dibuja ninguna faceta, pero se dibujan \_ \_ \_ otras primitivas, como puntos y líneas.

Las funciones siguientes recuperan información relacionada **con glCullFace**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ CULL \_ FACE \_ MODE

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ CULL \_ FACE

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





