---
title: Atributos de tipo de datos
description: Puede aplicar estos atributos a los tipos de datos de una instrucción TypeDef para definir más detalladamente el uso o el efecto del tipo de datos.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- MIDL, atributos, tipo de datos de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779903"
---
# <a name="data-type-attributes"></a>Atributos de tipo de datos

Puede aplicar estos atributos a los tipos de datos de una instrucción [**typedef**](typedef.md) para definir más detalladamente el uso o el efecto del tipo de datos.



| Atributo                                 | Uso                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**identificador de contexto \_**](context-handle.md) | Identifica un identificador de enlace que mantiene la información de estado (contexto) en un servidor determinado entre las llamadas a procedimientos remotos de un cliente determinado. No es válido para las funciones de la interfaz de [**objeto**](object.md) .                                                                                                         |
| [**asa**](handle.md)                  | Especifica un tipo de identificador personalizado específico de la aplicación.                                                                                                                                                                                                                                                                |
| [**Unión de MS \_**](-ms-union.md)            | Controla la alineación del NDR de las uniones no encapsuladas. Use en [**typedef**](typedef.md)s para mantener la compatibilidad con las interfaces compiladas con MIDL 1,0 o 2,0.                                                                                                                                                            |
| [**codo**](pipe.md)                      | Permite la transmisión de un flujo abierto de datos con tipo a través de una llamada a procedimiento remoto. Un parámetro [**in**](in.md) Pipe permite al servidor extraer el flujo de datos del cliente durante una llamada a procedimiento remoto. Un parámetro [**out**](-out.md) Pipe permite que el servidor devuelva la secuencia de datos al cliente. |
| [**transmitir \_ como**](transmit-as.md)       | Especifica cómo se transmitirá un tipo de datos a través de una red, que se utiliza para la serialización personalizada.                                                                                                                                                                                                                                  |
| [**\_enumeración v1**](v1-enum.md)               | Indica que el tipo enumerado especificado se va a transmitir como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.                                                                                                                                                                                                              |
| [**\_serialización de cable**](wire-marshal.md)     | Similar a [**transmitir \_ como**](transmit-as.md) , pero se implementan las rutinas para ajustar el tamaño, las referencias, las referencias y la liberación de los datos.                                                                                                                                                                                              |



 

 

 




