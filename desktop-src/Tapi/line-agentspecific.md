---
description: El mensaje TAPI LINE AGENTSPECIFIC se envía cuando cambia el estado de un agente de ACD en una línea que la aplicación \_ tiene abierta actualmente. La aplicación puede invocar lineGetAgentStatus para determinar el estado actual del agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: LINE_AGENTSPECIFIC mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87b0e6f5c6c96842f70ebe46c0b72e33e6767c996fa2cc5b4d8e95ff0f08cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867165"
---
# <a name="line_agentspecific-message"></a>LINE \_ AGENTSPECIFIC message

El mensaje TAPI **LINE \_ AGENTSPECIFIC** se envía cuando cambia el estado de un agente de ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar el estado actual del agente.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la aplicación al dispositivo de línea.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Índice de la matriz de identificadores de extensión de controlador en la [**estructura LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) de la extensión de controlador a la que está asociado el mensaje.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico de la extensión de controlador. Por lo general, este valor se usa para hacer que la aplicación invoque una función [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) para capturar más detalles sobre el mensaje.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico de la extensión de controlador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ LINE AGENTSPECIFIC** no se envía a las aplicaciones que admiten versiones anteriores de TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




