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
# <a name="application-specific-information"></a><span data-ttu-id="f9274-104">Información específica de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f9274-104">Application-specific Information</span></span>

<span data-ttu-id="f9274-105">La información específica de la aplicación permite a las aplicaciones pasar cada otra información relativa a una sesión a través de TAPI.</span><span class="sxs-lookup"><span data-stu-id="f9274-105">Application-specific information allows applications to pass each other information concerning a session through TAPI.</span></span> <span data-ttu-id="f9274-106">TAPI no interpreta esta información y el uso está definido por completo en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f9274-106">This information is not interpreted by TAPI and usage is entirely defined by the applications.</span></span>

<span data-ttu-id="f9274-107">Cuando una aplicación cambia la información específica de la aplicación, TAPI envía al resto de las aplicaciones con privilegios de monitor o propietario en la sesión un evento que indica que se ha producido un cambio.</span><span class="sxs-lookup"><span data-stu-id="f9274-107">When application-specific information is changed by one application, TAPI sends all other applications with monitor or owner privileges on the session an event indicating that a change has occurred.</span></span>

<span data-ttu-id="f9274-108">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="f9274-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f9274-109">**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*DwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**line \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* establecido en LINECALLINFOSTATE \_ APPSPECIFIC).</span><span class="sxs-lookup"><span data-stu-id="f9274-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_APPSPECIFIC).</span></span>

<span data-ttu-id="f9274-110">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**miembro \_ APPSPECIFIC de CIL** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="f9274-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL\_APPSPECIFIC** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
