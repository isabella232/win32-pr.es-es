---
title: función glGetError (GL. h)
description: La función glGetError devuelve información de error.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glGetError (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996947"
---
# <a name="glgeterror-function"></a>glGetError función)

La función **glGetError** devuelve información de error.

## <a name="syntax"></a>Sintaxis


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La función **glGetError** devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                           | Descripción                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | Se ha especificado un valor inaceptable para un argumento enumerado. La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.<br/>         |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | Un argumento numérico está fuera del intervalo. La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.<br/>                                    |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | No se permite la operación especificada en el estado actual. La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.<br/>           |
| <dl> <dt>**GL \_ no \_ error**</dt> </dl>          | No se ha registrado ningún error. Se garantiza que el valor de esta constante simbólica es cero.<br/>                                                                         |
| <dl> <dt>**desbordamiento de la pila de GL \_ \_**</dt> </dl>    | Esta función produciría un desbordamiento de pila. La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.<br/>                            |
| <dl> <dt>**subdesbordamiento de la pila de GL \_ \_**</dt> </dl>   | Esta función produciría un subdesbordamiento de la pila. La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.<br/>                           |
| <dl> <dt>**\_memoria insuficiente para GL \_ \_**</dt> </dl>    | No queda suficiente memoria para ejecutar la función. El estado de OpenGL es indefinido, excepto el estado de las marcas de error, después de que se registre este error.<br/> |



 

Tenga en cuenta que **glGetError** devuelve \_ una operación no válida GL \_ si se llama entre una llamada a [**glBegin**](glbegin.md) y su correspondiente llamada a [**glEnd**](glend.md).

## <a name="remarks"></a>Observaciones

A cada error detectable se le asigna un código numérico y un nombre simbólico. Cuando se produce un error, la marca de error se establece en el valor de código de error adecuado. No se registra ningún otro error hasta que se llama a **glGetError** , se devuelve el código de error y la marca se restablece a GL \_ no \_ error. Si una llamada a **glGetError** devuelve GL \_ no \_ error, no habrá ningún error detectable desde la última llamada a **glGetError** o desde que se inicializó OpenGL.

Para permitir implementaciones distribuidas, puede haber varias marcas de error. Si una marca de error individual ha registrado un error, se devuelve el valor de esa marca y la marca se restablece en GL \_ sin \_ errores cuando se llama a **glGetError** . Si se ha registrado un error en más de una marca, **glGetError** devuelve y borra un valor de marca de error arbitrario. Si todas las marcas de error se van a restablecer, siempre debe llamar a **glGetError** en un bucle hasta que devuelva GL \_ no \_ error.

Inicialmente, todas las marcas de error se establecen en GL \_ no \_ error.

Cuando se establece una marca de error, los resultados de una operación de OpenGL no se definen solo si se \_ ha agotado el libro \_ de \_ memoria. En todos los demás casos, la función que genera el error se omite y no tiene ningún efecto en el contenido de fotogramas o estado de OpenGL.

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

[**glEnd**](glend.md)
</dt> </dl>

 

 





