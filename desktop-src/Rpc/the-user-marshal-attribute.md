---
title: El user_marshal atributo
description: El atributo \user marshal\ es un atributo de tipo ACF similar en \_ sintaxis a \ represent \_ as\.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Llamada a procedimiento remoto RPC, atributos, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0501cfd3199d41a49da7f54919c86f9332ce976f33963f23c63a7938338da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923535"
---
# <a name="the-user_marshal-attribute"></a>Atributo de \_ serialización de usuario

El \[ [atributo de \_ serialización](/windows/desktop/Midl/user-marshal) \] de usuario es un atributo de tipo ACF similar en sintaxis para \[ [representar \_ como](/windows/desktop/Midl/represent-as) \] . Al igual que con el atributo IDL, wire marshal , ofrece una manera más eficaz de serializar los datos a través de una \[ [ \_ ](/windows/desktop/Midl/wire-marshal) \] red. Como atributo ACF, la serialización **\[ de \_ usuario \]** le permite serializar tipos de datos personalizados desconocidos para MIDL. Cada tipo específico de la aplicación tiene un tipo transmitible correspondiente que define la representación de conexión.

El tipo específico de la aplicación puede ser un tipo simple, compuesto o de puntero. La restricción principal es que la instancia de tipo debe tener un tamaño de memoria fijo y bien definido. Si es necesario cambiar el tamaño de la instancia de tipo, use un campo de puntero en lugar de una matriz compatible. Como alternativa, puede definir un puntero al tipo modificable.

Al igual que con el atributo **\[ \_ wire marshal, \]** se suministran rutinas para los pases de tamaño, serialización, desmarque y liberar. En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el usuario. es <type> el tipo userm-*especificado* en la **\[ definición del tipo \_ de \] serialización** de usuario.



| Rutina                                                            | Descripción                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_UserSize](the-type-usersize-function.md)           | Tamaños del búfer de datos RPC antes de serializar en el lado cliente o servidor. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Serializa los datos en el lado cliente o servidor.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Desmarshals los datos en el lado cliente o servidor.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Libera los datos del lado servidor.                                        |



 

El cliente o la aplicación de servidor proporcionan estas rutinas proporcionadas por el usuario, en función de los atributos direccionales.

Si el parámetro está \[ [solo en](/windows/desktop/Midl/in) \] , el cliente transmite al servidor. El cliente necesita las **<type> \_ funciones UserSize** **<type> \_ y UserMarshal.** El servidor necesita las **<type> \_ funciones UserUnmarshal** **<type> \_ y UserFree.**

Para un \[ [parámetro](/windows/desktop/Midl/out-idl) \] out -only, el servidor transmite al cliente. El servidor necesita las **<type> \_ funciones UserSize** y **<type> \_ UserMarshal,** mientras que el cliente necesita la **<type> \_ función UserMarshal.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributo de \_ la serialización de conexión](the-wire-marshal-attribute.md)
</dt> <dt>

[Reglas de serialización para la serialización de usuarios y la serialización \_ de conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**GetGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 