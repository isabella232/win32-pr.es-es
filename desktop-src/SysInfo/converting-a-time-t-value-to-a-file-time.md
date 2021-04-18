---
description: Las funciones de hora incluidas en el tiempo de ejecución de C usan el \_ tipo de tiempo t para representar el número de segundos transcurridos desde la medianoche del 1 de enero de 1970. En el ejemplo siguiente se convierte un \_ valor de hora t en una hora de archivo mediante la función Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Convertir un valor de time_t en una hora de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669976"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a><span data-ttu-id="4d0b0-104">Convertir un valor de hora \_ t en una hora de archivo</span><span class="sxs-lookup"><span data-stu-id="4d0b0-104">Converting a time\_t Value to a File Time</span></span>

<span data-ttu-id="4d0b0-105">Las funciones de hora incluidas en el tiempo de ejecución de C usan el \_ tipo de tiempo t para representar el número de segundos transcurridos desde la medianoche del 1 de enero de 1970.</span><span class="sxs-lookup"><span data-stu-id="4d0b0-105">The time functions included in the C run-time use the time\_t type to represent the number of seconds elapsed since midnight, January 1, 1970.</span></span> <span data-ttu-id="4d0b0-106">En el ejemplo siguiente se convierte un \_ valor de hora t en una hora de archivo mediante la función [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="4d0b0-106">The following example converts a time\_t value to a file time, using the [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) function.</span></span>


```C++
#include <windows.h>
#include <time.h>

void TimetToFileTime( time_t t, LPFILETIME pft )
{
    LONGLONG ll = Int32x32To64(t, 10000000) + 116444736000000000;
    pft->dwLowDateTime = (DWORD) ll;
    pft->dwHighDateTime = ll >>32;
}
```



<span data-ttu-id="4d0b0-107">Después de obtener un tiempo de archivo, puede convertir este valor a la hora del sistema mediante la función [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) .</span><span class="sxs-lookup"><span data-stu-id="4d0b0-107">After you have obtained a file time, you can convert this value to system time using the [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) function.</span></span>

 

 
