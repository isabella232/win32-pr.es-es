---
description: Obtenga información sobre la compatibilidad con los deltas de PrintTicket. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Compatibilidad con printticket deltas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548789"
---
# <a name="supporting-printticket-deltas"></a>Compatibilidad con printticket deltas

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La interfaz del proveedor PrintTicket tiene métodos que se pueden usar para realizar cambios incrementales en un PrintTicket existente. Los cambios incrementales de PrintTicket se pueden especificar en un PrintTicket parcial que se conoce como printTicket delta. Se crea un PrintTicket revisado combinando un valor delta de PrintTicket con un PrintTicket existente. Consulte el próximo documento de la interfaz del proveedor PrintTicket para obtener más información sobre los métodos que implican los deltas de PrintTicket.

Cuando se procesa un delta de PrintTicket, se deben realizar los pasos siguientes.

1.  Identifique las instancias de Feature o ParameterInit que son comunes tanto a la clase PrintTicket existente (printTicket de destino) como a la diferencia PrintTicket.

    -   Para cada característica común a la diferencia PrintTicket y PrintTicket de destino, reemplace la característica en el PrintTicket de destino por la característica correspondiente en la diferencia PrintTicket.

    -   Para cada ParameterInit común a la propiedad PrintTicket de destino y a la diferencia PrintTicket, reemplace ParameterInit en el PrintTicket de destino por el parámetro ParameterInit correspondiente en el delta de PrintTicket.

2.  Copie todas las instancias de Feature y ParameterInit restantes de la diferencia PrintTicket en el PrintTicket de destino.

3.  Si el algoritmo de resolución de conflictos permite especificar prioridades en el propio PrintTicket, puede elegir elevar las prioridades de las instancias Feature y ParameterInit denominadas en la diferencia PrintTicket.

4.  Realice la validación de PrintTicket como se describe en [Lista de comprobación de validación de PrintTicket.](printticket-validation-checklist.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



