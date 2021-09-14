---
title: Función glGetError (Gl.h)
description: La función glGetError devuelve información de error.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- Función glGetError OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260260"
---
# <a name="glgeterror-function"></a>Función glGetError

La **función glGetError** devuelve información de error.

## <a name="syntax"></a>Sintaxis


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La **función glGetError** devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                           | Descripción                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | Se especifica un valor inaceptable para un argumento enumerado. La función de ofendencia se omite, sin ningún efecto secundario que no sea establecer la marca de error.<br/>         |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | Un argumento numérico está fuera del intervalo. La función de ofendencia se omite, sin ningún efecto secundario que no sea establecer la marca de error.<br/>                                    |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | No se permite la operación especificada en el estado actual. La función de ofendencia se omite, sin ningún efecto secundario que no sea establecer la marca de error.<br/>           |
| <dl> <dt>**GL \_ NO \_ ERROR**</dt> </dl>          | No se ha registrado ningún error. Se garantiza que el valor de esta constante simbólica es cero.<br/>                                                                         |
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Esta función provocaría un desbordamiento de pila. La función de ofendencia se omite, sin ningún efecto secundario que no sea establecer la marca de error.<br/>                            |
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Esta función provocaría un subdesbordamiento de la pila. La función de ofendencia se omite, sin ningún efecto secundario que no sea establecer la marca de error.<br/>                           |
| <dl> <dt>**GL \_ FUERA \_ DE \_ MEMORIA**</dt> </dl>    | No queda suficiente memoria para ejecutar la función. El estado de OpenGL no está definido, excepto el estado de las marcas de error, después de registrar este error.<br/> |



 

Tenga en **cuenta que glGetError** devuelve GL INVALID OPERATION si se llama entre una llamada \_ a \_ [**glBegin**](glbegin.md) y su llamada correspondiente [**a glEnd**](glend.md).

## <a name="remarks"></a>Observaciones

A cada error detectable se le asigna un código numérico y un nombre simbólico. Cuando se produce un error, la marca de error se establece en el valor de código de error adecuado. No se registran otros errores hasta que **se llama a glGetError,** se devuelve el código de error y la marca se restablece a GL \_ NO \_ ERROR. Si una llamada a **glGetError** devuelve GL NO ERROR, no se ha producido ningún error detectable desde la última llamada a glGetError o desde que se inicializó \_ \_ OpenGL. 

Para permitir implementaciones distribuidas, puede haber varias marcas de error. Si alguna marca de error única ha registrado un error, se devuelve el valor de esa marca y esa marca se restablece a GL NO ERROR cuando se llama \_ \_ a **glGetError.** Si más de una marca ha registrado un error, **glGetError** devuelve y borra un valor de marca de error arbitrario. Si se van a restablecer todas las marcas de error, siempre debe llamar a **glGetError** en un bucle hasta que devuelva GL \_ NO \_ ERROR.

Inicialmente, todas las marcas de error se establecen en GL \_ NO \_ ERROR.

Cuando se establece una marca de error, los resultados de una operación OpenGL solo son indefinidos si se ha producido \_ GL OUT \_ OF \_ MEMORY. En todos los demás casos, la función que genera el error se omite y no tiene ningún efecto en el estado OpenGL ni en el contenido del búfer de fotogramas.

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

[**glEnd**](glend.md)
</dt> </dl>

 

 





