---
title: Función glAlphaFunc (Gl.h)
description: La función glAlphaFunc permite a la aplicación establecer la función de prueba alfa.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- Función glAlphaFunc OpenGL
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
ms.openlocfilehash: 7a0bdc04f899b9002c72eda0d4e64bf6f3bad64f8e77c5fd5daff9324fda744f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082255"
---
# <a name="glalphafunc-function"></a>Función glAlphaFunc

La **función glAlphaFunc** permite a la aplicación establecer la función de prueba alfa.

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

Función de comparación alfa. Las siguientes son las constantes simbólicas aceptadas y sus significados.



| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Nunca pasa.<br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Pasa si el valor alfa entrante es menor que el valor de referencia.<br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ EQUAL**</dt> </dl>          | Pasa si el valor alfa entrante es igual al valor de referencia.<br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Pasa si el valor alfa entrante es menor o igual que el valor de referencia.<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ GREATER**</dt> </dl>    | Pasa si el valor alfa entrante es mayor que el valor de referencia.<br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Pasa si el valor alfa entrante no es igual al valor de referencia.<br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Pasa si el valor alfa entrante es mayor o igual que el valor de referencia.<br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Siempre pasa. Este es el valor predeterminado.<br/>                                                 |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valor de referencia con el que se comparan los valores alfa entrantes. Este valor se fija en el intervalo de 0 a 1, donde 0 representa el valor alfa más bajo posible y 1 el valor más alto posible. La referencia predeterminada es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *func* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La prueba alfa descarta fragmentos en función del resultado de una comparación entre los valores alfa de los fragmentos entrantes y un valor de referencia constante. La **función glAlphaFunc** especifica la función de referencia y comparación. La comparación solo se realiza si está habilitada la prueba alfa. (Para obtener más información sobre GL \_ PRUEBA \_ ALFA, vea [**glEnable**](glenable.md)).)

Los *parámetros func* *y ref* especifican las condiciones en las que se dibuja el píxel. El valor alfa entrante se compara con *ref* mediante la función especificada por *func*. Si se supera la comparación, se dibuja el fragmento entrante, condicional en las pruebas posteriores de galería de símbolos y búfer de profundidad. Si se produce un error en la comparación, no se realiza ningún cambio en el búfer de fotogramas en esa ubicación de píxeles.

La **función glAlphaFunc** funciona en todas las escrituras de píxeles, incluidas las resultantes de la conversión de análisis de puntos, líneas, polígonos y mapas de bits, y a partir de operaciones de dibujo y copia de píxeles. La **función glAlphaFunc** no afecta a las operaciones de borrar pantalla.

Las pruebas alfa solo se realizan en modo RGBA.

Las siguientes funciones recuperan información relacionada con **la función glAlphaFunc:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ ALPHA TEST \_ \_ FUNC

**glGet con** el argumento GL \_ ALPHA TEST \_ \_ REF

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ ALPHA \_ TEST

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

 

 





