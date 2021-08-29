---
description: El mensaje LINE AGENTSTATUSEX se envía cuando cambia el estado de un agente de ACD en un controlador de agente para el que la aplicación tiene actualmente \_ una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: LINE_AGENTSTATUSEX mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc622d1df7b9d86009822f9920cf9f510c68b71a28952a4146e98bdbe69e9da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405235"
---
# <a name="line_agentstatusex-message"></a>MENSAJE \_ LINE AGENTSTATUSEX

El **mensaje \_ LINE AGENTSTATUSEX** se envía cuando cambia el estado de un agente de ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la [**función lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

Identificador de la aplicación al dispositivo de línea. Esto está relacionado con el controlador del agente.

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

Especifica el estado de la cola que ha cambiado. Puede ser una o varias de las [**constantes LINEQUEUESTATUS \_**](linequeuestatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam2* incluye el bit LINEAGENTSTATUSEX STATE, dwParam3 indica el nuevo valor del estado del agente, que es una de las \_ [**constantes LINEAGENTSTATEEX \_**](lineagentstateex--constants.md). 

De lo contrario, *dwParam3* se establece en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




