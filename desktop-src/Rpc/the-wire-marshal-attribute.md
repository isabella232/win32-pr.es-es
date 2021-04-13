---
title: El atributo wire_marshal
description: El atributo \ WIRE \_ Marshal \ es un atributo de tipo IDL similar en sintaxis a \ transmitir \_ como \, pero proporcionando una manera más eficaz de calcular las referencias de los datos a través de una red.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- RPC, atributos, wire_marshal llamada a procedimiento remoto
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421109"
---
# <a name="the-wire_marshal-attribute"></a>Atributo de \_ serialización de cable

El \[ atributo de [ \_ serialización de conexión](/windows/desktop/Midl/wire-marshal) \] es un atributo de tipo IDL similar en sintaxis para \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] , pero proporcionando una manera más eficaz de calcular las referencias de los datos a través de una red.

El atributo de \[ **\_ serialización** de la conexión se usa \] para especificar un tipo de datos que se transmitirá en lugar del tipo de datos específico de la aplicación. Cada tipo específico de la aplicación tiene un tipo de transmisión correspondiente que define la representación de la conexión (la representación usada en la red). No es necesario que el tipo específico de la aplicación sea transmitible, pero debe ser un tipo que MIDL reconozca. Para calcular las referencias de un tipo desconocido a MIDL, use el atributo ACF \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] .

El tipo específico de la aplicación puede ser un tipo simple, compuesto o de puntero. La restricción principal es que la instancia de tipo debe tener un tamaño de memoria fijo y bien definido. Si el tamaño de la instancia de tipo debe cambiar, use un campo de puntero en lugar de una matriz compatible. Como alternativa, puede definir un puntero al tipo modificable.

Debe proporcionar las rutinas para el ajuste de tamaño, la serialización y la serialización de los datos, así como la liberación de la memoria asociada. En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el usuario. <type>Es el tipo de userm especificado en la definición de tipo de \[ **\_ serialización de cable** \] .



| Rutina                                                            | Descripción                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_Usuarios](the-type-usersize-function.md)           | Ajusta el tamaño del búfer de datos RPC antes de calcular las referencias en el cliente o el servidor. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Calcula las referencias de los datos en el lado cliente o servidor.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Anula las referencias de los datos en el lado cliente o servidor.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Libera los datos en el lado del servidor.                                        |



 

Estas rutinas proporcionadas por el programador las proporciona el cliente o la aplicación de servidor en función de los atributos direccionales.

Si el parámetro es \[ solo [en](/windows/desktop/Midl/in) \] , el cliente se transmite al servidor. El cliente necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** . El servidor necesita las funciones **<type> \_ UserUnmarshal** y **<type> \_ UserFree** .

Para un \[ [](/windows/desktop/Midl/out-idl) \] parámetro de solo salida, el servidor se transmite al cliente. El servidor necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** , mientras que el cliente necesita la función **<type> \_ UserMarshal** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributo User \_ Marshal](the-user-marshal-attribute.md)
</dt> <dt>

[Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_serialización de cable](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_serialización de usuario](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 