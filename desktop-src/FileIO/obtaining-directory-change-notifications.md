---
description: Una aplicación puede supervisar el contenido de un directorio y sus subdirectorios mediante notificaciones de cambio.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Obtención de notificaciones de cambio de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44375c334c3630aee09bf4a13fc23f87cc91e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069890"
---
# <a name="obtaining-directory-change-notifications"></a>Obtención de notificaciones de cambio de directorio

Una aplicación puede supervisar el contenido de un directorio y sus subdirectorios mediante notificaciones de cambio. Esperar una notificación de cambio es similar a tener una operación de lectura pendiente en un directorio y, si es necesario, sus subdirectorios. Cuando algo cambia dentro del directorio que se está observando, se completa la operación de lectura. Por ejemplo, una aplicación puede usar estas funciones para actualizar una lista de directorios cada vez que cambia un nombre de archivo dentro del directorio supervisado.

Una aplicación puede especificar un conjunto de condiciones que desencadenan una notificación de cambio mediante la [**función FindFirstChangeNotification.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) Las condiciones incluyen cambios en los nombres de archivo, los nombres de directorio, los atributos, el tamaño del archivo, la hora de la última escritura y la seguridad. Esta función también devuelve un identificador que se puede esperar mediante las funciones [de espera](/windows/desktop/Sync/wait-functions). Si se cumple la condición de espera, [**findNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) se puede usar para proporcionar un identificador de notificación para esperar los cambios posteriores. Sin embargo, estas funciones no indican el cambio real que satisface la condición de espera.

Use [**FindCloseChangeNotification para**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) cerrar el identificador de notificación.

Para recuperar información sobre el cambio específico como parte de la notificación, use la [**función ReadDirectoryChangesW.**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) Esta función también permite proporcionar una rutina de finalización.

Para realizar un seguimiento de los cambios en un volumen, consulte [los diarios de cambios](change-journals.md).

En el ejemplo siguiente se supervisa el árbol de directorios en busca de cambios en el nombre del directorio. También supervisa un directorio para ver si hay cambios en el nombre de archivo. En el ejemplo se [**usa la función FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) para crear dos identificadores de notificación y la [**función WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) para esperar en los identificadores. Cada vez que se crea o elimina un directorio en el árbol, el ejemplo debe actualizar todo el árbol de directorios. Cada vez que se crea o elimina un archivo en el directorio, en el ejemplo se debe actualizar el directorio.

> [!Note]
>
> En este ejemplo simplista se usa la función [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) para la terminación y la limpieza, pero las aplicaciones más complejas siempre deben usar la administración adecuada de recursos, como [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) cuando corresponda.

 


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>

void RefreshDirectory(LPTSTR);
void RefreshTree(LPTSTR);
void WatchDirectory(LPTSTR);

void _tmain(int argc, TCHAR *argv[])
{
    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
        return;
    }

    WatchDirectory(argv[1]);
}

void WatchDirectory(LPTSTR lpDir)
{
   DWORD dwWaitStatus; 
   HANDLE dwChangeHandles[2]; 
   TCHAR lpDrive[4];
   TCHAR lpFile[_MAX_FNAME];
   TCHAR lpExt[_MAX_EXT];

   _tsplitpath_s(lpDir, lpDrive, 4, NULL, 0, lpFile, _MAX_FNAME, lpExt, _MAX_EXT);

   lpDrive[2] = (TCHAR)'\\';
   lpDrive[3] = (TCHAR)'\0';
 
// Watch the directory for file creation and deletion. 
 
   dwChangeHandles[0] = FindFirstChangeNotification( 
      lpDir,                         // directory to watch 
      FALSE,                         // do not watch subtree 
      FILE_NOTIFY_CHANGE_FILE_NAME); // watch file name changes 
 
   if (dwChangeHandles[0] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 
// Watch the subtree for directory creation and deletion. 
 
   dwChangeHandles[1] = FindFirstChangeNotification( 
      lpDrive,                       // directory to watch 
      TRUE,                          // watch the subtree 
      FILE_NOTIFY_CHANGE_DIR_NAME);  // watch dir name changes 
 
   if (dwChangeHandles[1] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 

// Make a final validation check on our handles.

   if ((dwChangeHandles[0] == NULL) || (dwChangeHandles[1] == NULL))
   {
     printf("\n ERROR: Unexpected NULL from FindFirstChangeNotification.\n");
     ExitProcess(GetLastError()); 
   }

// Change notification is set. Now wait on both notification 
// handles and refresh accordingly. 
 
   while (TRUE) 
   { 
   // Wait for notification.
 
      printf("\nWaiting for notification...\n");

      dwWaitStatus = WaitForMultipleObjects(2, dwChangeHandles, 
         FALSE, INFINITE); 
 
      switch (dwWaitStatus) 
      { 
         case WAIT_OBJECT_0: 
 
         // A file was created, renamed, or deleted in the directory.
         // Refresh this directory and restart the notification.
 
             RefreshDirectory(lpDir); 
             if ( FindNextChangeNotification(dwChangeHandles[0]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_OBJECT_0 + 1: 
 
         // A directory was created, renamed, or deleted.
         // Refresh the tree and restart the notification.
 
             RefreshTree(lpDrive); 
             if (FindNextChangeNotification(dwChangeHandles[1]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_TIMEOUT:

         // A timeout occurred, this would happen if some value other 
         // than INFINITE is used in the Wait call and no changes occur.
         // In a single-threaded environment you might not want an
         // INFINITE wait.
 
            printf("\nNo changes in the timeout period.\n");
            break;

         default: 
            printf("\n ERROR: Unhandled dwWaitStatus.\n");
            ExitProcess(GetLastError());
            break;
      }
   }
}

void RefreshDirectory(LPTSTR lpDir)
{
   // This is where you might place code to refresh your
   // directory listing, but not the subtree because it
   // would not be necessary.

   _tprintf(TEXT("Directory (%s) changed.\n"), lpDir);
}

void RefreshTree(LPTSTR lpDrive)
{
   // This is where you might place code to refresh your
   // directory listing, including the subtree.

   _tprintf(TEXT("Directory tree (%s) changed.\n"), lpDrive);
}
```



 

 
