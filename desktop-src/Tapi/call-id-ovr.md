---
description: El identificador de la llamada difiere del identificador de sesión de dos formas principales en que el proveedor de servicios lo asigna y es el mismo para todas las aplicaciones que controlan la sesión.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: IDENTIFICADOR de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687568"
---
# <a name="call-id"></a><span data-ttu-id="02f2a-103">IDENTIFICADOR de llamada</span><span class="sxs-lookup"><span data-stu-id="02f2a-103">Call ID</span></span>

<span data-ttu-id="02f2a-104">El identificador de la llamada difiere del [identificador de sesión](session-identifier-ovr.md) de dos maneras principales: el proveedor de servicios lo asigna y es el mismo para todas las aplicaciones que controlan la sesión.</span><span class="sxs-lookup"><span data-stu-id="02f2a-104">The Call ID differs from the [Session Identifier](session-identifier-ovr.md) in two primary ways: the service provider assigns it, and it is the same for every application that handles the session.</span></span> <span data-ttu-id="02f2a-105">No se puede usar para la comunicación normal con TAPI en relación con las operaciones de sesión porque no coincide con una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="02f2a-105">It cannot be used for ordinary communication with TAPI concerning session operations because it does not match to a particular application.</span></span>

<span data-ttu-id="02f2a-106">El identificador de llamada se usa en operaciones como determinar si un grupo de identificadores de sesión hace referencia realmente a una llamada, como es el caso de una conferencia o para comunicaciones con otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="02f2a-106">The Call ID is used in operations such as determining whether a group of session IDs actually refer to one call, as is the case for a conference, or for communications with another application.</span></span>

<span data-ttu-id="02f2a-107">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="02f2a-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="02f2a-108">**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (miembro **dwCallID** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="02f2a-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="02f2a-109">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLID** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="02f2a-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLID** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
