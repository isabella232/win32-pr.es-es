---
description: La identificación identifica la dirección de destino original de una sesión. En situaciones en las que una sesión se redirigió, reenvió o transfirió, es diferente de la identificación conectada.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Llamada de identificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911213"
---
# <a name="called-identification"></a><span data-ttu-id="0e920-104">Llamada de identificación</span><span class="sxs-lookup"><span data-stu-id="0e920-104">Called Identification</span></span>

<span data-ttu-id="0e920-105">La identificación identifica la dirección de destino original de una sesión.</span><span class="sxs-lookup"><span data-stu-id="0e920-105">Called identification identifies the original destination address for a session.</span></span> <span data-ttu-id="0e920-106">En situaciones en las que una sesión se redirigió, reenvió o transfirió, es diferente de la [identificación conectada](connected-identification-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="0e920-106">In situations where a session was redirected, forwarded, or transferred, this will be different than the [connected identification](connected-identification-ovr.md).</span></span>

<span data-ttu-id="0e920-107">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="0e920-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="0e920-108">**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset** y **dwCalledIDAddressType** miembros de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="0e920-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset**, and **dwCalledIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="0e920-109">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLEDIDADDRESSTYPE** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLEDIDNAME** y **CIS \_ CALLEDIDNAME** miembros de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="0e920-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLEDIDNAME** and **CIS\_CALLEDIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
