---
description: El mensaje de LINE_MONITORMEDIA TAPI se envía cuando se detecta un cambio en el tipo de medio de llamadas. El envío de este mensaje se controla con la función lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Mensaje de LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690364"
---
# <a name="line_monitormedia-message"></a>Mensaje de línea \_ MONITORMEDIA

El mensaje de **línea de \_ MONITORMEDIA** TAPI se envía cuando se detecta un cambio en el tipo de medio de la llamada. El envío de este mensaje se controla con la función [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .


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

Nuevo tipo de medio (o modo). Este parámetro debe ser una y solo una de las [**\_ constantes LINEMEDIAMODE**](linemediamode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se detectó el medio especificado. En el caso de las versiones de TAPI anteriores a 2,0, este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje **line \_ MONITORMEDIA** se envía a la aplicación que ha habilitado la supervisión multimedia para el tipo de medio detectado.

Dado que esta marca de tiempo se puede haber generado en un equipo que no sea el en el que se ejecuta la aplicación, solo resulta útil para compararla con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**\_ GATHERDIGITS de línea**](line-gatherdigits.md), [**\_ generación**](line-generate.md)de línea, [**línea \_ MONITORDIGITS**](line-monitordigits.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.

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

[**LÍNEA \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LÍNEA \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




