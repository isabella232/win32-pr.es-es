---
description: La identificación del autor de la llamada proporciona información sobre la entidad de llamada al recibir una sesión entrante. Normalmente, una aplicación usa estos datos como parte de un mensaje de estado a un usuario.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identificación del autor de la llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911210"
---
# <a name="caller-identification"></a><span data-ttu-id="f201b-104">Identificación del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="f201b-104">Caller Identification</span></span>

<span data-ttu-id="f201b-105">La identificación del autor de la llamada proporciona información sobre la entidad de llamada al recibir una sesión entrante.</span><span class="sxs-lookup"><span data-stu-id="f201b-105">Caller identification provides information on the calling party when receiving an incoming session.</span></span> <span data-ttu-id="f201b-106">Normalmente, una aplicación usa estos datos como parte de un mensaje de estado a un usuario.</span><span class="sxs-lookup"><span data-stu-id="f201b-106">An application typically uses this data as part of a status message to a user.</span></span>

<span data-ttu-id="f201b-107">Esta información no siempre está disponible inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f201b-107">This information is not always available immediately.</span></span> <span data-ttu-id="f201b-108">Una aplicación que desea usar esta información y ha comprobado que el proveedor de servicios la admite debe comprobarse varias veces antes de asumir que la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="f201b-108">An application that wants to use this information and has verified that the service provider supports it should check several times before assuming that the information is not available.</span></span>

<span data-ttu-id="f201b-109">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="f201b-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f201b-110">**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** y **dwCallerIDAddressType** miembros de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="f201b-110">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset**, and **dwCallerIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="f201b-111">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLERIDADDRESSTYPE** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** y **CIS \_ CALLERIDNAME** miembros de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="f201b-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLERIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLERIDNAME** and **CIS\_CALLERIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
