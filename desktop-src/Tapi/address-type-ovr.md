---
description: El tipo de dirección de dispositivo describe las formas de direccionamiento permitido en una dirección, como un número de teléfono o una dirección IP.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Tipo de dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678125"
---
# <a name="address-type"></a>Tipo de dirección

El tipo de dirección de dispositivo describe las formas de direccionamiento permitido en una dirección, como un número de teléfono o una dirección IP. Un dispositivo determinado comprenderá uno o varios tipos de direcciones. Para obtener una lista de tipos de direcciones compatibles con TAPI, vea [ \_ constantes LINEADDRESSTYPE](lineaddresstype--constants.md). La [traducción de direcciones](initiate-a-session-ovr.md) se puede usar para convertir una dirección de un tipo a otro.

Para obtener información general sobre las direcciones, vea [Dirección](address-ovr.md) en [categorías de dispositivos](device-categories.md).

El [tipo de dirección de una sesión](address-type-for-a-session-ovr.md) será un subconjunto de los tipos de direcciones de dispositivo.

**TAPI 2. x:** Vea [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) y el miembro **dwAddressType** de [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).

**TAPI 3. x:** Vea [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), con *AddressCap* establecido en el miembro **AC \_ ADDRESSTYPES** de [**la \_ funcionalidad Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).

 

 
