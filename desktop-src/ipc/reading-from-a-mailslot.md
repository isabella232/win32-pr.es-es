---
description: Cómo leer desde un buzón de correo. El proceso que crea un buzón de correo puede leer mensajes de él mediante el uso del identificador de buzón de correo en una llamada a la función ReadFile.
ms.assetid: e193dca9-3b77-4e41-be6d-90992e1a8fe3
title: Leer de un buzón de correo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35458f90ca381689275417e0e525c2d5a31ac9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696213"
---
# <a name="reading-from-a-mailslot"></a><span data-ttu-id="9fb86-104">Leer de un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="9fb86-104">Reading from a Mailslot</span></span>

<span data-ttu-id="9fb86-105">El proceso que crea un buzón de correo puede leer mensajes de él mediante el uso del identificador de buzón de correo en una llamada a la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="9fb86-105">The process that creates a mailslot can read messages from it by using the mailslot handle in a call to the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function.</span></span> <span data-ttu-id="9fb86-106">En el ejemplo siguiente se llama a la función [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) para determinar si hay mensajes en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="9fb86-106">The following example calls the [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) function to determine whether there are messages in the mailslot.</span></span> <span data-ttu-id="9fb86-107">Si los mensajes están en espera, se muestran cada uno junto con el número de mensajes que quedan para leer.</span><span class="sxs-lookup"><span data-stu-id="9fb86-107">If messages are waiting, each is displayed along with the number of messages remaining to be read.</span></span>

<span data-ttu-id="9fb86-108">Un buzón de correo existe hasta que se llama a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para todos los identificadores de servidor abiertos o hasta que todos los procesos de servidor que poseen un identificador de buzón de correo salgan.</span><span class="sxs-lookup"><span data-stu-id="9fb86-108">A mailslot exists until the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function is called for all open server handles or until all server processes that own a mailslot handle exit.</span></span> <span data-ttu-id="9fb86-109">En ambos casos, los mensajes no leídos se eliminan del buzón de correo, se cierran todos los identificadores de cliente en el buzón de correo y el propio buzón se elimina de la memoria.</span><span class="sxs-lookup"><span data-stu-id="9fb86-109">In both cases, any unread messages are deleted from the mailslot, all client handles to the mailslot are closed, and the mailslot itself is deleted from memory.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL ReadSlot() 
{ 
    DWORD cbMessage, cMessage, cbRead; 
    BOOL fResult; 
    LPTSTR lpszBuffer; 
    TCHAR achID[80]; 
    DWORD cAllMessages; 
    HANDLE hEvent;
    OVERLAPPED ov;
 
    cbMessage = cMessage = cbRead = 0; 

    hEvent = CreateEvent(NULL, FALSE, FALSE, TEXT("ExampleSlot"));
    if( NULL == hEvent )
        return FALSE;
    ov.Offset = 0;
    ov.OffsetHigh = 0;
    ov.hEvent = hEvent;
 
    fResult = GetMailslotInfo( hSlot, // mailslot handle 
        (LPDWORD) NULL,               // no maximum message size 
        &cbMessage,                   // size of next message 
        &cMessage,                    // number of messages 
        (LPDWORD) NULL);              // no read time-out 
 
    if (!fResult) 
    { 
        printf("GetMailslotInfo failed with %d.\n", GetLastError()); 
        return FALSE; 
    } 
 
    if (cbMessage == MAILSLOT_NO_MESSAGE) 
    { 
        printf("Waiting for a message...\n"); 
        return TRUE; 
    } 
 
    cAllMessages = cMessage; 
 
    while (cMessage != 0)  // retrieve all messages
    { 
        // Create a message-number string. 
 
        StringCchPrintf((LPTSTR) achID, 
            80,
            TEXT("\nMessage #%d of %d\n"), 
            cAllMessages - cMessage + 1, 
            cAllMessages); 

        // Allocate memory for the message. 
 
        lpszBuffer = (LPTSTR) GlobalAlloc(GPTR, 
            lstrlen((LPTSTR) achID)*sizeof(TCHAR) + cbMessage); 
        if( NULL == lpszBuffer )
            return FALSE;
        lpszBuffer[0] = '\0'; 
 
        fResult = ReadFile(hSlot, 
            lpszBuffer, 
            cbMessage, 
            &cbRead, 
            &ov); 
 
        if (!fResult) 
        { 
            printf("ReadFile failed with %d.\n", GetLastError()); 
            GlobalFree((HGLOBAL) lpszBuffer); 
            return FALSE; 
        } 
 
        // Concatenate the message and the message-number string. 
 
        StringCbCat(lpszBuffer, 
                    lstrlen((LPTSTR) achID)*sizeof(TCHAR)+cbMessage, 
                    (LPTSTR) achID); 
 
        // Display the message. 
 
        _tprintf(TEXT("Contents of the mailslot: %s\n"), lpszBuffer); 
 
        GlobalFree((HGLOBAL) lpszBuffer); 
 
        fResult = GetMailslotInfo(hSlot,  // mailslot handle 
            (LPDWORD) NULL,               // no maximum message size 
            &cbMessage,                   // size of next message 
            &cMessage,                    // number of messages 
            (LPDWORD) NULL);              // no read time-out 
 
        if (!fResult) 
        { 
            printf("GetMailslotInfo failed (%d)\n", GetLastError());
            return FALSE; 
        } 
    } 
    CloseHandle(hEvent);
    return TRUE; 
}

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
    return TRUE; 
}

void main()
{
   MakeSlot(SlotName);

   while(TRUE)
   {
      ReadSlot();
      Sleep(3000);
   }
}
```



<span data-ttu-id="9fb86-110">El siguiente es el resultado que se muestra cuando se ejecuta este ejemplo con el cliente de buzón de correo que se muestra en [escribir en un buzón de correo](writing-to-a-mailslot.md).</span><span class="sxs-lookup"><span data-stu-id="9fb86-110">The following is the output that is displayed when this example is run with the mailslot client shown in [Writing to a Mailslot](writing-to-a-mailslot.md).</span></span>

``` syntax
Waiting for a message...
Waiting for a message...
Contents of the mailslot: Message one for mailslot.
Message #1 of 2

Contents of the mailslot: Message two for mailslot.
Message #2 of 2

Waiting for a message...
Contents of the mailslot: Message three for mailslot.
Message #1 of 1

Waiting for a message...
Waiting for a message...
Waiting for a message...
^C
```

 

 
