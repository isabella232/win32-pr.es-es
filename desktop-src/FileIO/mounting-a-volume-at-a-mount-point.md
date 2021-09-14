---
description: Cómo crear una carpeta montada.
ms.assetid: c97bfd10-66ff-41e1-ba3b-f98a019948d5
title: Creación de una carpeta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8a16c4a8c06ae22fa7faf2c2b0a2e8cdfc38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069906"
---
# <a name="creating-a-mounted-folder"></a>Creación de una carpeta montada

En el ejemplo siguiente se muestra cómo crear una carpeta montada. Para obtener más información, vea [Crear carpetas montadas.](mounting-and-dismounting-a-volume.md)

En este ejemplo se usan las siguientes funciones: [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) y [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa).


```C++
#define _WIN32_WINNT 0x0501

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE MAX_PATH 

int _tmain( int argc, TCHAR *argv[] )
{
   BOOL bFlag;
   TCHAR Buf[BUFSIZE];     // temporary buffer for volume name

   if( argc != 3 ) 
   {
      _tprintf( TEXT("Usage: %s <mount_point> <volume>\n"), argv[0] );
      _tprintf( TEXT("For example, \"%s c:\\mnt\\fdrive\\ f:\\\"\n"), argv[0]);
      return( -1 );
   }

  // We should do some error checking on the inputs. Make sure there 
  // are colons and backslashes in the right places, and so on 

   bFlag = GetVolumeNameForVolumeMountPoint(
              argv[2], // input volume mount point or directory
                  Buf, // output volume name buffer
              BUFSIZE  // size of volume name buffer
           );

   if (bFlag != TRUE) 
   {
      _tprintf( TEXT("Retrieving volume name for %s failed.\n"), argv[2] );
      return (-2);
   }

   _tprintf( TEXT("Volume name of %s is %s\n"), argv[2], Buf );
   bFlag = SetVolumeMountPoint(
              argv[1], // mount point
                  Buf  // volume to be mounted
           );

   if (!bFlag)
     _tprintf (TEXT("Attempt to mount %s at %s failed.\n"), argv[2], argv[1]);

   return (bFlag);
}
```



 

 



