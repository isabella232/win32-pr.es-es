---
description: El mensaje TAPI LINE GATHERDIGITS se envía cuando la solicitud de recopilación de dígitos almacenados en búfer actual ha finalizado \_ o se ha cancelado. El búfer de dígitos se puede examinar después de que la aplicación haya recibido este mensaje.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: LINE_GATHERDIGITS mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250107"
---
# <a name="line_gatherdigits-message"></a>Mensaje \_ LINE GATHERDIGITS

El mensaje TAPI **LINE \_ GATHERDIGITS** se envía cuando la solicitud de recopilación de dígitos almacenados en búfer actual ha finalizado o se ha cancelado. El búfer de dígitos se puede examinar después de que la aplicación haya recibido este mensaje.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la llamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Motivo por el que se finalizó la recopilación de dígitos. Este parámetro debe ser uno y solo una de las [**constantes LINEGATHERTERM \_**](linegatherterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

El "recuento de pasos" (número de milisegundos desde que Windows inició) en el que se completó la recopilación de dígitos. En el caso de las versiones tapi anteriores a la 2.0, este parámetro no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **mensaje \_ LINE GATHERDIGITS** solo se envía a la aplicación que inició la recopilación de dígitos en la llamada [**mediante lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).

Si la función [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) se usa para cancelar una solicitud anterior para recopilar dígitos, TAPI envía un mensaje **LINE \_ GATHERDIGITS** con *dwParam1* establecido en LINEGATHERTERM CANCEL a la aplicación que indica que el búfer especificado originalmente contiene los dígitos recopilados hasta \_ la cancelación.

Dado que la marca de tiempo especificada por *dwParam3* puede haber sido generada en un equipo distinto del en el que se ejecuta la aplicación, solo es útil para la comparación con otros mensajes con marca de tiempo similares generados en el mismo dispositivo de línea [**(LINE \_ GENERATE**](line-generate.md), [**LINE \_ MONITORDIGITS**](line-monitordigits.md), [**LINE \_ MONITORMEDIA**](line-monitormedia.md), [**LINE \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de tics puede "encapsular" después de aproximadamente 49,7 días. las aplicaciones deben tener esto en cuenta al realizar cálculos.

Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.

> [!Note]  
> Cuando una aplicación invoca cualquier operación asincrónica que vuelva a escribir datos en la memoria de la aplicación, la aplicación debe mantener esa memoria disponible para escritura hasta que se reciba un mensaje [**LINE \_ REPLY**](line-reply.md) o **LINE \_ GATHERDIGITS.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GENERACIÓN \_ DE LÍNEA**](line-generate.md)
</dt> <dt>

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINE \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**RESPUESTA \_ DE LÍNEA**](line-reply.md)
</dt> <dt>

[**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




