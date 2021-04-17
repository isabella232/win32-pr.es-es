---
description: El \_ mensaje de respuesta de línea TAPI se envía para informar de los resultados de las llamadas a funciones que se completaron de forma asincrónica.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Mensaje de LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690977"
---
# <a name="line_reply-message"></a>Mensaje de respuesta de línea \_

El mensaje **de \_ respuesta de línea** TAPI se envía para informar de los resultados de las llamadas a funciones que se completaron de forma asincrónica.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Devuelve la instancia de devolución de llamada de la aplicación.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de solicitud para el que es la respuesta.

</dd> <dt>

*dwParam2* 
</dt> <dd>

La indicación de error o correcto. La aplicación debe convertir este parámetro en un valor LONG. Cero indica que se ha realizado correctamente; un número negativo indica un error.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones que operan de forma asincrónica devuelven un valor de identificador de solicitud positivo a la aplicación. Este identificador de solicitud se devuelve con el mensaje de respuesta para identificar la solicitud que se completó. El otro parámetro para el mensaje de **\_ respuesta de línea** contiene la indicación de éxito o error. Los errores posibles son los mismos que los definidos por la función correspondiente. Este mensaje no se puede deshabilitar.

En algunos casos, es posible que una aplicación no reciba el mensaje de **\_ respuesta de línea** correspondiente a una llamada a una función asincrónica. Esto sucede si se cancela la asignación del identificador de llamada correspondiente antes de que se haya recibido el mensaje.

> [!Note]  
> Cuando una aplicación invoca cualquier operación asincrónica que vuelva a escribir datos en la memoria de la aplicación, la aplicación debe mantener esa memoria disponible para escritura hasta que se reciba un mensaje de línea o **\_ respuesta de línea** [**\_ GATHERDIGITS**](line-gatherdigits.md) .

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> </dl>

 

 




