---
title: Propiedad Value
description: La propiedad Value proporciona una representación textual de la información visual contenida en un objeto . No todos los objetos admiten la propiedad Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcebf689016add11008b5d8249ce4eaa8adf4a99a406afea8d1267f01f94201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133278"
---
# <a name="value-property"></a>Propiedad Value

La **propiedad Value** proporciona una representación textual de la información visual contenida en un objeto . No todos los objetos admiten **la propiedad Value.**

La **propiedad Value** se recupera mediante una llamada a [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

La **propiedad Value** indica al cliente la información visual contenida en un objeto . Por ejemplo, el valor de un control de edición es el texto que contiene, mientras que un elemento de menú no tiene ningún valor.

## <a name="providing-hierarchical-information"></a>Proporcionar información jerárquica

La **propiedad Value** proporciona información jerárquica en casos como un control de vista de árbol. Aunque el objeto primario del control de vista de árbol no proporciona información en la propiedad **Value,** cada elemento del control tiene un valor de base cero que representa su nivel dentro de la jerarquía. Los elementos de nivel superior tienen un valor de cero, los elementos de segundo nivel tienen un valor de uno, y así sucesivamente.

 

 




