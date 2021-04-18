---
description: 'Cómo crear procesadores de buzones. Los procesadores de buzones son compatibles con tres funciones especializadas: CreateMailslot, GetMailslotInfo y SetMailslotInfo. El servidor de buzón de correo utiliza estas funciones.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Creación de un buzón de correo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4cfbcf990162347d1e45da01c815002f39299e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688520"
---
# <a name="creating-a-mailslot"></a>Creación de un buzón de correo

Los procesadores de buzones son compatibles con tres funciones especializadas: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)y [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo). El servidor de buzón de correo utiliza estas funciones.

En el ejemplo de código siguiente se usa la función [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) para recuperar el identificador de un buzón de correo denominado "Sample de \_ buzón de correo". En el ejemplo de código [que se escribe en un buzón de correo](writing-to-a-mailslot.md) se muestra cómo la aplicación cliente puede escribir en este buzón de correo.


```C++
#include <windows.h>
#include <stdio.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WINAPI MakeSlot(LPCTSTR lpszSlotName) 
{ 
    hSlot = CreateMailslot(lpszSlotName, 
        0,                             // no maximum message size 
        MAILSLOT_WAIT_FOREVER,         // no time-out for operations 
        (LPSECURITY_ATTRIBUTES) NULL); // default security
 
    if (hSlot == INVALID_HANDLE_VALUE) 
    { 
        printf("CreateMailslot failed with %d\n", GetLastError());
        return FALSE; 
    } 
    else printf("Mailslot created successfully.\n"); 
    return TRUE; 
}

void main()
{ 
   MakeSlot(SlotName);
}
```



Para crear un buzón de correo que pueda ser heredado por procesos secundarios, una aplicación debe cambiar la estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) pasada como el último parámetro de [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota). Para ello, la aplicación establece el miembro **bInheritHandle** de esta estructura en **true** (el valor predeterminado es **false**).

 

 
