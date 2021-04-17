---
description: Después de la asignación de direcciones, TAPI asigna identificadores de dirección a las direcciones.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Identificadores de direcciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686635"
---
# <a name="address-identifiers"></a>Identificadores de direcciones

Después de la asignación de direcciones, TAPI asigna identificadores de dirección a las direcciones. Un *identificador de dirección* es un número entre 0 y el número de direcciones de la línea menos uno. Un identificador de dirección es un número permanente asignado a un dispositivo determinado y permanece constante entre las actualizaciones del sistema operativo. La combinación de [identificador de dispositivo](device-identifier-ovr.md) e identificador de dirección identifica de forma única una dirección determinada.

**TAPI 2. x:** Las aplicaciones obtienen un identificador de dirección (y un identificador de dispositivo) durante una llamada a [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) o [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), en la estructura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) o en una llamada a [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).

**TAPI 3. x:** El valor de [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) llamado *AddressCap* establecido en el miembro **AC \_ ADDRESSID** de la [**\_ funcionalidad Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) volverá con el parámetro *plCapability* establecido en el identificador de dirección actual.

 

 
