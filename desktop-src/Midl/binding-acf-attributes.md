---
title: Enlazar atributos ACF
description: Especifique cómo se conecta el cliente al servidor para las llamadas a procedimiento remoto con los atributos enumerados en la tabla siguiente.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- MIDL de ACF, atributos, enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32b4d53cea81ed2a69a702a1a58942834a538ffbef75cb11315dd792882bf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385231"
---
# <a name="binding-acf-attributes"></a>Enlazar atributos ACF

Especifique cómo se conecta el cliente al servidor para las llamadas a procedimiento remoto con los atributos enumerados en la tabla siguiente.



| Atributo                                                          | Uso                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)                                             | Define un identificador que permite al autor de la llamada realizar una llamada asincrónica y volver inmediatamente sin esperar los resultados y, a continuación, volver a sincronizar con la función llamada para recibir datos una vez completada la llamada. |
| [**identificador \_ automático**](auto-handle.md)                                | Indica a MIDL que permita que el código auxiliar controle el enlace automáticamente. Este es el valor predeterminado si no se especifica ningún identificador de enlace.                                                                                    |
| [**context \_ handle \_ noserialize**](context-handle-noserialize.md) | Garantiza que un identificador de contexto nunca se serializará, independientemente del comportamiento predeterminado de la aplicación.                                                                                                       |
| [**serialización \_ del \_ identificador de contexto**](context-handle-serialize.md)     | Garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.                                                                                                       |
| [**identificador \_ explícito**](explicit-handle.md)                        | Permite que la aplicación cliente controle el enlace con un parámetro explícito en cada procedimiento.                                                                                                                      |
| [**identificador \_ implícito**](implicit-handle.md)                        | Especifica un identificador para los procedimientos que no tienen un parámetro de identificador explícito. La aplicación cliente todavía controla el enlace.                                                                                |
| [**control \_ de contexto \_ estricto**](strict-context-handle.md)           | Garantiza que los métodos de la interfaz solo acepten identificadores de contexto creados por un método de esa interfaz.                                                                                     |



 

 

 




