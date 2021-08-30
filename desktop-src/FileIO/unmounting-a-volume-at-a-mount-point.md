---
description: Cómo eliminar una carpeta montada mediante la función DeleteVolumeMountPoint.
ms.assetid: 33049110-acf8-4db5-a9c4-bd4a884c8590
title: Eliminación de una carpeta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a972e17decd2e923a2f789e1dd9156a07c2301d1ccecdaf55778b364b834cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047755"
---
# <a name="deleting-a-mounted-folder"></a>Eliminación de una carpeta montada

En el ejemplo de código de este tema se muestra cómo eliminar una carpeta montada mediante la [**función DeleteVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) Para obtener más información, vea [Crear carpetas montadas.](mounting-and-dismounting-a-volume.md)


```C++
#define _WIN32_WINNT 0x0501

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void
Syntax (TCHAR *argv)
{
   _tprintf(TEXT("%s unmounts a volume from a volume mount point\n"), 
          argv);
   _tprintf(TEXT("For example: \"%s c:\\mnt\\fdrive\\\"\n"), argv);
}

int _tmain(int argc, TCHAR *argv[])
{
   BOOL bFlag;

   if (argc != 2)
   {
      Syntax (argv[0]);
      return (-1);
   }

// We should do some error checking on the path argument, such as
// ensuring that there is a trailing backslash.

   bFlag = DeleteVolumeMountPoint(
              argv[1] // Path of the volume mount point
           );

   _tprintf(TEXT("\n%s %s in unmounting the volume at %s\n"), argv[0],
           bFlag ? TEXT("succeeded") : TEXT("failed"), argv[1]);

   return (bFlag);
}
```



 

 



