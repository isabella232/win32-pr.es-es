---
title: difundir atributo
description: La palabra clave \ Broadcast \ especifica que las llamadas a procedimientos remotos se envíen a todos los servidores de una red local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- difundir atributo MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358211"
---
# <a name="broadcast-attribute"></a>difundir atributo

La palabra clave **\[ Broadcast \]** especifica que las llamadas a procedimientos remotos se envían a todos los servidores de una red local.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto. Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica los atributos adicionales que se van a aplicar a la función. Separe varios atributos con comas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo de **\[ difusión \]** .

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La palabra clave **\[ Broadcast \]** especifica que la rutina siempre se difunde a todos los servidores de la red, en lugar de entregarse a un servidor determinado. El cliente recibe la salida de la primera respuesta para que se devuelva correctamente, mientras que las respuestas subsiguientes se descartan.

Una operación con el atributo **\[ Broadcast \]** es implícitamente una operación [**\[ idempotente \]**](idempotent.md) . Sin embargo, el atributo **\[ Broadcast \]** especifica propiedades adicionales que funcionan con el atributo **\[ idempotente \]** . En concreto, las funciones que usan el atributo **\[ Broadcast \]** especifican que se puede llamar varias veces a la rutina como resultado de una llamada a procedimiento remoto. Al mismo tiempo, se pueden enviar a varios servidores. Esto es diferente del atributo **\[ idempotente \]** , que especifica solo que se puede reintentar una llamada si no se completa.

Si un procedimiento remoto difunde su llamada a todos los hosts de una red local, debe usar la secuencia de protocolo [**\_ \_ UDP de ncadg**](ncadg-ip-udp.md) o [**ncadg \_**](ncadg-ipx.md) IP. Tenga en cuenta que el servicio de datagramas determina el tamaño de un paquete de **\[ difusión \]** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**incluso**](maybe.md)
</dt> <dt>

[**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> </dl>

 

 




