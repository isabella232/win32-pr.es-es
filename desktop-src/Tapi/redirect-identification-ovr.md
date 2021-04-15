---
description: Cuando una aplicación redirige una sesión, TAPI conserva la información de identificación sobre la ubicación que redirigió la sesión y la ubicación a la que se redirigió.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identificación de redireccionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689554"
---
# <a name="redirect-identification"></a>Identificación de redireccionamiento

Cuando una aplicación [redirige](redirect-ovr.md) una sesión, TAPI conserva la información de identificación sobre la ubicación que redirigió la sesión y la ubicación a la que se redirigió.

"Redirigiendo" hace referencia a la ubicación que invocó la operación de redirección. "Redirección" identifica el nuevo destino de la sesión.

No todos los proveedores de servicios admiten el uso de esta información.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** y **dwRedirectingIDNameOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)llamado con el **miembro CIS \_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER**, **CIS \_ REDIRECTINGIDNAME** o **CIS \_ REDIRECTINGIDNUMBER** de la [**\_ cadena CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
