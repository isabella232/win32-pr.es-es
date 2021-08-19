---
title: atributo broadcast
description: La palabra clave \ broadcast\ especifica que las llamadas a procedimiento remoto se envíen a todos los servidores de una red local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- atributo de difusión MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f176b03f9d33ee1bbe1d0e805dfc109de477b7499f8fd624ba7732709dc61a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385241"
---
# <a name="broadcast-attribute"></a>atributo broadcast

La **\[ difusión de \] palabras** clave especifica que las llamadas a procedimiento remoto se envíen a todos los servidores de una red local.

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

*interface-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en su conjunto. Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica atributos adicionales que se aplicarán a la función. Separe varios atributos con comas.

</dd> <dt>

*returntype* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ de \]** difusión.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\[ palabra clave broadcast \]** especifica que la rutina siempre se difunde a todos los servidores de la red, en lugar de entregarse a un servidor determinado. El cliente recibe la salida de la primera respuesta para devolver correctamente, mientras que las respuestas posteriores se descartan.

Una operación con el **\[ atributo broadcast \]** es implícitamente una operación [**\[ idempotente. \]**](idempotent.md) Sin embargo, **\[ el atributo broadcast \]** especifica propiedades adicionales que las funciones con el atributo **\[ idempotente \]** no tienen. En concreto, las funciones que usan el atributo **\[ broadcast \]** especifican que se puede llamar a la rutina varias veces como resultado de una llamada a procedimiento remoto. Al mismo tiempo, se pueden enviar a varios servidores. Esto es diferente del **\[ atributo \] idempotente,** que especifica solo que se puede reintente una llamada si no se completa.

Si un procedimiento remoto difunde su llamada a todos los hosts de una red local, debe usar la secuencia de protocolo [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md) o [**\_ ncadg ipx.**](ncadg-ipx.md) Tenga en cuenta que el tamaño de un **\[ paquete de difusión \]** viene determinado por el servicio de datagramas en uso.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**quizás**](maybe.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> </dl>

 

 




