---
description: El mensaje TAPI LINE \_ MONITORDIGITS se envía cuando se detecta un dígito. El envío de este mensaje se controla con la función lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: LINE_MONITORDIGITS mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49324bb90e774d15baaf58b873a7fdbfa9bfc938c8d86ea4be8514b02768bd70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774235"
---
# <a name="line_monitordigits-message"></a>LINE \_ MONITORDIGITS message

El mensaje TAPI **LINE \_ MONITORDIGITS** se envía cuando se detecta un dígito. El envío de este mensaje se controla con la [**función lineMonitorDigits.**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)


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

El byte de orden bajo contiene el último dígito recibido en una representación de texto.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Modo de dígito que se detectó. Este parámetro debe ser uno y solo una de las [**constantes LINEDIGITMODE \_**](linedigitmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

El "recuento de pasos" (número de milisegundos desde que Windows inició) en el que se detectó el dígito especificado. En el caso de las versiones tapi anteriores a la 2.0, este parámetro no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ LINE MONITORDIGITS** se envía a la aplicación que ha habilitado la supervisión de dígitos.

Dado que esta marca de tiempo puede haber sido generada en un equipo distinto del en el que se ejecuta la aplicación, solo es útil para la comparación con otros mensajes con marca de tiempo similares generados en el mismo dispositivo de línea [**(LINE \_ GATHERDIGITS**](line-gatherdigits.md), [**LINE \_ GENERATE**](line-generate.md), [**LINE \_ MONITORMEDIA**](line-monitormedia.md), [**LINE \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de tics puede "encapsular" después de aproximadamente 49,7 días. las aplicaciones deben tener esto en cuenta al realizar cálculos.

Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**GENERACIÓN \_ DE LÍNEA**](line-generate.md)
</dt> <dt>

[**LINE \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




