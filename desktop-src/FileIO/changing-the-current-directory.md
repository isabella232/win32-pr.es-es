---
description: Una aplicación puede cambiar el directorio actual llamando a la función SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Cambiar el directorio actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e507d206bcd988a7c00f557bde2b8a0ad39c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688729"
---
# <a name="changing-the-current-directory"></a><span data-ttu-id="0a49c-103">Cambiar el directorio actual</span><span class="sxs-lookup"><span data-stu-id="0a49c-103">Changing the Current Directory</span></span>

<span data-ttu-id="0a49c-104">El directorio situado al final de la ruta de acceso activa se denomina directorio actual. es el directorio en el que se inició la aplicación activa, a menos que se haya cambiado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="0a49c-104">The directory at the end of the active path is called the current directory; it is the directory in which the active application started, unless it has been explicitly changed.</span></span> <span data-ttu-id="0a49c-105">Una aplicación puede determinar qué directorio está actualizado mediante una llamada a la función [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="0a49c-105">An application can determine which directory is current by calling the [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) function.</span></span> <span data-ttu-id="0a49c-106">A veces es necesario usar la función [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) para asegurarse de que la letra de unidad se incluye en caso de que la aplicación lo requiera.</span><span class="sxs-lookup"><span data-stu-id="0a49c-106">It is sometimes necessary to use the [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) function to ensure the drive letter is included if the application requires it.</span></span>

> [!Note]  
> <span data-ttu-id="0a49c-107">Aunque cada proceso solo puede tener un directorio actual, si la aplicación cambia los volúmenes mediante la función [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , el sistema recuerda la última ruta de acceso actual de cada volumen (letra de unidad).</span><span class="sxs-lookup"><span data-stu-id="0a49c-107">Although each process can have only one current directory, if the application switches volumes by using the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function, the system remembers the last current path for each volume (drive letter).</span></span> <span data-ttu-id="0a49c-108">Este comportamiento solo se manifestará cuando se especifica una letra de unidad sin una ruta de acceso completa al cambiar el punto de directorio actual de referencia a un volumen diferente.</span><span class="sxs-lookup"><span data-stu-id="0a49c-108">This behavior will manifest itself only when specifying a drive letter without a fully qualified path when changing the current directory point of reference to a different volume.</span></span> <span data-ttu-id="0a49c-109">Esto se aplica a las operaciones GET o set.</span><span class="sxs-lookup"><span data-stu-id="0a49c-109">This applies to either Get or Set operations.</span></span>

 

<span data-ttu-id="0a49c-110">Una aplicación puede cambiar el directorio actual llamando a la función [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="0a49c-110">An application can change the current directory by calling the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function.</span></span>

<span data-ttu-id="0a49c-111">En el ejemplo siguiente se muestra el uso de [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) y [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span><span class="sxs-lookup"><span data-stu-id="0a49c-111">The following example demonstrates the use of [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) and [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH
 
void _tmain(int argc, TCHAR **argv) 
{ 
   TCHAR Buffer[BUFSIZE];
   DWORD dwRet;

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }

   dwRet = GetCurrentDirectory(BUFSIZE, Buffer);

   if( dwRet == 0 )
   {
      printf("GetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   if(dwRet > BUFSIZE)
   {
      printf("Buffer too small; need %d characters\n", dwRet);
      return;
   }

   if( !SetCurrentDirectory(argv[1]))
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Set current directory to %s\n"), argv[1]);

   if( !SetCurrentDirectory(Buffer) )
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Restored previous directory (%s)\n"), Buffer);
}
```



 

 



