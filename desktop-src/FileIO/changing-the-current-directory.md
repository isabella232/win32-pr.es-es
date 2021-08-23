---
description: Una aplicación puede cambiar el directorio actual llamando a la función SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Cambiar el directorio actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf742c872bab7d37e115afa815fff961d2f975bfbd3db75ff61a5e992d64a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632115"
---
# <a name="changing-the-current-directory"></a>Cambiar el directorio actual

El directorio al final de la ruta de acceso activa se denomina directorio actual; es el directorio en el que se inició la aplicación activa, a menos que se haya cambiado explícitamente. Una aplicación puede determinar qué directorio está actual llamando a la [**función GetCurrentDirectory.**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) A veces es necesario usar la [**función GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) para asegurarse de que la letra de unidad se incluye si la aplicación lo requiere.

> [!Note]  
> Aunque cada proceso solo puede tener un directorio actual, si la aplicación cambia los volúmenes mediante la función [**SetCurrentDirectory,**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) el sistema recuerda la última ruta de acceso actual para cada volumen (letra de unidad). Este comportamiento se manifesta solo cuando se especifica una letra de unidad sin una ruta de acceso completa al cambiar el punto de referencia del directorio actual a otro volumen. Esto se aplica a las operaciones Get o Set.

 

Una aplicación puede cambiar el directorio actual llamando a la [**función SetCurrentDirectory.**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)

En el ejemplo siguiente se muestra el uso de [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) y [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).


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



 

 



