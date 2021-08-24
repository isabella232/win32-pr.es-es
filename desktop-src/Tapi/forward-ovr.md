---
description: El reenvío es la contracción de una sesión entrante a una dirección de destino diferente.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Adelante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddddd21a945c3ca63a5c9040b8eabe0d1056b74b2f819f3fb62dbd8b760aaca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660855"
---
# <a name="forward"></a>Adelante

El reenvío es la contracción de una sesión entrante a una dirección de destino diferente. TAPI permite a una aplicación especificar una lista de condiciones de reenvío para una dirección. Las condiciones de reenvío pueden ser tan específicas como un destino diferente y el modo de reenvío [**para**](./lineforwardmode--constants.md) cada dirección del autor de la llamada.

La operación de reenvío también se puede usar para implementar una característica selectiva de no alterar, reenviando algunos llamadores al correo de voz y permitiendo que otros intenten completarse.

La operación de reenvío también puede cancelar cualquier reenvío actualmente en vigor.

Algunos proveedores de servicios requieren que una aplicación cree una llamada de consulta antes de una operación de reenvío. A continuación, la operación de reenvío se pasa un puntero a la llamada de consulta.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Para establecer [**lineForward para**](/windows/win32/api/tapi/nf-tapi-lineforward) obtener [**lineGetAddressStatus,**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)cambie el mensaje de notificación [**LINE \_ ADDRESSSTATE**](./line-addressstate.md) por LINEADDRESSSTATE \_ FORWARD.

**TAPI 3.x:** Vea [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), notificación de cambio: [**ITAddressEvent::get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ FORWARD.

> [!Note]  
> Puede que sea imposible que un proveedor de servicios sepa en todo momento qué reenvío está en vigor para una dirección. El reenvío se puede cancelar o cambiar de manera que no se realice una notificación al proveedor de servicios.

 

 

 
