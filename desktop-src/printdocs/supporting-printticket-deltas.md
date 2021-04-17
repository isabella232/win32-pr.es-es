---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Compatibilidad con diferencias de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707619"
---
# <a name="supporting-printticket-deltas"></a>Compatibilidad con diferencias de PrintTicket

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La interfaz del proveedor PrintTicket tiene métodos que se pueden usar para realizar cambios incrementales en un PrintTicket existente. Los cambios incrementales de PrintTicket se pueden especificar en un PrintTicket parcial que se conoce como una diferencia de PrintTicket. Se crea un PrintTicket revisado mediante la combinación de una diferencia de PrintTicket con un PrintTicket existente. Vea el documento sobre la interfaz del proveedor de PrintTicket próximamente para obtener más información sobre los métodos que implican diferencias de PrintTicket.

Cuando se procesa una diferencia de PrintTicket, se deben realizar los siguientes pasos.

1.  Identifique las instancias de Feature o ParameterInit que son comunes al PrintTicket existente (el PrintTicket de destino) y la diferencia de PrintTicket.

    -   Para cada característica común al PrintTicket de destino y al delta de PrintTicket, reemplace la característica en el PrintTicket de destino por la característica correspondiente en la diferencia de PrintTicket.

    -   Para cada ParameterInit común al PrintTicket de destino y al delta de PrintTicket, reemplace el ParameterInit en el PrintTicket de destino por el ParameterInit correspondiente en la diferencia de PrintTicket.

2.  Copie todas las instancias de Feature y ParameterInit restantes en la diferencia de PrintTicket en el PrintTicket de destino.

3.  Si el algoritmo de resolución de conflictos permite que se especifiquen prioridades en el propio PrintTicket, puede optar por elevar las prioridades de la característica y las instancias de ParameterInit mencionadas en la diferencia de PrintTicket.

4.  Realice la validación de PrintTicket como se describe en la [lista de comprobación de validación de PrintTicket](printticket-validation-checklist.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



