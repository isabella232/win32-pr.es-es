---
description: La aplicación debe inventariar los recursos de comunicaciones disponibles para ella y, a continuación, notificar a TAPI qué recursos usará y cómo los usará.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventario de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436479877f63255ce6132a5907f97a511efea16dd5e21db41b0e41000beb8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773425"
---
# <a name="resource-inventory"></a>Inventario de recursos

La aplicación debe inventariar los recursos de comunicaciones disponibles para ella y, a continuación, notificar a TAPI qué recursos usará y cómo los usará. Consulte [Control de dispositivos](device-control.md) para obtener información adicional sobre los tipos de recursos y funcionalidades a los que puede acceder una aplicación.

**TAPI 2.x:** Las aplicaciones obtienen el número de líneas disponibles [**cuando lineInitializeEx devuelve.**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) A continuación, pueden [**realizar lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) en cada línea, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para cada dirección y [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) para cada línea que se usará.

**TAPI 3.x:** Las aplicaciones [**usan ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) o [**ITTAPI::get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) para detectar las direcciones disponibles. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) e [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) suministran información sobre los tipos de comunicación posibles para cada dirección. Si lo implementa el proveedor de servicios, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) proporciona a una aplicación acceso a información y controles adicionales.

 

 
