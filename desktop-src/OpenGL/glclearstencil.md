---
title: Función glClearStencil (Gl.h)
description: La función glClearStencil especifica el valor sin borrar para el búfer de galería de símbolos.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- Función glClearStencil OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4749a8d9c4844bd95181a7353bb0ce4559001fa47164fec3dbab5c188de8d994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618035"
---
# <a name="glclearstencil-function"></a>Función glClearStencil

La **función glClearStencil** especifica el valor sin borrar para el búfer de galería de símbolos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* 
</dt> <dd>

Índice utilizado cuando se borra el búfer de galería de símbolos. El valor predeterminado es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glClearStencil** especifica el índice utilizado por [**glClear**](glclear.md) para borrar el búfer de galería de símbolos. El *parámetro s* se enmascara con 2 <sup>m</sup>  - 1, donde *m* es el número de bits del búfer de galería de símbolos.

Las funciones siguientes recuperan información relacionada con **la función glClearStencil:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ STENCIL \_ CLEAR \_ VALUE

**glGet con** el argumento GL \_ STENCIL \_ BITS

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





