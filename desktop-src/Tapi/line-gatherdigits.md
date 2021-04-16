---
description: El mensaje de línea de \_ GATHERDIGITS TAPI se envía cuando la solicitud de recopilación de dígitos almacenada en búfer actual ha finalizado o se ha cancelado. El búfer de dígitos se puede examinar una vez que la aplicación ha recibido este mensaje.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Mensaje de LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679468"
---
# <a name="line_gatherdigits-message"></a>Mensaje de línea \_ GATHERDIGITS

El mensaje de **línea de \_ GATHERDIGITS** TAPI se envía cuando la solicitud de recopilación de dígitos almacenada en búfer actual ha finalizado o se ha cancelado. El búfer de dígitos se puede examinar una vez que la aplicación ha recibido este mensaje.


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

Motivo por el que finalizó la recopilación de dígitos. Este parámetro debe ser una y solo una de las [**\_ constantes LINEGATHERTERM**](linegatherterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se completó la recopilación del dígito. En el caso de las versiones de TAPI anteriores a 2,0, este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje **line \_ GATHERDIGITS** solo se envía a la aplicación que inició la recopilación de dígitos en la llamada con [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).

Si se usa la función [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) para cancelar una solicitud anterior para recopilar dígitos, TAPI envía un mensaje de **línea \_ GATHERDIGITS** con *dwParam1* establecido en LINEGATHERTERM \_ cancelar a la aplicación que indica que el búfer especificado originalmente contiene los dígitos recopilados hasta la cancelación.

Dado que la marca de tiempo especificada por *dwParam3* puede haberse generado en un equipo que no sea el en el que se está ejecutando la aplicación, solo es útil para la comparación con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**\_ generación**](line-generate.md)de línea, [**línea \_ MONITORDIGITS**](line-monitordigits.md), línea [**\_ MONITORMEDIA**](line-monitormedia.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.

Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.

> [!Note]  
> Cuando una aplicación invoca cualquier operación asincrónica que vuelva a escribir datos en la memoria de la aplicación, la aplicación debe mantener esa memoria disponible para escritura hasta que se reciba un mensaje de línea o [**\_ respuesta de línea**](line-reply.md) **\_ GATHERDIGITS** .

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**generación de línea \_**](line-generate.md)
</dt> <dt>

[**LÍNEA \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LÍNEA \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LÍNEA \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**respuesta de línea \_**](line-reply.md)
</dt> <dt>

[**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




