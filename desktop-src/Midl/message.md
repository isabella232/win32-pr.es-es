---
title: atributo message
description: El atributo \ message\ indica que la llamada a procedimiento remoto se va a tratar como un mensaje del cliente al servidor.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- atributo de mensaje MIDL
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159498"
---
# <a name="message-attribute"></a>atributo message

El **\[ atributo \]** message indica que la llamada a procedimiento remoto se va a tratar como un mensaje del cliente al servidor.

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*optional-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la función. Solo se pueden usar los atributos **\[** [](local.md) **\]** locales , **\[** [**nocode**](nocode.md), code y **\]** **\[** [](code.md)**\]** **\[** [**optimize**](optimize.md) **\]** con el atributo **\[ message. \]**

</dd> <dt>

*function-name* 
</dt> <dd>

Nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*optional-parameter-attributes* 
</dt> <dd>

Cero o más atributos MIDL que se aplicarán al parámetro .

</dd> <dt>

*param-name* 
</dt> <dd>

Nombre del parámetro tal como se define en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Como mensajes del cliente, las llamadas a procedimiento remoto con el atributo **\[ message \]** se entregan al servidor de forma asincrónica a través del transporte [**de ncadg \_ mq**](ncadg-mq.md) message-queuing. Puede indicar la mensajería en modo sincrónico especificando el protocolo de transporte **ncadg \_ mq** sin usar el **\[ atributo message. \]**

Al especificar la mensajería en modo asincrónico, el atributo **\[ message \]** permite al cliente realizar la llamada a procedimiento remoto y volver inmediatamente, incluso cuando la aplicación de servidor no responde. Si el servidor de destino no está disponible, la llamada se almacenará hasta que el servidor esté disponible.

Además, la mensajería en modo asincrónico permite controlar las propiedades de cola de mensajes de la cola de recepción para el servidor. Vea [**RpcBindingSetOption para**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) obtener más información sobre cómo seleccionar la calidad del servicio, la prioridad de llamada y la duración de las llamadas para el proceso del servidor.

Las restricciones siguientes también se aplican al atributo **\[ de \]** mensaje:

-   Microsoft Message Queuing deben implementarse en los sistemas cliente y servidor y los sistemas deben ser visibles entre sí según lo determinado por el ámbito de la instalación de la cola de mensajes.
-   El enlace debe usar puntos de conexión conocidos y el [**protocolo de transporte ncadg \_ mq.**](ncadg-mq.md)
-   La función no puede contener parámetros de salida o un tipo de valor devuelto distinto de [**void.**](void.md) Tenga en cuenta que esta última restricción hace que el atributo **\[ de \]** mensaje no sea adecuado para los métodos de interfaz COM (objeto), en este momento. La próxima versión de MIDL permitirá que las **\[ funciones de \]** mensaje devuelvan el estado de error t o \_ \_ HRESULT.
-   Cualquier interfaz que contenga al menos una llamada de mensaje debe registrarse llamando **a \[ \]** [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) antes de llamar a [**RpcServerUseProtseqEpEx(ncadg \_ mq).**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex) De lo contrario, las llamadas que estaban esperando en la cola para el servidor se leerán antes de que se registre la interfaz y se producirá un error en las llamadas.

## <a name="examples"></a>Ejemplos

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Código**](code.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**ncadg \_ mq**](ncadg-mq.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Optimizar**](optimize.md)
</dt> <dt>

[RPC Message Queuing](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 