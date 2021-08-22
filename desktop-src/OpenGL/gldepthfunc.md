---
title: Función glDepthFunc (Gl.h)
description: La función glDepthFunc especifica el valor utilizado para las comparaciones de búfer de profundidad.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- Función GlDepthFunc OpenGL
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
ms.openlocfilehash: 229b269e8d9677e0ffdedffb3d91029a473292082409830ac26490bf34680075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617050"
---
# <a name="gldepthfunc-function"></a>Función glDepthFunc

La **función glDepthFunc** especifica el valor utilizado para las comparaciones de búfer de profundidad.

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
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Nunca pasa.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Pasa si el valor *z* entrante es menor que el valor *z* almacenado. Este es el valor predeterminado.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Pasa si el valor z entrante es menor o igual que el valor z almacenado.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ EQUAL**</dt> </dl>          | Pasa si el valor z entrante es igual al valor z almacenado.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ GREATER**</dt> </dl>    | Pasa si el valor z entrante es mayor que el valor z almacenado.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Pasa si el valor z entrante no es igual al valor z almacenado.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Pasa si el valor z entrante es mayor o igual que el valor z almacenado.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Siempre pasa.<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glDepthFunc** especifica la función que se usa para comparar cada valor *z* de píxel entrante con el valor *z* presente en el búfer de profundidad. La comparación solo se realiza si está habilitada la prueba de profundidad. (Vea [**glEnable**](glenable.md) con el argumento GL \_ PRUEBA \_ DE PROFUNDIDAD).

Inicialmente, las pruebas de profundidad están deshabilitadas.

Las funciones siguientes recuperan información relacionada **con glDepthFunc**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ DEPTH \_ FUNC

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ DEPTH \_ TEST

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

 

 





