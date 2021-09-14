---
description: Monitor de red utiliza la función de exportación DllMain para identificar la existencia del analizador y liberar recursos que Monitor de red usa para almacenar información sobre el analizador.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementación de DllMain Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069334"
---
# <a name="implementing-dllmain-parser"></a>Implementación de DllMain Parser

Monitor de red la función de exportación **DllMain** para identificar la existencia del analizador y liberar recursos que Monitor de red usa para almacenar información sobre el analizador.

Cuando Monitor de red a **DllMain** por primera vez, el archivo DLL del analizador llama a [**CreateProtocol**](createprotocol.md) para hacer lo siguiente:

-   Especifique el protocolo que detecta el analizador.
-   Proporcione puntos de entrada para las funciones de exportación restantes del analizador que Monitor de red llamadas.

Cuando Monitor de red **a DllMain** por última vez, **DllMain** llama a [**DestroyProtocol**](destroyprotocol.md) para liberar todos los recursos que Monitor de red usa para almacenar información sobre el analizador.

El procedimiento siguiente identifica los pasos necesarios para implementar **DllMain**.

**Para implementar DllMain**

1.  Especifique la [**estructura ENTRYPOINTS**](entrypoints.md) para la [**función CreateProtocol**](createprotocol.md) y la variable attach global. La variable Attach se usa para realizar un seguimiento del número de instancias de protocolo que se están ejecutando.
2.  Mire el valor del parámetro *Command* que establece el sistema operativo.

    Si el *parámetro Command* está establecido en DLL PROCESS ATTACH y Attach es 0, llame a \_ \_ [**CreateProtocol**](createprotocol.md) para proporcionar el nombre de protocolo y los puntos de entrada para las siguientes funciones de exportación.

    -   **Registro**
    -   **Eliminar registro**
    -   **RecognizeFrame**
    -   **AttachProperties**
    -   **FormatProperties** (solo es necesario si Monitor de red mostrará las propiedades del protocolo).

    Si el *parámetro Command* está establecido en DLL PROCESS DETACH y Attach es 0, llame a DestroyProtocol mediante el identificador de instancia que \_ devuelve \_ [**CreateProtocol.**](createprotocol.md) [](destroyprotocol.md)

3.  Devuelve **TRUE** porque la función del analizador **DllMain** siempre debe devolver **TRUE.**

A continuación se muestra una implementación básica de **DllMain**. En el ejemplo de código se usa una instrucción case para capturar los valores del parámetro *Command* para determinar si se debe llamar a [**CreateProtocol**](createprotocol.md) o [**DestroyProtocol.**](destroyprotocol.md)

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



