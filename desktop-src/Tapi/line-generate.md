---
description: El mensaje TAPI LINE GENERATE se envía para notificar a la aplicación que la generación de tono o dígito \_ actual ha finalizado.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: LINE_GENERATE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3ab0d503d7515fec2cdbd1676eed235cced88e2adfa9fcc1dd354663929e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774245"
---
# <a name="line_generate-message"></a>MENSAJE \_ LINE GENERATE

El mensaje TAPI **LINE \_ GENERATE** se envía para notificar a la aplicación que la generación de tono o dígito actual ha finalizado. Solo una solicitud de generación de este tipo puede estar en curso una llamada determinada en cualquier momento. Este mensaje también se envía cuando se cancela la generación de dígitos o tono.


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

Motivo por el que se finalizó la generación de dígitos o tono. Este parámetro debe ser uno y solo una de las [**constantes LINEGENERATETERM \_**](linegenerateterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

El "recuento de tics" (número de milisegundos desde que Windows inició) en el que se completó la generación de dígitos o tono. Para las versiones de API anteriores a la 2.0, este parámetro no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje LINE \_ GENERATE** solo se envía a la aplicación que solicitó la generación de dígitos o tono.

Dado que la marca de tiempo especificada por *dwParam3* puede haber sido generada en un equipo distinto del en el que se ejecuta la aplicación, solo es útil para la comparación con otros mensajes con marca de tiempo similares generados en el mismo dispositivo de línea [**(LINE \_ GATHERDIGITS**](line-gatherdigits.md), [**LINE \_ MONITORDIGITS**](line-monitordigits.md), [**LINE \_ MONITORMEDIA**](line-monitormedia.md), [**LINE \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos). El recuento de tics puede "encapsular" después de aproximadamente 49,7 días. Las aplicaciones deben tener esto en cuenta al realizar cálculos.

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

[**LINE \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINE \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**LINE \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




