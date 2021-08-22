---
description: Cuando una aplicación redirige una sesión, TAPI conserva información de identificación sobre la ubicación que redirija la sesión y la ubicación a la que se redirija.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identificación de redireccionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7648167e6f60dc2e8593a576053df9a0ff54eb0fadc9a446a66127b435e5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060453"
---
# <a name="redirect-identification"></a>Identificación de redireccionamiento

Cuando una aplicación [redirige](redirect-ovr.md) una sesión, TAPI conserva información de identificación sobre la ubicación que redirija la sesión y la ubicación a la que se redirija.

"Redireccionamiento" hace referencia a la ubicación que invocó la operación de redireccionamiento. "Redireccionamiento" identifica el nuevo destino de la sesión.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** y **dwRedirectingIDNameOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)llamado con CIS **\_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER**, **CIS \_ REDIRECTINGIDNAME** o el miembro **CIS \_ REDIRECTINGIDNUMBER** de [**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
