---
description: El identificador de la llamada difiere del identificador de sesión de dos formas principales en que el proveedor de servicios lo asigna y es el mismo para todas las aplicaciones que controlan la sesión.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: IDENTIFICADOR de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687568"
---
# <a name="call-id"></a>IDENTIFICADOR de llamada

El identificador de la llamada difiere del [identificador de sesión](session-identifier-ovr.md) de dos maneras principales: el proveedor de servicios lo asigna y es el mismo para todas las aplicaciones que controlan la sesión. No se puede usar para la comunicación normal con TAPI en relación con las operaciones de sesión porque no coincide con una aplicación determinada.

El identificador de llamada se usa en operaciones como determinar si un grupo de identificadores de sesión hace referencia realmente a una llamada, como es el caso de una conferencia o para comunicaciones con otra aplicación.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (miembro **dwCallID** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLID** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
