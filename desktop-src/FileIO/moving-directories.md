---
description: Para trasladar un directorio a otra ubicación, junto con los archivos y subdirectorios contenidos en él, llame a la función MoveFileEx, MoveFileWithProgress o MoveFileTransacted.
ms.assetid: ca56c109-d6a3-456e-956c-126ce4aee8ba
title: Mover directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56167f0831894350a044104bce1f41ef3c5770ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669864"
---
# <a name="moving-directories"></a><span data-ttu-id="40716-103">Mover directorios</span><span class="sxs-lookup"><span data-stu-id="40716-103">Moving Directories</span></span>

<span data-ttu-id="40716-104">Para trasladar un directorio a otra ubicación, junto con los archivos y subdirectorios contenidos en él, llame a la función [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)o [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) .</span><span class="sxs-lookup"><span data-stu-id="40716-104">To move a directory to another location, along with the files and subdirectories contained within it, call the [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa), or [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) function.</span></span> <span data-ttu-id="40716-105">La función [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa) tiene la misma funcionalidad que [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), salvo que **MoveFileWithProgress** permite especificar una rutina de devolución de llamada que recibe notificaciones sobre el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="40716-105">The [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa) function has the same functionality as [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), except that **MoveFileWithProgress** enables you to specify a callback routine that receives notifications on the progress of the operation.</span></span> <span data-ttu-id="40716-106">La función [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) permite realizar la operación como una operación de transacción.</span><span class="sxs-lookup"><span data-stu-id="40716-106">The [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) function enables you to perform the operation as a transacted operation.</span></span>

<span data-ttu-id="40716-107">En el ejemplo siguiente se muestra el uso de la función [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) con un directorio.</span><span class="sxs-lookup"><span data-stu-id="40716-107">The following example demonstrates the use of the [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) function with a directory.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    printf("\n");
    if( argc != 3 )
    {
        printf("ERROR:  Incorrect number of arguments\n\n");
        printf("Description:\n");
        printf("  Moves a directory and its contents\n\n");
        printf("Usage:\n");
        _tprintf(TEXT("  %s [source_dir] [target_dir]\n\n"), argv[0]);
        printf("  The target directory cannot exist already.\n\n");
        return;
    }

    // Move the source directory to the target directory location.
    // The target directory must be on the same drive as the source.
    // The target directory cannot already exist.

    if (!MoveFileEx(argv[1], argv[2], MOVEFILE_WRITE_THROUGH))
    { 
        printf ("MoveFileEx failed with error %d\n", GetLastError());
        return;
    }
    else _tprintf(TEXT("%s has been moved to %s\n"), argv[1], argv[2]);
}
```



 

 



