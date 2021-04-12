---
description: Número del tronco sobre el que se enruta la llamada. Este miembro se utiliza para las llamadas entrantes y salientes.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Tronco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4afea1387c6d43dc4d9a2f5a6a12f260a8daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278095"
---
# <a name="trunk"></a><span data-ttu-id="bf3a6-104">Tronco</span><span class="sxs-lookup"><span data-stu-id="bf3a6-104">Trunk</span></span>

<span data-ttu-id="bf3a6-105">Número del tronco sobre el que se enruta la llamada.</span><span class="sxs-lookup"><span data-stu-id="bf3a6-105">The number of the trunk over which the call is routed.</span></span> <span data-ttu-id="bf3a6-106">Este miembro se utiliza para las llamadas entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="bf3a6-106">This member is used for both incoming and outgoing calls.</span></span>

<span data-ttu-id="bf3a6-107">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="bf3a6-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="bf3a6-108">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="bf3a6-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="bf3a6-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), llamado con el miembro **\_ troncal de CIL** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="bf3a6-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with **CIL\_TRUNK** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

 

 
