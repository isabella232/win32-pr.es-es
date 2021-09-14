---
title: ncadg_mq atributo
description: La palabra clave ncadg \_ mq identifica Microsoft Message Queuing Services (MSMQ) como el protocolo de transporte para el punto de conexión. Este protocolo está obsoleto y no debe usarse en nuevas aplicaciones.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159458"
---
# <a name="ncadg_mq-attribute"></a>Atributo mq de ncadg \_

La **palabra clave ncadg \_ mq** identifica Microsoft Message Queuing Services (MSMQ) como el protocolo de transporte para el punto de conexión. Este protocolo está obsoleto y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica el nombre del servidor o host del equipo. El nombre es una cadena de caracteres y puede ser un nombre de dominio completo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar el protocolo de transporte **ncadg \_ mq,** los componentes de MSMQ deben estar completamente instalados y los sistemas cliente y servidor deben ser accesibles a través de los protocolos MQ.

El **protocolo ncadg \_ mq** no admite puntos de conexión dinámicos ni [**llamadas de difusión.**](broadcast.md) Al igual que con otros protocolos de **datagrama, ncadg \_ mq** no admite devoluciones de llamada; cualquier función que use el atributo [**de**](callback.md) devolución de llamada producirá un error.

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

## <a name="examples"></a>Ejemplos

La sintaxis del protocolo message-queue se define independientemente de la especificación de IDL. El compilador MIDL realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de durante la compilación.

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Difusión**](broadcast.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Mensaje**](message.md)
</dt> <dt>

[RPC Message Queuing](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[Enlace de cadena](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 