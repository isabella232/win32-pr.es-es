---
title: Recuperación de información sobre un recurso de red
description: Para identificar el proveedor de red que posee un recurso, una aplicación puede llamar a la función WNetGetResourceInformation, como se muestra en el ejemplo de código siguiente.
ms.assetid: 4bddb55c-181d-4c6f-bd92-9c27d6b894bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf21e48be540f5307fc1ebd2359aea7ff03cbe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149437"
---
# <a name="retrieving-information-about-a-network-resource"></a>Recuperación de información sobre un recurso de red

Para identificar el proveedor de red que posee un recurso, una aplicación puede llamar a la función [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , como se muestra en el ejemplo de código siguiente.

El ejemplo siguiente es una función (CheckServer) que toma un nombre de servidor como parámetro y devuelve información sobre ese servidor. En primer lugar, la función llama a la función [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) para inicializar el contenido de un bloque de memoria en cero. Después, el ejemplo llama a la función [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , especificando un búfer lo suficientemente grande como para contener solo una estructura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) . La rutina incluye el procesamiento de errores para controlar el caso cuando un búfer de este tamaño es insuficiente para contener las cadenas de longitud variable a las que pertenecen los miembros del punto de la estructura **NETRESOURCE** . Si se produce este error, el ejemplo asigna memoria suficiente y llama de nuevo a **WNetGetResourceInformation** . Por último, el ejemplo libera la memoria asignada.

Tenga en cuenta que en el ejemplo se da por supuesto que el parámetro *pszServer* apunta a un nombre de servidor que reconoce uno de los proveedores de red del equipo local.


```C++
#include <Windows.h>
#include <Winnetwk.h >

// Need to link with Mpr.lib
#pragma comment(lib, "Mpr.lib")
//
// Verify a server on the network. 
//
DWORD
CheckServer( LPTSTR pszServer )
{  
    DWORD dwBufferSize = sizeof(NETRESOURCE);
    LPBYTE lpBuffer;                  // buffer
    NETRESOURCE nr;
    LPTSTR pszSystem = NULL;          // variable-length strings

    //
    // Set the block of memory to zero; then initialize
    // the NETRESOURCE structure. 
    //
    ZeroMemory(&nr, sizeof(nr));

    nr.dwScope       = RESOURCE_GLOBALNET;
    nr.dwType        = RESOURCETYPE_ANY;
    nr.lpRemoteName  = pszServer;

    //
    // First call the WNetGetResourceInformation function with 
    // memory allocated to hold only a NETRESOURCE structure. This 
    // method can succeed if all the NETRESOURCE pointers are NULL.
    // If the call fails because the buffer is too small, allocate
    // a larger buffer.
    //
    lpBuffer = (LPBYTE) malloc( dwBufferSize );
    if (lpBuffer == NULL) 
        return FALSE;

    while ( WNetGetResourceInformation(&nr, lpBuffer, &dwBufferSize, 
                &pszSystem) == ERROR_MORE_DATA)
    {
        lpBuffer = (LPBYTE) realloc(lpBuffer, dwBufferSize);
    }

    // Process the contents of the NETRESOURCE structure and the
    // variable-length strings in lpBuffer and set dwValue. When
    // finished, free the memory.

    free(lpBuffer);

    return TRUE;
}
```



 

 