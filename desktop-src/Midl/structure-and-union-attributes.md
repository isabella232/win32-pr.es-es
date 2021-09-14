---
title: Estructura y atributos de unión
description: Use el modificador \_ \ atributos para especificar la característica de una unión en una llamada a procedimiento remoto. Use el atributo ignore para designar determinados miembros de estructura o unión como locales para la aplicación cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, atributos, estructura y unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159370"
---
# <a name="structure-and-union-attributes"></a>Estructura y atributos de unión

Use los **atributos \_ switch** para especificar la característica de una unión en una llamada a procedimiento \* remoto. Use el [**atributo ignore**](ignore.md) para designar determinados miembros de estructura o unión como locales para la aplicación cliente.



| Atributo                           | Uso                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Interruptor**](switch.md)            | Selecciona el discriminador de una unión encapsulada.                                                                           |
| [**switch \_ es**](switch-is.md)     | Identifica el discriminador de una unión nocapsulada.                                                                      |
| [**tipo \_ de conmutador**](switch-type.md) | Identifica el tipo del discriminador para una unión nocapsulada.                                                          |
| [**Ignorar**](ignore.md)            | Designa que un puntero contenido en una estructura o unión y el objeto indicado por el puntero no se va a transmitir. |



 

También puede usar la matriz y [los atributos de puntero de tamaño](array-and-sized-pointer-attributes.md) para especificar las características de los miembros de estructura o unión.

 

 




