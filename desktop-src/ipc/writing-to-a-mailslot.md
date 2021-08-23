---
description: Cómo escribir en un mailslot. Escribir en un mailslot es similar a escribir en un archivo de disco estándar.
ms.assetid: a69ba953-cd5c-487f-b9e0-dbd6c44b88b8
title: Escribir en mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13c31fd6b24217267b394f80c2dcdf551b6949f8692811173021fb78326f2f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359315"
---
# <a name="writing-to-a-mailslot"></a>Escribir en mailslot

Escribir en un mailslot es similar a escribir en un archivo de disco estándar. El código siguiente usa las [**funciones CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)y [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para colocar un mensaje corto en un mailslot. El mensaje se difunde al servidor mailslot denominado \_ "mailslot de ejemplo" en el equipo local. El código funciona bajo la suposición de que el servidor mailslot ya se ha creado.


```C++
#include <windows.h>
#include <stdio.h>

LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WriteSlot(HANDLE hSlot, LPCTSTR lpszMessage)
{
   BOOL fResult; 
   DWORD cbWritten; 
 
   fResult = WriteFile(hSlot, 
     lpszMessage, 
     (DWORD) (lstrlen(lpszMessage)+1)*sizeof(TCHAR),  
     &cbWritten, 
     (LPOVERLAPPED) NULL); 
 
   if (!fResult) 
   { 
      printf("WriteFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   printf("Slot written to successfully.\n"); 

   return TRUE;
}

int main()
{ 
   HANDLE hFile; 

   hFile = CreateFile(SlotName, 
     GENERIC_WRITE, 
     FILE_SHARE_READ,
     (LPSECURITY_ATTRIBUTES) NULL, 
     OPEN_EXISTING, 
     FILE_ATTRIBUTE_NORMAL, 
     (HANDLE) NULL); 
 
   if (hFile == INVALID_HANDLE_VALUE) 
   { 
      printf("CreateFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   WriteSlot(hFile, TEXT("Message one for mailslot."));
   WriteSlot(hFile, TEXT("Message two for mailslot."));

   Sleep(5000);

   WriteSlot(hFile, TEXT("Message three for mailslot."));
 
   CloseHandle(hFile); 
 
   return TRUE;
}
```



A continuación se muestra la salida que se muestra cuando se ejecuta este ejemplo con el servidor mailslot que se muestra en [Reading from a Mailslot](reading-from-a-mailslot.md).

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
