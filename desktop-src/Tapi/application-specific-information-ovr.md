---
description: La información específica de la aplicación permite que las aplicaciones pasen entre sí información relacionada con una sesión a través de TAPI. TAPI no interpreta esta información y el uso lo definen por completo las aplicaciones.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Información específica de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473424"
---
# <a name="application-specific-information"></a>Información específica de la aplicación

La información específica de la aplicación permite que las aplicaciones pasen entre sí información relacionada con una sesión a través de TAPI. TAPI no interpreta esta información y el uso lo definen por completo las aplicaciones.

Cuando una aplicación cambia la información específica de la aplicación, TAPI envía a todas las demás aplicaciones con privilegios de monitor o propietario en la sesión un evento que indica que se ha producido un cambio.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**LINE \_ CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE \_ APPSPECIFIC).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**miembro \_ CIL APPSPECIFIC** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
