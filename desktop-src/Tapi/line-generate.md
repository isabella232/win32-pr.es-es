---
description: Se envía el mensaje de generación de línea TAPI \_ para notificar a la aplicación que ha finalizado la generación de dígitos o tono actual.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Mensaje de LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690699"
---
# <a name="line_generate-message"></a>Mensaje de generación de línea \_

Se envía el mensaje de generación de **línea \_** TAPI para notificar a la aplicación que ha finalizado la generación de dígitos o tono actual. Solo una solicitud de este tipo puede estar en curso en una llamada determinada en cualquier momento. Este mensaje también se envía cuando se cancela la generación de dígitos o de tono.


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

Razón por la que finalizó la generación de dígitos o tono. Este parámetro debe ser una y solo una de las [**\_ constantes LINEGENERATETERM**](linegenerateterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se completó la generación de dígitos o tono. En el caso de las versiones de API anteriores a 2,0, este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje de generación de **línea \_** solo se envía a la aplicación que solicitó la generación de dígitos o tono.

Dado que la marca de tiempo especificada por *dwParam3* puede haberse generado en un equipo que no sea el en el que se ejecuta la aplicación, solo es útil para la comparación con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**línea \_ GATHERDIGITS**](line-gatherdigits.md), [**línea \_ MONITORDIGITS**](line-monitordigits.md), [**línea \_ MONITORMEDIA**](line-monitormedia.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su temporización relativa (separación entre eventos). El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.

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

[**LÍNEA \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LÍNEA \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LÍNEA \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




