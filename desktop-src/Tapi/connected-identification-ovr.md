---
description: La identificación conectada identifica la entidad a la que se conectó realmente. Puede ser diferente de la identificación llamada si se desvirtió la llamada.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Identificación conectada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361712"
---
# <a name="connected-identification"></a>Identificación conectada

La identificación conectada identifica la entidad a la que se conectó realmente. Puede ser diferente de la identificación llamada si se desvirtió la llamada.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **DwConnectedIDOffset**, **dwConnectedIDNameSize** y **dwConnectedIDNameOffset** miembros de *lpCallInfo*).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ CONNECTEDIDNAME** member of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
