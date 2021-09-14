---
description: El mensaje TAPI LINE \_ MONITORTONE se envía cuando se detecta un tono. El envío de este mensaje se controla con la función lineMonitorMonitorMonitor.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: LINE_MONITORTONE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250094"
---
# <a name="line_monitortone-message"></a>Mensaje \_ LINE MONITORTONE

El mensaje TAPI **LINE \_ MONITORTONE** se envía cuando se detecta un tono. El envío de este mensaje se controla con la [**función lineMonitorMonitorMonitor.**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)


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

Miembro **dwAppSpecific específico** de la aplicación de la [**estructura LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) para el tono detectado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

El "recuento de tics" (número de milisegundos desde Windows inició) en el que se detectó el tono. Para las versiones de API anteriores a la 2.0, este parámetro no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **mensaje \_ LINE MONITORTONE** solo se envía a la aplicación que ha solicitado que se supervise el tono.

Dado que esta marca de tiempo se puede haber generado en un equipo distinto del en el que se ejecuta la aplicación, solo es útil para la comparación con otros mensajes con marca de tiempo similares generados en el mismo dispositivo de línea [**(LINE \_ GATHERDIGITS**](line-gatherdigits.md), [**LINE \_ GENERATE**](line-generate.md), [**LINE \_ MONITORDIGITS**](line-monitordigits.md), **LINE \_ MONITORTONE**), con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de tics puede "encapsular" después de aproximadamente 49,7 días. las aplicaciones deben tener esto en cuenta al realizar cálculos.

Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**GENERACIÓN \_ DE LÍNEA**](line-generate.md)
</dt> <dt>

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[**lineMonitorMonitorMonitor**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




