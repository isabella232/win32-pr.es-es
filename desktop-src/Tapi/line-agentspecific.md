---
description: El \_ mensaje AGENTSPECIFIC de línea de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar lineGetAgentStatus para determinar el estado actual del agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Mensaje de LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680779"
---
# <a name="line_agentspecific-message"></a>Mensaje de línea \_ AGENTSPECIFIC

El mensaje **\_ AGENTSPECIFIC de línea** de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar el estado actual del agente.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la aplicación para el dispositivo de línea.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Índice en la matriz de identificadores de extensión de controlador en la estructura [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) de la extensión de controlador a la que está asociado el mensaje.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico de la extensión de controlador. Normalmente, este valor se usa para hacer que la aplicación invoque una función [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) para capturar más detalles sobre el mensaje.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico de la extensión de controlador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje **line \_ AGENTSPECIFIC** no se envía a las aplicaciones que admiten versiones anteriores de TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




