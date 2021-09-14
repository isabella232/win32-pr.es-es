---
description: Privilegio hace referencia a si una aplicación posee o está supervisando la sesión.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilegio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160620"
---
# <a name="privilege"></a>Privilegio

Privilegio hace referencia a si una aplicación posee o está supervisando la sesión. Si la aplicación es propietaria de la sesión, puede realizar diversas operaciones de sesión. Si la aplicación solo está supervisando, recibirá mensajes de estado y puede acceder a la información de la sesión, pero cualquier intento de realizar la mayoría de las operaciones producirá un error.

Durante la inicialización, una aplicación indica a TAPI qué nivel de privilegios requiere en qué direcciones. TAPI ofrece sesiones entrantes solo a las aplicaciones que se han registrado para los privilegios de propietario o propietario y de supervisión.

El privilegio de una aplicación en una sesión que crea siempre es propietario.

**TAPI 2.x:** Vea [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **miembro dwCallPrivilege** de [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), llamado con el miembro **CIL \_ NUMBEROFOWNERS** o **CIL \_ NUMBEROFMONITORS** de [**CALLINFO \_ LONG.**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
