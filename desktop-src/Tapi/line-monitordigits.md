---
description: El mensaje de línea de \_ MONITORDIGITS TAPI se envía cuando se detecta un dígito. El envío de este mensaje se controla con la función lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Mensaje de LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680253"
---
# <a name="line_monitordigits-message"></a>Mensaje de línea \_ MONITORDIGITS

El mensaje de **línea de \_ MONITORDIGITS** TAPI se envía cuando se detecta un dígito. El envío de este mensaje se controla con la función [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .


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

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

El byte de orden inferior contiene el último dígito recibido en una representación de texto.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Modo de dígito que se ha detectado. Este parámetro debe ser una y solo una de las [**\_ constantes LINEDIGITMODE**](linedigitmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se detectó el dígito especificado. En el caso de las versiones de TAPI anteriores a 2,0, este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje **line \_ MONITORDIGITS** se envía a la aplicación que ha habilitado la supervisión de dígitos.

Dado que esta marca de tiempo se puede haber generado en un equipo que no sea el en el que se ejecuta la aplicación, solo resulta útil para compararla con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**\_ GATHERDIGITS de línea**](line-gatherdigits.md), [**\_ generación**](line-generate.md)de línea, [**línea \_ MONITORMEDIA**](line-monitormedia.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.

Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**generación de línea \_**](line-generate.md)
</dt> <dt>

[**LÍNEA \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LÍNEA \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




