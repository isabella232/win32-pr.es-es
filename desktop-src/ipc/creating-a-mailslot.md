---
description: 'Cómo crear mailslots. Los mailslots son compatibles con tres funciones especializadas: CreateMailslot, GetMailslotInfo y SetMailslotInfo. El servidor mailslot usa estas funciones.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Crear un mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebdc255772c8dbe06ff3a1258c5d2176f595d4e6e0a162bfbe662ce15838881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350425"
---
# <a name="creating-a-mailslot"></a>Crear un mailslot

Los mailslots son compatibles con tres funciones [**especializadas: CreateMailslot,**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)y [**SetMailslotInfo.**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) El servidor mailslot usa estas funciones.

En el ejemplo de código siguiente se usa [**la función CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) para recuperar el identificador de un mailslot denominado "mailslot \_ de ejemplo". El ejemplo de código de Writing to a Mailslot (Escribir [en mailslot)](writing-to-a-mailslot.md) muestra cómo la aplicación cliente puede escribir en este mailslot.


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



Para crear un mailslot que puedan heredar los procesos secundarios, una aplicación debe cambiar la estructura [**ATRIBUTOS \_ DE**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) SEGURIDAD pasada como el último parámetro de [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota). Para ello, la aplicación establece el miembro **bInheritHandle** de esta estructura en **TRUE** (el valor predeterminado es **FALSE).**

 

 
