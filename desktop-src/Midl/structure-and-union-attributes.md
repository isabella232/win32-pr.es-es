---
title: Atributos de estructura y unión
description: Use el modificador \_ \ atributos para especificar la característica de una unión en una llamada a procedimiento remoto. Use el atributo ignore para designar determinados miembros de estructura o unión como locales para la aplicación cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, atributos, estructura y unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc179632bb7e0d64b777f3c8a08b9de2af7bbf818978d6bb0a7ee2ea8b515542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066675"
---
# <a name="structure-and-union-attributes"></a>Atributos de estructura y unión

Use los **atributos \_ switch** para especificar la característica de una unión en una llamada a procedimiento \* remoto. Use el [**atributo ignore**](ignore.md) para designar determinados miembros de estructura o unión como locales para la aplicación cliente.



| Atributo                           | Uso                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Interruptor**](switch.md)            | Selecciona el discriminador de una unión encapsulada.                                                                           |
| [**switch \_ es**](switch-is.md)     | Identifica el discriminador de una unión nocapsulada.                                                                      |
| [**tipo \_ de conmutador**](switch-type.md) | Identifica el tipo del discriminador para una unión nocapsulada.                                                          |
| [**Ignorar**](ignore.md)            | Designa que un puntero contenido en una estructura o unión y el objeto indicado por el puntero no se va a transmitir. |



 

También puede usar la matriz y [los atributos de puntero de tamaño](array-and-sized-pointer-attributes.md) para especificar las características de los miembros de estructura o unión.

 

 




