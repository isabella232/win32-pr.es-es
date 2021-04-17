---
description: Las funciones de telefonía extendidas se enumeran por Categoría en las tablas siguientes.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Referencia de servicios de telefonía extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677380"
---
# <a name="extended-telephony-services-reference"></a>Referencia de servicios de telefonía extendidos

Las funciones de telefonía extendidas se enumeran por Categoría en las tablas siguientes.

## <a name="extended-telephony-functions-for-line-devices"></a>Funciones de telefonía extendidas para dispositivos de línea



| Función                                                   | Descripción                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | Permite que una aplicación negocie una versión de extensión para usarla con el dispositivo de línea especificado. Asincrónica |
| [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | Proporciona a los proveedores de servicios acceso a características específicas del dispositivo no ofrecidas por otras funciones TAPI. Synchronous. |
| [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | Envía características de conmutador específicas del dispositivo al conmutador. Asincrónica                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a>Funciones de telefonía extendidas para dispositivos telefónicos



| Función                                                     | Descripción                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | Función de escape específica del dispositivo para permitir las extensiones dependientes del proveedor. Asincrónica                          |
| [**PhoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Permite que una aplicación negocie una versión de extensión para usarla con el dispositivo de teléfono especificado. Synchronous. |



 

 

 



