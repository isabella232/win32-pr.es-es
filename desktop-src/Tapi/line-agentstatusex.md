---
description: El \_ mensaje line AGENTSTATUSEX se envía cuando cambia el estado de un agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Mensaje de LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680774"
---
# <a name="line_agentstatusex-message"></a>Mensaje de línea \_ AGENTSTATUSEX

El mensaje **line \_ AGENTSTATUSEX** se envía cuando cambia el estado de un agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

Identificador de la aplicación para el dispositivo de línea. Esto se relaciona con el controlador del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador del agente cuyo estado ha cambiado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado de la cola que ha cambiado. Puede ser una o varias de las [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam2* incluye el \_ bit de estado LINEAGENTSTATUSEX, *dwParam3* indica el nuevo valor del estado del agente, que es una de [**las \_ constantes de LINEAGENTSTATEEX**](lineagentstateex--constants.md).

De lo contrario, *dwParam3* se establece en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




