---
description: El búfer de compatibilidad es específico del estándar de p. 931 de ISDN. Consulte la documentación de los proveedores de servicios sobre el significado y el uso de estos datos.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Búfer de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677489"
---
# <a name="compatibility-buffer"></a>Búfer de compatibilidad

El búfer de compatibilidad es específico del estándar de p. 931 de ISDN. Consulte la documentación del proveedor de servicios sobre el significado y el uso de estos datos.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** y **dwLowLevelCompOffset** miembros de *lpCallInfo*).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** y **CIB \_ LOWLEVELCOMPATIBILITYBUFFER** en el [**\_ búfer de CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
