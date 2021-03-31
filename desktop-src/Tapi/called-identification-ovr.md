---
description: La identificación identifica la dirección de destino original de una sesión. En situaciones en las que una sesión se redirigió, reenvió o transfirió, es diferente de la identificación conectada.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Llamada de identificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911213"
---
# <a name="called-identification"></a>Llamada de identificación

La identificación identifica la dirección de destino original de una sesión. En situaciones en las que una sesión se redirigió, reenvió o transfirió, es diferente de la [identificación conectada](connected-identification-ovr.md).

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset** y **dwCalledIDAddressType** miembros de *lpCallInfo*).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLEDIDADDRESSTYPE** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLEDIDNAME** y **CIS \_ CALLEDIDNAME** miembros de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
