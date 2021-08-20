---
description: El identificador de llamada difiere del identificador de sesión de dos maneras principales que el proveedor de servicios le asigna y es el mismo para cada aplicación que controla la sesión.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: Identificador de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb32a8cd00e3c8f77bcabb14de79170a259fba0e40ddb354afeab022528369c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870155"
---
# <a name="call-id"></a>Identificador de llamada

El identificador de llamada [](session-identifier-ovr.md) difiere del identificador de sesión de dos maneras principales: el proveedor de servicios lo asigna y es el mismo para cada aplicación que controla la sesión. No se puede usar para la comunicación normal con TAPI relativa a las operaciones de sesión porque no coincide con una aplicación determinada.

El identificador de llamada se usa en operaciones como determinar si un grupo de identificadores de sesión hace referencia realmente a una llamada, como es el caso de una conferencia, o para las comunicaciones con otra aplicación.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**miembro dwCallID** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**miembro CIL \_ CALLID** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
