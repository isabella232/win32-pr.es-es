---
description: La aplicación debe realizar un inventario de los recursos de comunicaciones disponibles y, a continuación, notificar a TAPI los recursos que utilizará y cómo los usará.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventario de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677798"
---
# <a name="resource-inventory"></a>Inventario de recursos

La aplicación debe realizar un inventario de los recursos de comunicaciones disponibles y, a continuación, notificar a TAPI los recursos que utilizará y cómo los usará. Consulte [control de dispositivos](device-control.md) para obtener información adicional sobre los tipos de recursos y capacidades a los que puede tener acceso una aplicación.

**TAPI 2. x:** Las aplicaciones obtienen el número de líneas disponibles cuando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) devuelve. Después, pueden realizar [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) en cada línea, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para cada dirección y [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) para cada línea que se va a usar.

**TAPI 3. x:** Las aplicaciones usan [**ITTAPI:: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) o [**ITTAPI:: get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) para detectar las direcciones disponibles. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) y [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) proporcionan información sobre los tipos de comunicación posibles para cada dirección. Si lo implementa el proveedor de servicios, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) proporciona a la aplicación acceso a información y controles adicionales.

 

 
