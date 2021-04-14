---
title: atributo Message
description: El atributo \ Message \ indica que la llamada a procedimiento remoto se tratará como un mensaje desde el cliente al servidor.
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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487631"
---
# <a name="message-attribute"></a>atributo Message

El atributo **\[ Message \]** indica que la llamada a procedimiento remoto se tratará como un mensaje desde el cliente al servidor.

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Otros atributos que se aplican a la función. Solo **\[** [](local.md) **\]** **\[** se pueden usar los atributos local, [**nocode**](nocode.md) **\]** , **\[** [**code**](code.md)**\]** y **\[** [**Optimize**](optimize.md) **\]** con el atributo **\[ Message \]** .

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*opcional-Parameter-Attributes* 
</dt> <dd>

Cero o más atributos de MIDL que se aplicarán al parámetro.

</dd> <dt>

*param: nombre* 
</dt> <dd>

Nombre del parámetro tal y como se define en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Como mensajes del cliente, las llamadas a procedimientos remotos con el atributo **\[ Message \]** se entregan al servidor de forma asincrónica a través del transporte de cola de mensajes de [**ncadg \_ MQ**](ncadg-mq.md) . Puede indicar la mensajería de modo sincrónico especificando el protocolo de **transporte \_ MQ ncadg** sin usar el atributo **\[ Message \]** .

Al especificar la mensajería de modo asincrónico, el atributo de **\[ mensaje \]** permite al cliente realizar la llamada a procedimiento remoto y volver inmediatamente, incluso cuando la aplicación de servidor no responde. Si el servidor de destino no está disponible, la llamada se almacenará hasta que el servidor esté disponible.

Además, la mensajería de modo asincrónico le permite controlar las propiedades de la cola de mensajes de la cola de recepción del servidor. Vea [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) para obtener más información sobre cómo seleccionar la calidad de servicio, la prioridad de llamada y la duración de la llamada para el proceso de servidor.

Las restricciones siguientes también se aplican al atributo **\[ Message \]** :

-   Microsoft Message Queuing debe implementarse en los sistemas cliente y servidor, y los sistemas deben ser visibles entre sí según lo determinado por el ámbito de la instalación de la cola de mensajes.
-   El enlace debe usar puntos de conexión conocidos y el protocolo de transporte [**\_ MQ de ncadg**](ncadg-mq.md) .
-   La función no puede contener parámetros de salida ni un tipo de valor devuelto distinto de [**void**](void.md). Tenga en cuenta que la última restricción hace que el atributo de **\[ mensaje \]** no sea adecuado para los métodos de interfaz com (objeto), en este momento. La siguiente versión de MIDL permitirá que las funciones de **\[ mensaje \]** devuelvan el estado de error \_ \_ t o HRESULT.
-   Cualquier interfaz que contenga al menos una llamada de **\[ mensaje \]** se debe registrar llamando a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) antes de llamar a [**RpcServerUseProtseqEpEx (ncadg \_ MQ)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex). De lo contrario, las llamadas que estaban esperando en la cola del servidor se leerán antes de que se registre la interfaz y se producirá un error en las llamadas.

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

[**codifica**](code.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**ncadg \_ MQ**](ncadg-mq.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**optimiz**](optimize.md)
</dt> <dt>

[Message Queue Server de RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 