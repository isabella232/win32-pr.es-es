---
title: Recuperar una cadena que describe un filtro
description: Recuperar una cadena que describe un filtro
ms.assetid: 47390448-eaa6-4bea-bd90-549fa37e739a
keywords:
- Administrador de compresión de audio (ACM), recuperar cadenas que describen filtros
- ACM (Administrador de compresión de audio), recuperar cadenas que describen filtros
- Ejemplos de ACM, recuperar cadenas que describen filtros
- recuperar cadenas que describen filtros
- acmFilterTagDetails función)
- acmFilterDetails función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641f2b9993d9c916113d14eaf92925e916409619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676251"
---
# <a name="retrieving-a-string-that-describes-a-filter"></a><span data-ttu-id="0d170-109">Recuperar una cadena que describe un filtro</span><span class="sxs-lookup"><span data-stu-id="0d170-109">Retrieving a String That Describes a Filter</span></span>

<span data-ttu-id="0d170-110">A menudo, una aplicación debe mostrar una cadena que describa el formato actual.</span><span class="sxs-lookup"><span data-stu-id="0d170-110">An application often needs to display a string that describes the current format.</span></span> <span data-ttu-id="0d170-111">Esta tarea se puede realizar fácilmente con las funciones [**acmFilterTagDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails) y [**acmFilterDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails) .</span><span class="sxs-lookup"><span data-stu-id="0d170-111">This task can be accomplished easily with the [**acmFilterTagDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails) and [**acmFilterDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails) functions.</span></span> <span data-ttu-id="0d170-112">Estas funciones deben llamarse con el filtro o la etiqueta de filtro adecuados.</span><span class="sxs-lookup"><span data-stu-id="0d170-112">These functions must be called with the appropriate filter or filter tag.</span></span> <span data-ttu-id="0d170-113">En el ejemplo siguiente se muestra cómo usar estas funciones.</span><span class="sxs-lookup"><span data-stu-id="0d170-113">The following example shows how to use these functions.</span></span>


```C++
#include <mmsystem.h>
#include <mmreg.h>
#include <msacm.h>

BOOL GetFilterDescription 
( 
    LPWAVEFILTER  pwfltr, 
    LPTSTR        pszFilterTag, 
    DWORD         cchFilterTag, // Size of pszFilterTag buffer.
    LPTSTR        pszFilter,
    DWORD         cchFilter     // Size of pszFilter buffer.

) 
{ 
    MMRESULT      mmr; 
    errno_t       errno;
 
    // Retrieve the name for the filter tag of the specified filter. 
    if (NULL != pszFilterTag) { 
        ACMFILTERTAGDETAILS aftd; 
 
        // Initialize all unused members of the ACMFILTERTAGDETAILS 
        // structure to zero. 
        memset(&aftd, 0, sizeof(aftd)); 
 
        // Fill in the required members of the ACMFILTERTAGDETAILS 
        // structure for the ACM_FILTERTAGDETAILSF_FILTERTAG query. 
        aftd.cbStruct = sizeof(aftd); 
        aftd.dwFilterTag = pwfltr->dwFilterTag; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter tag. 
        mmr = acmFilterTagDetails(NULL, &aftd, 
            ACM_FILTERTAGDETAILSF_FILTERTAG); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter tag. 
            return FALSE; 
        } 
 
        // Copy the filter tag name into the calling application's 
        // buffer. 

        errno = wcscpy_s(pszFilterTag, cchFilterTag, aftd.szFilterTag); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    // Retrieve the description of the attributes for the specified 
    // filter. 
    if (NULL != pszFilter) { 
        ACMFILTERDETAILS afd; 
 
        // Initialize all unused members of the ACMFILTERDETAILS 
        // structure to zero. 
        memset(&afd, 0, sizeof(afd)); 
 
        // Fill in the required members of the ACMFILTERDETAILS 
        // structure for the ACM_FILTERDETAILSF_FILTER query. 
        afd.cbStruct    = sizeof(afd); 
        afd.dwFilterTag = pwfltr->dwFilterTag; 
        afd.pwfltr      = pwfltr; 
        afd.cbwfltr     = pwfltr->cbStruct; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter. 
        mmr = acmFilterDetails(NULL, &afd, ACM_FILTERDETAILSF_FILTER); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter. 
            return FALSE; 
        } 
 
        // Copy the description string into the caller's buffer. 
        errno = wcscpy_s(pszFilter, cchFilter, afd.szFilter); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    return TRUE; 
}
 
```



 

 




