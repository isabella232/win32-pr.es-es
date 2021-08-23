---
description: El privilegio hace referencia a si una aplicación posee o supervisa la sesión.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilegio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4423b5eb1d50f5a7329726ab2e01040971daecca7e603247c49bcbc1d7c6d570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060583"
---
# <a name="privilege"></a>Privilegio

El privilegio hace referencia a si una aplicación posee o supervisa la sesión. Si la aplicación posee la sesión, se permite realizar diversas operaciones de sesión. Si la aplicación solo está supervisando, recibirá mensajes de estado y puede acceder a la información de sesión, pero cualquier intento de realizar la mayoría de las operaciones producirá un error.

Durante la inicialización, una aplicación indica a TAPI qué nivel de privilegios requiere en qué direcciones. TAPI solo ofrece sesiones entrantes a las aplicaciones que se han registrado para el propietario o propietario y supervisar privilegios.

El privilegio de una aplicación en una sesión que crea siempre es propietario.

**TAPI 2.x:** Vea [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), llamado con el miembro **CIL \_ NUMBEROFOWNERS** o **CIL \_ NUMBEROFMONITORS** de [**CALLINFO \_ LONG.**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
