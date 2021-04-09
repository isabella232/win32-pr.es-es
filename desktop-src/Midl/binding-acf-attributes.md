---
title: Atributos ACF de enlace
description: Especifique cómo el cliente se conecta al servidor para las llamadas a procedimientos remotos con los atributos que se muestran en la tabla siguiente.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF (MIDL), atributos, enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076120"
---
# <a name="binding-acf-attributes"></a>Atributos ACF de enlace

Especifique cómo el cliente se conecta al servidor para las llamadas a procedimientos remotos con los atributos que se muestran en la tabla siguiente.



| Atributo                                                          | Uso                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)                                             | Define un identificador que permite al llamador realizar una llamada asincrónica y devolver inmediatamente sin esperar los resultados y, a continuación, volver a sincronizar con la función llamada para recibir los datos después de que se complete la llamada. |
| [**\_identificador automático**](auto-handle.md)                                | Indica a MIDL que permita que el código auxiliar Controle automáticamente el enlace. Este es el valor predeterminado si no se especifica ningún controlador de enlace.                                                                                    |
| [**identificador de contexto de \_ \_ noserialización**](context-handle-noserialize.md) | Garantiza que nunca se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.                                                                                                       |
| [**\_serializar identificador de contexto \_**](context-handle-serialize.md)     | Garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.                                                                                                       |
| [**\_identificador explícito**](explicit-handle.md)                        | Permite que la aplicación cliente controle el enlace con un parámetro explícito en cada procedimiento.                                                                                                                      |
| [**\_identificador implícito**](implicit-handle.md)                        | Especifica un identificador para los procedimientos que no tienen un parámetro de identificador explícito. La aplicación cliente sigue controlando el enlace.                                                                                |
| [**\_identificador de contexto estricto \_**](strict-context-handle.md)           | Garantiza que los métodos de la interfaz solo aceptarán los identificadores de contexto creados por un método de la interfaz.                                                                                     |



 

 

 




