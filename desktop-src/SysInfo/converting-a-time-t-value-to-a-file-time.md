---
description: Las funciones de tiempo incluidas en el tiempo de ejecución de C usan el tipo t de tiempo para representar el número de segundos transcurridos desde la medianoche del 1 de enero de \_ 1970. En el ejemplo siguiente se convierte un valor \_ time t en una hora de archivo, mediante la función Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Convertir un valor time_t en una hora de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068896"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>Convertir un valor time \_ t en una hora de archivo

Las funciones de tiempo incluidas en el tiempo de ejecución de C usan el tipo t de tiempo para representar el número de segundos transcurridos desde la medianoche del 1 de enero de \_ 1970. En el ejemplo siguiente se convierte un valor \_ time t en una hora de archivo, mediante la función [**Int32x32To64.**](/windows/desktop/api/winnt/nf-winnt-int32x32to64)


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



Después de obtener una hora de archivo, puede convertir este valor en la hora del sistema mediante la [**función FileTimeToSystemTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)

 

 
