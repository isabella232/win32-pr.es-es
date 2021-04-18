---
title: El atributo user_marshal
description: El atributo \ User \_ Marshal \ es un atributo de tipo ACF similar en sintaxis a \ representarse \_ como \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC, atributos, user_marshal llamada a procedimiento remoto
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488066"
---
# <a name="the-user_marshal-attribute"></a>Atributo User \_ Marshal

El \[ atributo [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] es un atributo de tipo ACF similar en sintaxis para \[ [representar \_ como](/windows/desktop/Midl/represent-as) \] . Al igual que con el atributo IDL, las \[ [ \_ referencias de cable](/windows/desktop/Midl/wire-marshal) \] ofrecen una manera más eficaz de calcular las referencias de los datos a través de una red. Como atributo ACF, el **\[ \_ cálculo de \] referencias de usuario** permite calcular las referencias de tipos de datos personalizados que son desconocidos para MIDL. Cada tipo específico de la aplicación tiene un tipo de transmisión correspondiente que define la representación de la conexión.

El tipo específico de la aplicación puede ser un tipo simple, compuesto o de puntero. La restricción principal es que la instancia de tipo debe tener un tamaño de memoria fijo y bien definido. Si el tamaño de la instancia de tipo debe cambiar, use un campo de puntero en lugar de una matriz compatible. Como alternativa, puede definir un puntero al tipo modificable.

Al igual que con el atributo de **\[ \_ serialización \] de conexión** , se proporcionan rutinas para el ajuste de tamaño, el cálculo de referencias, la unserialización y la liberación. En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el usuario. <type>Es el *tipo* de userm especificado en la definición del tipo de **\[ cálculo de \_ referencias \] del usuario** .



| Rutina                                                            | Descripción                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_Usuarios](the-type-usersize-function.md)           | Ajusta el tamaño del búfer de datos RPC antes de calcular las referencias en el cliente o el servidor. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Calcula las referencias de los datos en el lado cliente o servidor.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Anula las referencias de los datos en el lado cliente o servidor.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Libera los datos en el lado del servidor.                                        |



 

Estas rutinas proporcionadas por el usuario las proporciona el cliente o la aplicación de servidor, en función de los atributos direccionales.

Si el parámetro es \[ solo [en](/windows/desktop/Midl/in) \] , el cliente se transmite al servidor. El cliente necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** . El servidor necesita las funciones **<type> \_ UserUnmarshal** y **<type> \_ UserFree** .

Para un \[ [](/windows/desktop/Midl/out-idl) \] parámetro de solo salida, el servidor se transmite al cliente. El servidor necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** , mientras que el cliente necesita la función **<type> \_ UserMarshal** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributo de \_ serialización de cable](the-wire-marshal-attribute.md)
</dt> <dt>

[Serialización de reglas para serialización de usuario y \_ serialización de conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_serialización de usuario](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[\_serialización de cable](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 