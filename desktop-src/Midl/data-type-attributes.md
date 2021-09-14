---
title: Atributos de tipo de datos
description: Puede aplicar estos atributos a los tipos de datos en una instrucción typedef para definir aún más el uso o el efecto del tipo de datos.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL, atributos, tipo de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159634"
---
# <a name="data-type-attributes"></a>Atributos de tipo de datos

Puede aplicar estos atributos a los tipos de datos en una [**instrucción typedef**](typedef.md) para definir aún más el uso o el efecto del tipo de datos.



| Atributo                                 | Uso                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**identificador de \_ contexto**](context-handle.md) | Identifica un identificador de enlace que mantiene información de estado (contexto) en un servidor determinado entre llamadas a procedimientos remotos desde un cliente determinado. No es válido para las [**funciones de interfaz**](object.md) de objeto.                                                                                                         |
| [**handle**](handle.md)                  | Especifica un tipo de identificador personalizado específico de la aplicación.                                                                                                                                                                                                                                                                |
| [**ms \_ union**](-ms-union.md)            | Controla la alineación BAND de las uniones nocapsuladas. Use en [**definiciones de**](typedef.md)tipo para la compatibilidad con versiones anteriores con interfaces creadas con MIDL 1.0 o 2.0.                                                                                                                                                            |
| [**Pipa**](pipe.md)                      | Permite la transmisión de un flujo de datos con tipo abierto a través de una llamada a procedimiento remoto. Un [**parámetro in**](in.md) pipe permite al servidor extraer el flujo de datos del cliente durante una llamada a procedimiento remoto. Un [**parámetro de**](-out.md) canalización de salida permite que el servidor vuelva a insertar el flujo de datos en el cliente. |
| [**transmitir \_ como**](transmit-as.md)       | Especifica cómo se transmitirá un tipo de datos a través de una red, que se usa para la serialización personalizada.                                                                                                                                                                                                                                  |
| [**Enumeración \_ v1**](v1-enum.md)               | Indica que el tipo enumerado especificado se transmita como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.                                                                                                                                                                                                              |
| [**wire \_ marshal**](wire-marshal.md)     | Es similar [**a \_ transmitir como,**](transmit-as.md) pero se implementan las rutinas para cambiar el tamaño, serializar, desmarshal y liberar los datos.                                                                                                                                                                                              |



 

 

 




