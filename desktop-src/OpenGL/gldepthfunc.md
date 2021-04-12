---
title: función glDepthFunc (GL. h)
description: La función glDepthFunc especifica el valor utilizado para las comparaciones de búfer de profundidad.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- glDepthFunc (función) OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489736"
---
# <a name="gldepthfunc-function"></a>glDepthFunc función)

La función **glDepthFunc** especifica el valor utilizado para las comparaciones de búfer de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*func* 
</dt> <dd>

Especifica la función de comparación de profundidad. Se aceptan las siguientes constantes simbólicas.



| Value                                                                                                                                                   | Significado                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nunca**</dt> </dl>          | Nunca pasa.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**CONTABILIDAD \_ inferior**</dt> </dl>             | Pasa si el valor *z* entrante es menor que el valor *z* almacenado. Este es el valor predeterminado.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Pasa si el valor z entrante es menor o igual que el valor z almacenado.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**igual a GL \_**</dt> </dl>          | Pasa si el valor z entrante es igual al valor z almacenado.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**LIBRO \_ superior**</dt> </dl>    | Pasa si el valor z entrante es mayor que el valor z almacenado.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**NOTEQUAL en GL \_**</dt> </dl> | Pasa si el valor z entrante no es igual que el valor z almacenado.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Se pasa si el valor z entrante es mayor o igual que el valor z almacenado.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ siempre**</dt> </dl>       | Siempre pasa.<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glDepthFunc** especifica la función que se usa para comparar cada valor *z* de píxel entrante con el valor *z* presente en el búfer de profundidad. La comparación se realiza solo si está habilitada la prueba de profundidad. (Consulte [**glEnable**](glenable.md) con el argumento GL \_ prueba de profundidad \_ ).

Inicialmente, las pruebas de profundidad están deshabilitadas.

Las siguientes funciones recuperan información relacionada con **glDepthFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de profundidad de libro de contabilidad \_ \_

[**glIsEnabled**](glisenabled.md) con el argumento \_ prueba de profundidad de GL \_

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

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





