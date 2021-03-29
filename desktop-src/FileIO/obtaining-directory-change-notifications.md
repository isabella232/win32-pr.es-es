---
description: Una aplicación puede supervisar el contenido de un directorio y sus subdirectorios mediante notificaciones de cambios.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Obtención de notificaciones de cambio de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44375c334c3630aee09bf4a13fc23f87cc91e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811323"
---
# <a name="obtaining-directory-change-notifications"></a><span data-ttu-id="13256-103">Obtención de notificaciones de cambio de directorio</span><span class="sxs-lookup"><span data-stu-id="13256-103">Obtaining Directory Change Notifications</span></span>

<span data-ttu-id="13256-104">Una aplicación puede supervisar el contenido de un directorio y sus subdirectorios mediante notificaciones de cambios.</span><span class="sxs-lookup"><span data-stu-id="13256-104">An application can monitor the contents of a directory and its subdirectories by using change notifications.</span></span> <span data-ttu-id="13256-105">Esperar una notificación de cambio es similar a tener una operación de lectura pendiente en un directorio y, si es necesario, sus subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="13256-105">Waiting for a change notification is similar to having a read operation pending against a directory and, if necessary, its subdirectories.</span></span> <span data-ttu-id="13256-106">Cuando algo cambia dentro del directorio que se está inspeccionando, se completa la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="13256-106">When something changes within the directory being watched, the read operation is completed.</span></span> <span data-ttu-id="13256-107">Por ejemplo, una aplicación puede utilizar estas funciones para actualizar una lista de directorios cada vez que cambia un nombre de archivo dentro del directorio supervisado.</span><span class="sxs-lookup"><span data-stu-id="13256-107">For example, an application can use these functions to update a directory listing whenever a file name within the monitored directory changes.</span></span>

<span data-ttu-id="13256-108">Una aplicación puede especificar un conjunto de condiciones que desencadenan una notificación de cambio mediante la función [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="13256-108">An application can specify a set of conditions that trigger a change notification by using the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function.</span></span> <span data-ttu-id="13256-109">Entre las condiciones se incluyen los cambios en los nombres de archivo, los nombres de directorio, los atributos, el tamaño de archivo, la hora de la última escritura y la seguridad.</span><span class="sxs-lookup"><span data-stu-id="13256-109">The conditions include changes to file names, directory names, attributes, file size, time of last write, and security.</span></span> <span data-ttu-id="13256-110">Esta función también devuelve un identificador que se puede esperar mediante las funciones de [espera](/windows/desktop/Sync/wait-functions).</span><span class="sxs-lookup"><span data-stu-id="13256-110">This function also returns a handle that can be waited on by using the [wait functions](/windows/desktop/Sync/wait-functions).</span></span> <span data-ttu-id="13256-111">Si se cumple la condición de espera, se puede usar [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) para proporcionar un identificador de notificación que espere en los cambios posteriores.</span><span class="sxs-lookup"><span data-stu-id="13256-111">If the wait condition is satisfied, [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) can be used to provide a notification handle to wait on subsequent changes.</span></span> <span data-ttu-id="13256-112">Sin embargo, estas funciones no indican el cambio real que cumplía la condición de espera.</span><span class="sxs-lookup"><span data-stu-id="13256-112">However, these functions do not indicate the actual change that satisfied the wait condition.</span></span>

<span data-ttu-id="13256-113">Use [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) para cerrar el identificador de notificación.</span><span class="sxs-lookup"><span data-stu-id="13256-113">Use [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) to close the notification handle.</span></span>

<span data-ttu-id="13256-114">Para recuperar información sobre el cambio específico como parte de la notificación, utilice la función [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) .</span><span class="sxs-lookup"><span data-stu-id="13256-114">To retrieve information about the specific change as part of the notification, use the [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) function.</span></span> <span data-ttu-id="13256-115">Esta función también le permite proporcionar una rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="13256-115">This function also enables you to provide a completion routine.</span></span>

<span data-ttu-id="13256-116">Para realizar el seguimiento de los cambios en un volumen, consulte [cambiar diarios](change-journals.md).</span><span class="sxs-lookup"><span data-stu-id="13256-116">To track changes on a volume, see [change journals](change-journals.md).</span></span>

<span data-ttu-id="13256-117">En el siguiente ejemplo se supervisa el árbol de directorios para los cambios de nombre de directorio.</span><span class="sxs-lookup"><span data-stu-id="13256-117">The following example monitors the directory tree for directory name changes.</span></span> <span data-ttu-id="13256-118">También supervisa los cambios de nombre de archivo de un directorio.</span><span class="sxs-lookup"><span data-stu-id="13256-118">It also monitors a directory for file name changes.</span></span> <span data-ttu-id="13256-119">En el ejemplo se usa la función [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) para crear dos identificadores de notificación y la función [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) para esperar en los identificadores.</span><span class="sxs-lookup"><span data-stu-id="13256-119">The example uses the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function to create two notification handles and the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to wait on the handles.</span></span> <span data-ttu-id="13256-120">Cada vez que se crea o se elimina un directorio en el árbol, el ejemplo debe actualizar todo el árbol de directorios.</span><span class="sxs-lookup"><span data-stu-id="13256-120">Whenever a directory is created or deleted in the tree, the example should update the entire directory tree.</span></span> <span data-ttu-id="13256-121">Cada vez que se crea o se elimina un archivo en el directorio, el ejemplo debe actualizar el directorio.</span><span class="sxs-lookup"><span data-stu-id="13256-121">Whenever a file is created or deleted in the directory, the example should refresh the directory.</span></span>

> [!Note]
>
> <span data-ttu-id="13256-122">En este sencillo ejemplo se usa la función [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) para finalizar y limpiar, pero las aplicaciones más complejas siempre deben usar la administración de recursos adecuada, como [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="13256-122">This simplistic example uses the [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) function for termination and cleanup, but more complex applications should always use proper resource management such as [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) where appropriate.</span></span>

 


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



 

 
