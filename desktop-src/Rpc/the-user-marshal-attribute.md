---
title: El user_marshal atributo
description: El atributo \user marshal\ es un atributo de tipo ACF similar en \_ sintaxis a \ represent \_ as\.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Llamada a procedimiento remoto RPC, atributos, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769e6a7e176d5aeba68afd322cdd6f24d76c6b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883749"
---
# <a name="the-user_marshal-attribute"></a>Atributo de \_ serialización de usuario

El \[ [atributo de \_ serialización](/windows/desktop/Midl/user-marshal) \] de usuario es un atributo de tipo ACF similar en sintaxis para \[ [representar \_ como](/windows/desktop/Midl/represent-as) \] . Al igual que con el atributo IDL, wire marshal , ofrece una manera más eficaz de serializar los datos a través de una \[ [ \_ ](/windows/desktop/Midl/wire-marshal) \] red. Como atributo ACF, las **\[ referencias de \_ \]** usuario le permiten serializar tipos de datos personalizados desconocidos para MIDL. Cada tipo específico de la aplicación tiene un tipo transmitible correspondiente que define la representación de la conexión.

El tipo específico de la aplicación puede ser un tipo simple, compuesto o de puntero. La restricción principal es que la instancia de tipo debe tener un tamaño de memoria fijo y bien definido. Si es necesario cambiar el tamaño de la instancia de tipo, use un campo de puntero en lugar de una matriz compatible. Como alternativa, puede definir un puntero al tipo modificable.

Al igual que con el atributo **\[ \_ wire marshal, \]** se suministran rutinas para los pases de tamaño, serialización, desmarque y liberación. En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el usuario. El &lt; tipo es el tipo &gt; userm-*especificado* en la **\[ definición del tipo \_ de serialización \]** de usuario.



| Rutina                                                            | Descripción                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [&lt;tipo &gt; \_ UserSize](the-type-usersize-function.md)           | Tamaños del búfer de datos RPC antes de serializar en el lado cliente o servidor. |
| [&lt;tipo &gt; \_ UserMarshal](the-type-usermarshal-function.md)     | Serializa los datos en el lado cliente o servidor.                           |
| [&lt;tipo &gt; \_ UserUnmarshal](the-type-userunmarshal-function.md) | Desmarshals los datos en el lado cliente o servidor.                         |
| [&lt;tipo &gt; \_ UserFree](the-type-userfree-function.md)           | Libera los datos del lado servidor.                                        |



 

El cliente o la aplicación de servidor proporcionan estas rutinas proporcionadas por el usuario, en función de los atributos direccionales.

Si el parámetro solo \[ [está en](/windows/desktop/Midl/in) \] , el cliente transmite al servidor. El cliente necesita el **&lt; tipo &gt; \_ UserSize y** el tipo **&lt; &gt; \_ UserMarshal** functions. El servidor necesita el **&lt; tipo &gt; \_ UserUnmarshal y** el tipo Funciones **&lt; &gt; \_ UserFree.**

Para un \[ [parámetro](/windows/desktop/Midl/out-idl) \] de solo salida, el servidor transmite al cliente. El servidor necesita el **&lt; tipo &gt; \_ UserSize** y **&lt; las funciones &gt; \_ UserMarshal,** mientras que el cliente necesita el **&lt; tipo &gt; \_ Función UserMarshal.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributo de \_ serialización de conexión](the-wire-marshal-attribute.md)
</dt> <dt>

[Reglas de serialización para la serialización de usuario y la serialización \_ de conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**GetGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 
