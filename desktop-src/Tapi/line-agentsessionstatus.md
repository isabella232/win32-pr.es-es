---
description: El mensaje LINE AGENTSESSIONSTATUS se envía cuando cambia el estado de una sesión de agente de ACD en un controlador de agente para el que la aplicación tiene actualmente \_ una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: LINE_AGENTSESSIONSTATUS mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25209abda7cfec3864c45bfd58a35a9fad21a1aa5e5645669a7fdad6ec907d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003223"
---
# <a name="line_agentsessionstatus-message"></a>Mensaje \_ DE LINE AGENTSESSIONSTATUS

El **mensaje LINE \_ AGENTSESSIONSTATUS** se envía cuando cambia el estado de una sesión de agente de ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la [**función lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

El identificador de la aplicación al dispositivo de línea en el que ha cambiado el estado de sesión del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de la sesión del agente cuyo estado ha cambiado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado de sesión del agente que ha cambiado. Puede ser uno o varios de **los line \_ AGENTSESSIONSTATUS.**

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

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




