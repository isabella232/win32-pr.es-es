---
description: El búfer de compatibilidad es específico del estándar de p. 931 de ISDN. Consulte la documentación de los proveedores de servicios sobre el significado y el uso de estos datos.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Búfer de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677489"
---
# <a name="compatibility-buffer"></a><span data-ttu-id="5c6da-104">Búfer de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="5c6da-104">Compatibility Buffer</span></span>

<span data-ttu-id="5c6da-105">El búfer de compatibilidad es específico del estándar de p. 931 de ISDN.</span><span class="sxs-lookup"><span data-stu-id="5c6da-105">The compatibility buffer is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="5c6da-106">Consulte la documentación del proveedor de servicios sobre el significado y el uso de estos datos.</span><span class="sxs-lookup"><span data-stu-id="5c6da-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="5c6da-107">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="5c6da-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="5c6da-108">**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** y **dwLowLevelCompOffset** miembros de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="5c6da-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize**, and **dwLowLevelCompOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="5c6da-109">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** y **CIB \_ LOWLEVELCOMPATIBILITYBUFFER** en el [**\_ búfer de CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="5c6da-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_HIGHLEVELCOMPATIBILITYBUFFER** and **CIB\_LOWLEVELCOMPATIBILITYBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
