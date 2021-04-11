---
description: Origin es una descripción general de la ubicación en la que se inició la sesión, por ejemplo, si es externa o interna de una red corporativa. Vea \_ constantes LINECALLORIGIN para obtener una lista de los orígenes que admite TAPI.
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: Origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71105caff17850c76c1e2c388911086a4cf9ea8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156488"
---
# <a name="origin"></a>Origen

Origin es una descripción general de la ubicación en la que se inició la sesión, por ejemplo, si es externa o interna de una red corporativa. Vea [ \_ constantes LINECALLORIGIN](./linecallorigin--constants.md) para obtener una lista de los orígenes que admite TAPI.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (miembro **dwOrigin** de *lpCallInfo*).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (miembro de **\_ origen de CIL** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
