---
title: Propiedad DefaultAction
description: La propiedad DefaultAction de un objeto describe el método principal de manipulación del objeto desde el punto de vista del usuario. La propiedad DefaultAction de un objeto debe ser un verbo o una frase de verbo corto.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd5aa70e0c6c633aa5b0ca3fe5c40049dbeb8cf2496c7785eea513821e1d5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325759"
---
# <a name="defaultaction-property"></a>Propiedad DefaultAction

La propiedad **DefaultAction de** un objeto describe el método principal de manipulación del objeto desde el punto de vista del usuario. La propiedad **DefaultAction de un** objeto debe ser un verbo o una frase de verbo corto.

La **propiedad DefaultAction** se recupera mediante una llamada a [**IAccessible::get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).

Para realizar la acción predeterminada de un objeto, los clientes llaman [**a IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).

No todos los objetos tienen acciones predeterminadas y algunos objetos tienen una acción predeterminada que está relacionada con su [**propiedad Value,**](value-property.md) como en los ejemplos siguientes:

-   Una casilla seleccionada tiene una acción predeterminada de "Uncheck" y un valor de "Checked".
-   Una casilla desactivada tiene una acción predeterminada de "Check" y un valor de "Unchecked".
-   Un botón con la etiqueta "Imprimir" tiene una acción predeterminada de "Press", sin ningún valor.
-   Un control de texto estático o un control de edición que muestra "Printer" no tiene ninguna acción predeterminada, pero tiene el valor "Printer".

 

 




