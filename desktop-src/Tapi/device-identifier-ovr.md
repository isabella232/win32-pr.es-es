---
description: Un identificador de dispositivo es un identificador independiente de la aplicación para un dispositivo de comunicaciones específico.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Identificador de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19078b7d2774fb2b71d951fade9c7a560a597a188ac4d87982ee2a6f2bfc9416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946003"
---
# <a name="device-identifier"></a>Identificador de dispositivo

Un *identificador de dispositivo* es un identificador independiente de la aplicación para un dispositivo de comunicaciones específico. Normalmente solo es necesario cuando una aplicación TAPI necesita entregar parte del procesamiento que implica una sesión de comunicaciones a las funciones de una API diferente. Por ejemplo, es posible que las aplicaciones TAPI 2.2 no puedan acceder directamente a un flujo multimedia y puedan usar Wave API.

**TAPI 2.x:** Vea [**lineGetID.**](/windows/win32/api/tapi/nf-tapi-linegetid)

**TAPI 3.x:** Vea [**ITAddressCapabilities::get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC \_ PERMANENTDEVICEID** member of [**ADDRESS \_ CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).

 

 
