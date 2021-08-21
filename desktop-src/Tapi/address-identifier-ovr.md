---
description: Después de la asignación de direcciones, TAPI asigna identificadores de dirección a las direcciones.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Identificadores de dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fa2d3a9aead56c0354cb7ffa487c7044853a25ea40c88b00b9eea0fa7db0f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872399"
---
# <a name="address-identifiers"></a>Identificadores de dirección

Después de la asignación de direcciones, TAPI asigna identificadores de dirección a las direcciones. Un *identificador de* dirección es un número entre 0 y el número de direcciones de la línea menos uno. Un identificador de dirección es un número permanente asignado a un dispositivo determinado y permanece constante incluso en las actualizaciones del sistema operativo. La combinación de identificador [de dispositivo e](device-identifier-ovr.md) identificador de dirección identifica de forma única una dirección determinada.

**TAPI 2.x:** Las aplicaciones obtienen un identificador de dirección (y un identificador de dispositivo) durante una llamada a [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) o [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), en la estructura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) o en una llamada a [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).

**TAPI 3.x:** [**ItAddressCapabilities::get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) llamado *AddressCap* establecido en el miembro **AC \_ ADDRESSID** de [**ADDRESS \_ CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) devolverá con el parámetro *plCapability* establecido en el identificador de dirección actual.

 

 
