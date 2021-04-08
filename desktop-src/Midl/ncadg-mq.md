---
title: ncadg_mq atributo)
description: La \_ palabra clave ncadg MQ identifica Microsoft Message Queuing Services (MSMQ) como protocolo de transporte para el extremo. Este protocolo está obsoleto y no debe usarse en aplicaciones nuevas.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq el atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995171"
---
# <a name="ncadg_mq-attribute"></a>\_atributo MQ ncadg

La palabra clave **ncadg \_ mq** identifica Microsoft Message QUEUING Services (MSMQ) como protocolo de transporte para el extremo. Este protocolo está obsoleto y no debe usarse en aplicaciones nuevas.

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del servidor* 
</dt> <dd>

Especifica el nombre del servidor, o host, del equipo. El nombre es una cadena de caracteres y puede ser un nombre de dominio completo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar el protocolo de **transporte \_ MQ de ncadg** , los componentes de MSMQ deben estar completamente instalados y los sistemas de servidor y cliente deben ser accesibles a través de los protocolos MQ.

El **Protocolo \_ MQ ncadg** no admite puntos de conexión dinámicos ni llamadas de [**difusión**](broadcast.md) . Al igual que con otros protocolos de datagrama, **ncadg \_ MQ** no admite las devoluciones de llamada; se producirá un error en todas las funciones que utilicen el atributo [**callback**](callback.md) .

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

## <a name="examples"></a>Ejemplos

La sintaxis del protocolo Message-Queue se define independientemente de la especificación IDL. El compilador MIDL realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del extremo sea correcta. Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de durante la compilación.

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

[**amplia**](broadcast.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Mensaje**](message.md)
</dt> <dt>

[Message Queue Server de RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[Enlace de cadenas](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 