---
description: Las posibles razones de una sesión entrante, como que se transfirieron, se enumeran en las constantes LINECALLREASON. \_
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: Razón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4be431b5d3918714a11fb95411a8d5503a47f9e6d4cd462f9a208f00dfb96c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139958"
---
# <a name="reason"></a>Motivo

Las posibles razones de una sesión entrante, como que se transfirieron, se enumeran en [las constantes LINECALLREASON \_ ](./linecallreason--constants.md).

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** member of *lpCallInfo*)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** miembro CIL \_ REASON** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))

 

 
