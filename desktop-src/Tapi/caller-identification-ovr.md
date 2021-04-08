---
description: La identificación del autor de la llamada proporciona información sobre la entidad de llamada al recibir una sesión entrante. Normalmente, una aplicación usa estos datos como parte de un mensaje de estado a un usuario.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identificación del autor de la llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911210"
---
# <a name="caller-identification"></a>Identificación del autor de la llamada

La identificación del autor de la llamada proporciona información sobre la entidad de llamada al recibir una sesión entrante. Normalmente, una aplicación usa estos datos como parte de un mensaje de estado a un usuario.

Esta información no siempre está disponible inmediatamente. Una aplicación que desea usar esta información y ha comprobado que el proveedor de servicios la admite debe comprobarse varias veces antes de asumir que la información no está disponible.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** y **dwCallerIDAddressType** miembros de *lpCallInfo*).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLERIDADDRESSTYPE** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** y **CIS \_ CALLERIDNAME** miembros de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
