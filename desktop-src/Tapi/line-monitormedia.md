---
description: El mensaje de LINE_MONITORMEDIA TAPI se envía cuando se detecta un cambio en el tipo de medio de llamadas. El envío de este mensaje se controla con la función lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: LINE_MONITORMEDIA mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fec42f0e8aa630b518f989a9237762edc71281767b281f7af78eb54210138d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519025"
---
# <a name="line_monitormedia-message"></a>LINE \_ MONITORMedia message

El mensaje TAPI **LINE \_ MONITORMEDIA** se envía cuando se detecta un cambio en el tipo de medio de la llamada. El envío de este mensaje se controla con la [**función lineMonitorMedia.**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia)


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

Nuevo tipo de medio (o modo). Este parámetro debe ser uno y solo una de las [**constantes LINEMEDIAMODE \_**](linemediamode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

El "número de pasos" (número de milisegundos desde que Windows inició) en el que se detectó el medio especificado. Para las versiones de TAPI anteriores a la 2.0, este parámetro no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ LINE MONITORMEDIA** se envía a la aplicación que ha habilitado la supervisión de medios para el tipo de medio detectado.

Dado que esta marca de tiempo se puede haber generado en un equipo distinto del en el que se ejecuta la aplicación, solo es útil para la comparación con otros mensajes con marca de tiempo similares generados en el mismo dispositivo de línea [**(LINE \_ GATHERDIGITS,**](line-gatherdigits.md) [**LINE \_ GENERATE**](line-generate.md), [**LINE \_ MONITORDIGITS**](line-monitordigits.md), [**LINE \_ MONITORTONE),**](line-monitortone.md)con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de tics puede "encapsular" después de aproximadamente 49,7 días. Las aplicaciones deben tener esto en cuenta al realizar cálculos.

Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**GENERACIÓN \_ DE LÍNEA**](line-generate.md)
</dt> <dt>

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




