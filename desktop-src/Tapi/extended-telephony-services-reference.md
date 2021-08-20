---
description: Las funciones de telefonía extendida se enumeran por categoría en las tablas siguientes.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Referencia de servicios de telefonía extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c37ec658592b3dbaad5187f8dbf14489d269cff71f923fc68905fc1393941d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945436"
---
# <a name="extended-telephony-services-reference"></a>Referencia de servicios de telefonía extendidos

Las funciones de telefonía extendida se enumeran por categoría en las tablas siguientes.

## <a name="extended-telephony-functions-for-line-devices"></a>Funciones de telefonía extendidas para dispositivos de línea



| Función                                                   | Descripción                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | Permite que una aplicación negocie una versión de extensión que se usará con el dispositivo de línea especificado. Asincrónica |
| [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | Proporciona a los proveedores de servicios acceso a características específicas del dispositivo que no ofrecen otras funciones tapi. Synchronous. |
| [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | Envía características de conmutador específicas del dispositivo al conmutador. Asincrónica                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a>Funciones de telefonía extendidas para Teléfono dispositivos



| Función                                                     | Descripción                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | Función de escape específica del dispositivo para permitir extensiones dependientes del proveedor. Asincrónica                          |
| [**PhoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Permite que una aplicación negocie una versión de extensión para usarla con el dispositivo telefónico especificado. Synchronous. |



 

 

 



