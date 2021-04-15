---
title: Atributos de estructura y de Unión
description: Use los \_ atributos switch \ para especificar la característica de una Unión en una llamada a procedimiento remoto. Utilice el atributo Ignore para designar determinados miembros de estructura o Unión como locales para la aplicación cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- MIDL, atributos, estructura y Unión IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486734"
---
# <a name="structure-and-union-attributes"></a>Atributos de estructura y de Unión

Utilice los **atributos \_ Switch** \* para especificar la característica de una Unión en una llamada a procedimiento remoto. Utilice el atributo [**Ignore**](ignore.md) para designar determinados miembros de estructura o Unión como locales para la aplicación cliente.



| Atributo                           | Uso                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**switch**](switch.md)            | Selecciona el discriminante de una Unión encapsulada.                                                                           |
| [**el modificador \_ es**](switch-is.md)     | Identifica discriminante para una Unión no encapsulada.                                                                      |
| [**tipo de conmutador \_**](switch-type.md) | Identifica el tipo de discriminante para una Unión no encapsulada.                                                          |
| [**omitir**](ignore.md)            | Designa que un puntero contenido en una estructura o Unión y el objeto indicado por el puntero no se va a transmitir. |



 

También puede usar los [atributos de puntero de matriz y tamaño](array-and-sized-pointer-attributes.md) para especificar características de miembros de estructura o Unión.

 

 




