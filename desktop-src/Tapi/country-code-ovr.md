---
description: El código de país o región solo es relevante cuando el tipo de dirección es LINEADDRESSTYPE \_ PHONENUMBER. Identifica un área del mundo.
ms.assetid: d838c2ac-4ee3-4314-8573-deed6c7430e3
title: Código de país o región
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5557e4d67b701fda2aa05ad81686ae474b172063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908217"
---
# <a name="country-or-region-code"></a><span data-ttu-id="75438-104">Código de país o región</span><span class="sxs-lookup"><span data-stu-id="75438-104">Country or Region Code</span></span>

<span data-ttu-id="75438-105">El código de país o región solo es relevante cuando el tipo de dirección es LINEADDRESSTYPE \_ PHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="75438-105">The country or region code is relevant only when the address type is LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="75438-106">Identifica un área del mundo.</span><span class="sxs-lookup"><span data-stu-id="75438-106">It identifies an area of the world.</span></span>

<span data-ttu-id="75438-107">Todos los proveedores de servicios que admiten el uso de números de teléfono deben admitir el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="75438-107">All service providers that support use of telephone numbers must support use of this information.</span></span>

<span data-ttu-id="75438-108">**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (miembro **dwCountryCode** de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="75438-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCountryCode** member of *lpCallInfo*).</span></span>

<span data-ttu-id="75438-109">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**\_ miembro de CIL** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="75438-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_COUNTRYCODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
