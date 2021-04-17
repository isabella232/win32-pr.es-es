---
description: Cómo obtener una ruta de acceso de GUID de volumen para cada volumen local asociado a una letra de unidad que esté actualmente en uso en el equipo.
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: Enumerar rutas de acceso de GUID de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e363369d3ea26abb054c8b9321c0147ace7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667698"
---
# <a name="enumerating-volume-guid-paths"></a>Enumerar rutas de acceso de GUID de volumen

En el ejemplo de código de este tema se muestra cómo obtener una ruta de acceso de **GUID** de volumen para cada volumen local asociado a una letra de unidad que está actualmente en uso en el equipo.

En el ejemplo de código se usa la función [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH 

void main(void)
 {
  BOOL bFlag;
  TCHAR Buf[BUFSIZE];           // temporary buffer for volume name
  TCHAR Drive[] = TEXT("c:\\"); // template drive specifier
  TCHAR I;                      // generic loop counter

  // Walk through legal drive letters, skipping floppies.
  for (I = TEXT('c'); I < TEXT('z');  I++ ) 
   {
    // Stamp the drive for the appropriate letter.
    Drive[0] = I;

    bFlag = GetVolumeNameForVolumeMountPoint(
                Drive,     // input volume mount point or directory
                Buf,       // output volume name buffer
                BUFSIZE ); // size of volume name buffer

    if (bFlag) 
     {
      _tprintf (TEXT("The ID of drive \"%s\" is \"%s\"\n"), Drive, Buf);
     }
   }
 }
```



Para obtener un ejemplo en el que se enumeran todos los volúmenes conectados localmente y se muestra la ruta de acceso del dispositivo, la ruta de acceso del **GUID** del volumen y las rutas de acceso montadas (incluidas las letras de unidad), consulte [Mostrar rutas](displaying-volume-paths.md)de

 

 



