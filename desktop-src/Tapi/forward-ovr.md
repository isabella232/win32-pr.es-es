---
description: El reenvío es la desviación de una sesión entrante en una dirección de destino diferente.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Adelante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907975"
---
# <a name="forward"></a>Adelante

El reenvío es la desviación de una sesión entrante en una dirección de destino diferente. TAPI permite que una aplicación especifique una lista de condiciones de reenvío para una dirección. Las condiciones de reenvío pueden ser tan precisas como un modo de destino y [**reenvío**](./lineforwardmode--constants.md) diferente para cada dirección del llamador.

La operación de reenvío también se puede usar para implementar una característica de acción de no molestar selectiva, reenviando algunos autores de llamadas al correo de voz y permitiendo que otros intenten finalizar.

La operación de reenvío también puede cancelar cualquier reenvío que esté actualmente en vigor.

Algunos proveedores de servicios requieren que una aplicación cree una llamada de consulta antes de una operación de reenvío. A continuación, se pasa a la operación de reenvío un puntero a la llamada de consulta.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Para establecer [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) para obtener [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), cambie la [**línea \_ ADDRESSSTATE**](./line-addressstate.md) mensaje de notificación con LINEADDRESSSTATE \_ forward.

**TAPI 3. x:** Vea [**ITAddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress:: get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), Change Notification: [**ITADDRESSEVENT:: get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ forward.

> [!Note]  
> Puede ser imposible que un proveedor de servicios sepa en todo momento qué reenvío está en vigor para una dirección. El reenvío se puede cancelar o cambiar de maneras que no producen notificaciones al proveedor de servicios.

 

 

 
