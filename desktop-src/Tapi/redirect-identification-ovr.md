---
description: Cuando una aplicación redirige una sesión, TAPI conserva información de identificación sobre la ubicación que redirija la sesión y la ubicación a la que se redirija.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identificación de redirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068725"
---
# <a name="redirect-identification"></a>Identificación de redirección

Cuando una aplicación [redirige](redirect-ovr.md) una sesión, TAPI conserva información de identificación sobre la ubicación que redirija la sesión y la ubicación a la que se redirija.

"Redirección" hace referencia a la ubicación que invocó la operación de redireccionamiento. "Redireccionamiento" identifica el nuevo destino de la sesión.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** y **dwRedirectingIDNameOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)llamado con CIS **\_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER,** **CIS \_ REDIRECTINGIDNAME** o CIS **\_ REDIRECTINGIDNUMBER** miembro de [**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
