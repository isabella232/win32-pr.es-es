---
title: Determinar la ubicación de un recurso compartido
description: En el ejemplo siguiente se muestra cómo llamar a la función WNetGetUniversalName para determinar la ubicación de un recurso compartido en una unidad redirigida.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995461"
---
# <a name="determining-the-location-of-a-share"></a>Determinar la ubicación de un recurso compartido

En el ejemplo siguiente se muestra cómo llamar a la función [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) para determinar la ubicación de un recurso compartido en una unidad redirigida.

En primer lugar, el ejemplo de código llama a la función **WNetGetUniversalName** , especificando el nivel de información del [**nombre universal para recuperar un puntero a una cadena \_ \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) de nombre UNC (Convención de nomenclatura universal) para el recurso. Después, el ejemplo llama a **WNetGetUniversalName** por segunda vez, especificando el nivel de información del [**nombre remoto para recuperar dos cadenas \_ \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) de información de conexión de red adicionales. Si las llamadas se realizan correctamente, el ejemplo imprime la ubicación del recurso compartido.

Para probar el siguiente ejemplo de código, realice los pasos siguientes:

1.  Asigne al código el nombre GetUni. cpp.
2.  Agregue el ejemplo a una aplicación de consola denominada GetUni.
3.  Vincule las bibliotecas shell32. lib, MPR. lib y NetApi32. lib a la lista de bibliotecas del compilador.
4.  En el símbolo del sistema, cambie al directorio GetUni
5.  Compile GetUni. cpp.
6.  Ejecute el archivo GetUni.exe seguido de una letra de unidad y dos puntos, como en este ejemplo:

    **GetUni H:\\**


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 