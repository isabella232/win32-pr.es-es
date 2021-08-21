---
description: Origin es una descripción general de dónde se inició la sesión, por ejemplo, si es externa o interna a una red corporativa. Consulte LINECALLORIGIN \_ Constants (Constantes LINECALLORIGIN) para obtener una lista de los orígenes que admite TAPI.
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: Origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a1f4dafd2b4a3ee85b3a05b3c8ab8f95656237b0ad5bf292c53a5bbb2d3bed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002833"
---
# <a name="origin"></a>Origen

Origin es una descripción general de dónde se inició la sesión, por ejemplo, si es externa o interna a una red corporativa. Consulte [LINECALLORIGIN \_ Constants (Constantes LINECALLORIGIN)](./linecallorigin--constants.md) para obtener una lista de los orígenes que admite TAPI.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**miembro dwOrigin** *de lpCallInfo*).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**miembro CIL \_ ORIGIN** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
