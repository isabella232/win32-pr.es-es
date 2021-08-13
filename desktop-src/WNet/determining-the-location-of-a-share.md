---
title: Determinar la ubicación de un recurso compartido
description: En el ejemplo siguiente se muestra cómo llamar a la función WNetGetUniversalName para determinar la ubicación de un recurso compartido en una unidad redirigida.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a881d452c6aa9eac5eea85d4ef0e9ddce83524f001294d2a6d6d6307f5ff1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566898"
---
# <a name="determining-the-location-of-a-share"></a>Determinar la ubicación de un recurso compartido

En el ejemplo siguiente se muestra cómo llamar a la función [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) para determinar la ubicación de un recurso compartido en una unidad redirigida.

En primer lugar, el ejemplo de código llama a la función **WNetGetUniversalName** y especifica el nivel de información [**DE \_ \_ INFORMACIÓN**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) DE NOMBRE UNIVERSAL para recuperar un puntero a una cadena de nombre de convención de nomenclatura universal (UNC) para el recurso. A continuación, el ejemplo llama a **WNetGetUniversalName** una segunda vez, especificando el nivel de información [**REMOTE NAME \_ \_ INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) para recuperar dos cadenas de información de conexión de red adicionales. Si las llamadas son correctas, el ejemplo imprime la ubicación del recurso compartido.

Para probar el ejemplo de código siguiente, realice los pasos siguientes:

1.  Asigne al ejemplo de código el nombre GetUni.cpp.
2.  Agregue el ejemplo a una aplicación de consola denominada GetUni.
3.  Vincule las bibliotecas Shell32.lib, Mpr.lib y NetApi32.lib a la lista de bibliotecas del compilador.
4.  En el símbolo del sistema, cambie al directorio GetUni.
5.  Compile GetUni.cpp.
6.  Ejecute el archivo GetUni.exe seguido de una letra de unidad y dos puntos, de la siguiente manera:

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



 

 