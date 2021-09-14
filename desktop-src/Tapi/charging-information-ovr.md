---
description: La información de carga es específica del estándar ISDN Q.931. Consulte la documentación de los proveedores de servicios sobre el significado y el uso de estos datos.
ms.assetid: 5032e2cb-486a-4667-9873-bf88365f12cf
title: Información de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14d988ec34e901a94e27156f321436b59714cffb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264980"
---
# <a name="charging-information"></a>Información de carga

La información de carga es específica del estándar ISDN Q.931. Consulte la documentación del proveedor de servicios sobre el significado y el uso de estos datos.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwChargingInfoSize** y **dwChargingInfoOffset** miembros *de lpCallInfo*).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**miembro \_ CIB CHARGINGINFOBUFFER** de [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
