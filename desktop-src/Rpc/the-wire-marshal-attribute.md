---
title: El wire_marshal atributo
description: El atributo \ wire marshal\ es un atributo de tipo IDL similar en sintaxis a \ transmit as\, pero proporciona una manera más eficaz de serializar los datos \_ a través de una \_ red.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- Llamada a procedimiento remoto RPC, atributos, wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b54c923c59fd2146b5b1c3db898f6606a1a3d0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881182"
---
# <a name="the-wire_marshal-attribute"></a>Atributo de \_ serialización de conexión

El atributo wire marshal es un atributo de tipo IDL similar en sintaxis para transmitir como , pero que proporciona una manera más eficaz de serializar los datos a través de \[ [ \_ ](/windows/desktop/Midl/wire-marshal) \] una \[ [ \_ ](/windows/desktop/Midl/transmit-as) \] red.

Use el atributo wire marshal para especificar un tipo de datos que se transmitirá en lugar del tipo de datos específico \[ **\_** de \] la aplicación. Cada tipo específico de la aplicación tiene un tipo transmitible correspondiente que define la representación de conexión (la representación usada en la red). No es necesario transmitir el tipo específico de la aplicación, pero debe ser un tipo que MIDL reconozca. Para serializar un tipo desconocido para MIDL, use la serialización de usuario del atributo ACF \[ [ \_ ](/windows/desktop/Midl/user-marshal) \] .

El tipo específico de la aplicación puede ser un tipo simple, compuesto o de puntero. La restricción principal es que la instancia de tipo debe tener un tamaño de memoria fijo y bien definido. Si es necesario cambiar el tamaño de la instancia de tipo, use un campo de puntero en lugar de una matriz compatible. Como alternativa, puede definir un puntero al tipo modificable.

Debe proporcionar las rutinas para cambiar el tamaño, serializar y desmarque los datos, así como liberar la memoria asociada. En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el usuario. El &lt; tipo es el tipo &gt; userm especificado en la definición del tipo \[ **de \_ serialización** de \] conexión.



| Rutina                                                            | Descripción                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [&lt;tipo &gt; \_ UserSize](the-type-usersize-function.md)           | Tamaños del búfer de datos RPC antes de serializar en el lado cliente o servidor. |
| [&lt;tipo &gt; \_ UserMarshal](the-type-usermarshal-function.md)     | Serializa los datos en el lado cliente o servidor.                           |
| [&lt;tipo &gt; \_ UserUnmarshal](the-type-userunmarshal-function.md) | Desmarshals los datos en el lado cliente o servidor.                         |
| [&lt;tipo &gt; \_ UserFree](the-type-userfree-function.md)           | Libera los datos del lado servidor.                                        |



 

El cliente o la aplicación de servidor proporcionan estas rutinas proporcionadas por el programador en función de los atributos direccionales.

Si el parámetro solo \[ [está en](/windows/desktop/Midl/in) \] , el cliente transmite al servidor. El cliente necesita el **&lt; tipo &gt; \_ UserSize y** el tipo **&lt; &gt; \_ UserMarshal** functions. El servidor necesita el **&lt; tipo &gt; \_ UserUnmarshal y** las funciones **&lt; &gt; \_ UserFree.**

Para un \[ [parámetro](/windows/desktop/Midl/out-idl) \] de solo salida, el servidor transmite al cliente. El servidor necesita el **&lt; tipo &gt; \_ UserSize** y **&lt; las funciones &gt; \_ UserMarshal,** mientras que el cliente necesita el **&lt; tipo &gt; \_ Función UserMarshal.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributo de \_ serialización de usuario](the-user-marshal-attribute.md)
</dt> <dt>

[Reglas de serialización para la serialización \_ de usuario y la serialización de \_ conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[**GetGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 
