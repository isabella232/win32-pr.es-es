---
description: La información específica de la aplicación permite a las aplicaciones pasar cada otra información relativa a una sesión a través de TAPI. TAPI no interpreta esta información y el uso está definido por completo en las aplicaciones.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Información específica de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678572"
---
# <a name="application-specific-information"></a>Información específica de la aplicación

La información específica de la aplicación permite a las aplicaciones pasar cada otra información relativa a una sesión a través de TAPI. TAPI no interpreta esta información y el uso está definido por completo en las aplicaciones.

Cuando una aplicación cambia la información específica de la aplicación, TAPI envía al resto de las aplicaciones con privilegios de monitor o propietario en la sesión un evento que indica que se ha producido un cambio.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*DwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**line \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* establecido en LINECALLINFOSTATE \_ APPSPECIFIC).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**miembro \_ APPSPECIFIC de CIL** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
