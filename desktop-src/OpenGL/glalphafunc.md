---
title: función glAlphaFunc (GL. h)
description: La función glAlphaFunc permite que la aplicación establezca la función de prueba alfa.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glAlphaFunc (función) OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686009"
---
# <a name="glalphafunc-function"></a>glAlphaFunc función)

La función **glAlphaFunc** permite que la aplicación establezca la función de prueba alfa.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*func* 
</dt> <dd>

Función de comparación alfa. A continuación se indican las constantes simbólicas aceptadas y su significado.



| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nunca**</dt> </dl>          | Nunca pasa.<br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**CONTABILIDAD \_ inferior**</dt> </dl>             | Pasa si el valor alfa de entrada es menor que el valor de referencia.<br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**igual a GL \_**</dt> </dl>          | Pasa si el valor alfa entrante es igual al valor de referencia.<br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Pasa si el valor alfa entrante es menor o igual que el valor de referencia.<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**LIBRO \_ superior**</dt> </dl>    | Pasa si el valor alfa entrante es mayor que el valor de referencia.<br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**NOTEQUAL en GL \_**</dt> </dl> | Pasa si el valor alfa entrante no es igual que el valor de referencia.<br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Pasa si el valor alfa entrante es mayor o igual que el valor de referencia.<br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ siempre**</dt> </dl>       | Siempre pasa. Este es el valor predeterminado.<br/>                                                 |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valor de referencia con el que se comparan los valores alfa entrantes. Este valor se fija en el intervalo comprendido entre 0 y 1, donde 0 representa el valor alfa más bajo posible y 1 el valor más alto posible. La referencia predeterminada es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *FUNC* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La prueba alfa descarta los fragmentos según el resultado de una comparación entre los valores alfa de los fragmentos entrantes y un valor de referencia constante. La función **glAlphaFunc** especifica la función de referencia y de comparación. La comparación solo se realiza si está habilitada la prueba alfa. (Para obtener más información sobre GL \_ ) La \_ prueba alfa, vea [**glEnable**](glenable.md)).

Los parámetros *FUNC* y *ref* especifican las condiciones en las que se dibuja el píxel. El valor alfa entrante se compara con *ref* mediante la función especificada por *FUNC*. Si se pasa la comparación, se dibuja el fragmento entrante, condicional en las siguientes pruebas de estarcido y de búfer de profundidad. Si se produce un error en la comparación, no se realiza ningún cambio en el fotogramas en esa ubicación de píxeles.

La función **glAlphaFunc** funciona en todas las escrituras de píxeles, incluidas las que resultan de la conversión de recorrido de puntos, líneas, polígonos y mapas de bits, así como de las operaciones de copia y dibujo de píxeles. La función **glAlphaFunc** no afecta a las operaciones de borrado de pantalla.

La prueba alfa solo se realiza en el modo RGBA.

Las siguientes funciones recuperan información relacionada con la función **glAlphaFunc** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ FUNC Alpha test \_ FUNC

**glGet** con argumento referencia de prueba de GL \_ alpha \_ \_

[**glIsEnabled**](glisenabled.md) con el argumento \_ prueba de GL alpha \_

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





