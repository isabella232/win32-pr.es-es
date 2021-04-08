---
description: Monitor de red usa la función de exportación de DllMain para identificar la existencia del analizador y liberar recursos que Monitor de red utiliza para almacenar información sobre el analizador.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementar el analizador de DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808689"
---
# <a name="implementing-dllmain-parser"></a>Implementar el analizador de DllMain

Monitor de red usa la función de exportación de **DllMain** para identificar la existencia del analizador y liberar recursos que monitor de red utiliza para almacenar información sobre el analizador.

Cuando Monitor de red llama a **DllMain** por primera vez, el archivo DLL del analizador llama a [**CreateProtocol**](createprotocol.md) para hacer lo siguiente:

-   Especifique el protocolo que detecta el analizador.
-   Proporcione puntos de entrada para las funciones de exportación de analizador restantes que Monitor de red llamadas.

Cuando Monitor de red llama a **DllMain** por última vez, **DllMain** llama a [**DestroyProtocol**](destroyprotocol.md) para liberar todos los recursos que monitor de red utiliza para almacenar información sobre el analizador.

En el procedimiento siguiente se identifican los pasos necesarios para implementar **DllMain**.

**Para implementar DllMain**

1.  Especifique la estructura [**ENTRYPOINTS**](entrypoints.md) para la función [**CreateProtocol**](createprotocol.md) y la variable de conexión global. La variable Attach se usa para realizar el seguimiento del número de instancias de protocolo que se están ejecutando.
2.  Observe el valor del parámetro de *comando* que establece el sistema operativo.

    Si el parámetro de *comando* se establece en la Asociación de proceso de dll \_ y Attach \_ es 0, llame a [**CreateProtocol**](createprotocol.md) para proporcionar el nombre del protocolo y los puntos de entrada para las siguientes funciones de exportación.

    -   **Registro**
    -   **Eliminar registro**
    -   **RecognizeFrame**
    -   **AttachProperties**
    -   **FormatProperties** (solo es necesario si monitor de red mostrarán las propiedades del Protocolo).

    Si el parámetro de *comando* se establece en \_ la \_ desasociación de proceso de dll y Attach es 0, llame a [**DestroyProtocol**](destroyprotocol.md) con el identificador de instancia que devuelve [**CreateProtocol**](createprotocol.md) .

3.  Devuelve **true** porque la función del analizador **DllMain** siempre debe devolver **true**.

La siguiente es una implementación básica de **DllMain**. En el ejemplo de código se usa una instrucción Case para capturar valores del parámetro de *comando* con el fin de determinar si se debe llamar a [**CreateProtocol**](createprotocol.md) o [**DestroyProtocol**](destroyprotocol.md) .

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

 

 



