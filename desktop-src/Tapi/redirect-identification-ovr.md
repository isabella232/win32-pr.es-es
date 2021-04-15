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
# <a name="redirect-identification"></a><span data-ttu-id="a156c-103">Identificación de redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="a156c-103">Redirect Identification</span></span>

<span data-ttu-id="a156c-104">Cuando una aplicación [redirige](redirect-ovr.md) una sesión, TAPI conserva la información de identificación sobre la ubicación que redirigió la sesión y la ubicación a la que se redirigió.</span><span class="sxs-lookup"><span data-stu-id="a156c-104">When an application [redirects](redirect-ovr.md) a session, TAPI retains identification information about the location that redirected the session and the location to which it was redirected.</span></span>

<span data-ttu-id="a156c-105">"Redirigiendo" hace referencia a la ubicación que invocó la operación de redirección.</span><span class="sxs-lookup"><span data-stu-id="a156c-105">"Redirecting" refers to the location that invoked the redirect operation.</span></span> <span data-ttu-id="a156c-106">"Redirección" identifica el nuevo destino de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a156c-106">"Redirection" identifies the new destination for the session.</span></span>

<span data-ttu-id="a156c-107">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="a156c-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="a156c-108">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** y **dwRedirectingIDNameOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="a156c-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize**, and **dwRedirectingIDNameOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="a156c-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)llamado con el **miembro CIS \_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER**, **CIS \_ REDIRECTINGIDNAME** o **CIS \_ REDIRECTINGIDNUMBER** de la [**\_ cadena CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span><span class="sxs-lookup"><span data-stu-id="a156c-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with the **CIS\_REDIRECTIONIDNAME**, **CIS\_REDIRECTIONIDNUMBER**, **CIS\_REDIRECTINGIDNAME**, or **CIS\_REDIRECTINGIDNUMBER** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span></span>

 

 
