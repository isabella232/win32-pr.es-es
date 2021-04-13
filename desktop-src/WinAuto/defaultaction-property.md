---
title: Propiedad DefaultAction
description: La propiedad DefaultAction de un objeto describe el método principal de manipulación del objeto desde el punto de vista del usuario. La propiedad DefaultAction de un objeto debe ser un verbo o una frase de verbo corta.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356815"
---
# <a name="defaultaction-property"></a>Propiedad DefaultAction

La propiedad **DEFAULTACTION** de un objeto describe el método principal de manipulación del objeto desde el punto de vista del usuario. La propiedad **DEFAULTACTION** de un objeto debe ser un verbo o una frase de verbo corta.

La propiedad **DEFAULTACTION** se recupera llamando a [**IAccessible:: get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).

Para realizar la acción predeterminada de un objeto, los clientes llaman a [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).

No todos los objetos tienen acciones predeterminadas y algunos objetos tienen una acción predeterminada relacionada con su propiedad [**Value**](value-property.md) , como en los ejemplos siguientes:

-   Una casilla seleccionada tiene una acción predeterminada de "desactivar" y un valor de "activado".
-   Una casilla desactivada tiene una acción predeterminada de "comprobar" y un valor de "desactivada".
-   Un botón con la etiqueta "Imprimir" tiene una acción predeterminada de "presionar", sin ningún valor.
-   Un control de texto estático o un control de edición que muestra "Printer" no tiene ninguna acción predeterminada, pero tiene un valor de "Printer".

 

 




