---
description: El mensaje TAPI LINE \_ REPLY se envía para notificar los resultados de las llamadas de función que se completaron de forma asincrónica.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: LINE_REPLY mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250040"
---
# <a name="line_reply-message"></a>MENSAJE \_ DE RESPUESTA DE LÍNEA

El mensaje TAPI **LINE \_ REPLY** se envía para notificar los resultados de las llamadas de función que se completaron de forma asincrónica.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

No se usa.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Devuelve la instancia de devolución de llamada de la aplicación.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de solicitud para el que se trata de la respuesta.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Indicación de éxito o error. La aplicación debe convertir este parámetro en LONG. Cero indica que el resultado es correcto; Un número negativo indica un error.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones que operan de forma asincrónica devuelven un valor de identificador de solicitud positivo a la aplicación. Este identificador de solicitud se devuelve con el mensaje de respuesta para identificar la solicitud que se completó. El otro parámetro para el mensaje **LINE \_ REPLY** lleva la indicación de éxito o error. Los posibles errores son los mismos que los definidos por la función correspondiente. Este mensaje no se puede deshabilitar.

En algunos casos, una aplicación puede no recibir el mensaje **LINE \_ REPLY** correspondiente a una llamada a una función asincrónica. Esto sucede si el identificador de llamada correspondiente se desasigna antes de que se reciba el mensaje.

> [!Note]  
> Cuando una aplicación invoca cualquier operación asincrónica que reescriba datos en la memoria de la aplicación, la aplicación debe mantener esa memoria disponible para su escritura hasta que se reciba un mensaje **LINE \_ REPLY** o [**LINE \_ GATHERDIGITS.**](line-gatherdigits.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> </dl>

 

 




