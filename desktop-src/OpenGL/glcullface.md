---
title: Función glCullFace (Gl.h)
description: La función glCullFace especifica si se pueden seleccionar facetas orientadas al frente o hacia atrás.
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
ms.openlocfilehash: 70fd983e9a5921d96ba487f7eb8d6f631b000019e8ff566eb1ecc79e05ce4fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081675"
---
# <a name="glcullface-function"></a>Función glCullFace

La **función glCullFace** especifica si se pueden seleccionar facetas orientadas al frente o hacia atrás.

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

Especifica si las facetas orientadas hacia delante o hacia atrás son candidatas para la selección. Se aceptan las constantes simbólicas GL \_ FRONT, GL \_ BACK y GL FRONT AND \_ \_ \_ BACK. El valor predeterminado es GL \_ BACK.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *mode* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glCullFace** especifica si las facetas orientadas hacia delante o hacia atrás se completan (como se especifica en el modo *)* cuando está habilitada la selección de facetas. Puede habilitar y deshabilitar la selección de facetas mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ CULL \_ FACE. Las facetas incluyen triángulos, cuadriláteros, polígonos y rectángulos.

La [**función glFrontFace**](glfrontface.md) especifica cuáles de las facetas en el sentido de las agujas del reloj y en sentido contrario a las agujas del reloj son orientadas hacia delante y hacia atrás.

Si *el modo* es GL FRONT AND BACK, no se dibuja ninguna faceta, pero se dibujan \_ \_ \_ otras primitivas, como puntos y líneas.

Las funciones siguientes recuperan información relacionada **con glCullFace**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CULL \_ FACE \_ MODE

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ CULL \_ FACE

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

 

 





