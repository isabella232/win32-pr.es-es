---
description: La información de usuario es un búfer que se puede transmitir desde un extremo de una conexión a otra. Esta información es específica del estándar de p. 931 de ISDN. Consulte la documentación de los proveedores de servicios sobre el significado y el uso de estos datos.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Información de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546299"
---
# <a name="user-user-information"></a><span data-ttu-id="ace91-105">Información de usuario</span><span class="sxs-lookup"><span data-stu-id="ace91-105">User-user information</span></span>

<span data-ttu-id="ace91-106">La información de usuario es un búfer que se puede transmitir desde un extremo de una conexión a otra.</span><span class="sxs-lookup"><span data-stu-id="ace91-106">User-user information is a buffer that can be transmitted from one end of a connection to another.</span></span> <span data-ttu-id="ace91-107">Esta información es específica del estándar de p. 931 de ISDN.</span><span class="sxs-lookup"><span data-stu-id="ace91-107">This information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="ace91-108">Consulte la documentación del proveedor de servicios sobre el significado y el uso de estos datos.</span><span class="sxs-lookup"><span data-stu-id="ace91-108">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="ace91-109">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="ace91-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="ace91-110">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** y **dwCallDataOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="ace91-110">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span></span>

<span data-ttu-id="ace91-111">\* \* TAPI 3. x: \* \*[**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), llamado con el miembro **CIB \_ USERUSERINFO** del [**\_ búfer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo:: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="ace91-111">\*\*TAPI 3.x:  \*\*[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), called with the **CIB\_USERUSERINFO** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span></span>

 

 
