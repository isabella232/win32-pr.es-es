---
title: Enumeración de recursos de red
description: En el ejemplo siguiente se muestra una función definida por la aplicación (EnumerateFunc) que enumera todos los recursos de una red.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313e679746b09603d2514b418abf281fefa9bc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568196"
---
# <a name="enumerating-network-resources"></a>Enumeración de recursos de red

En el ejemplo siguiente se muestra una función definida por la aplicación (EnumerateFunc) que enumera todos los recursos de una red. El ejemplo especifica **NULL para el** puntero a la estructura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) porque cuando [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) recibe un puntero **NULL,** recupera un identificador a la raíz de la red.

Para comenzar la enumeración de un recurso de contenedor de red, la aplicación debe realizar los pasos siguientes:

1.  Pase la dirección de una [**estructura NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) que representa el recurso a la [**función WNetOpenEnum.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)
2.  Asigne un búfer lo suficientemente grande como para contener la matriz de estructuras [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) que devuelve la función [**WNetEnumResource,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) además de las cadenas a las que apuntan sus miembros.
3.  Pase el identificador de recursos devuelto [**por WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) a la [**función WNetEnumResource.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)
4.  Cierre el identificador de recursos cuando ya no sea necesario llamando a la [**función WNetCloseEnum.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)

Puede continuar enumerando un recurso de contenedor descrito en la matriz de estructuras [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperadas por [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea). Si el **miembro dwUsage** de la estructura **NETRESOURCE** es igual a RESOURCEUSAGE CONTAINER, pase la dirección de la estructura a la función \_ [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para abrir el contenedor y continuar con la enumeración. Si **dwUsage** es igual a RESOURCEUSAGE CONNECTABLE, la aplicación puede pasar la dirección de la estructura a la función \_ [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o a la función [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) para conectarse al recurso.

En primer lugar, el ejemplo llama [**a la función WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para comenzar la enumeración. El ejemplo llama a la [**función GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) para asignar el búfer necesario y, a continuación, llama a la [**función ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) para establecer el contenido del búfer en cero. A continuación, el ejemplo llama [**a la función WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) para continuar con la enumeración . Siempre que el **miembro dwUsage** de una estructura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperada por **WNetEnumResource** sea igual a RESOURCEUSAGE CONTAINER, la función EnumerateFunc se llama a sí misma de forma recursiva y usa un puntero a esa estructura en su llamada \_ a **WNetOpenEnum.** Por último, el ejemplo llama a la [**función GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) para liberar la memoria asignada y [**a WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) para finalizar la enumeración.


```C++
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr);
void DisplayStruct(int i, LPNETRESOURCE lpnrLocal);

int main()
{

    LPNETRESOURCE lpnr = NULL;

    if (EnumerateFunc(lpnr) == FALSE) {
        printf("Call to EnumerateFunc failed\n");
        return 1;
    } else
        return 0;

}

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr)
{
    DWORD dwResult, dwResultEnum;
    HANDLE hEnum;
    DWORD cbBuffer = 16384;     // 16K is a good size
    DWORD cEntries = -1;        // enumerate all possible entries
    LPNETRESOURCE lpnrLocal;    // pointer to enumerated structures
    DWORD i;
    //
    // Call the WNetOpenEnum function to begin the enumeration.
    //
    dwResult = WNetOpenEnum(RESOURCE_GLOBALNET, // all network resources
                            RESOURCETYPE_ANY,   // all resources
                            0,  // enumerate all resources
                            lpnr,       // NULL first time the function is called
                            &hEnum);    // handle to the resource

    if (dwResult != NO_ERROR) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
        return FALSE;
    }
    //
    // Call the GlobalAlloc function to allocate resources.
    //
    lpnrLocal = (LPNETRESOURCE) GlobalAlloc(GPTR, cbBuffer);
    if (lpnrLocal == NULL) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
//      NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetOpenEnum");
        return FALSE;
    }

    do {
        //
        // Initialize the buffer.
        //
        ZeroMemory(lpnrLocal, cbBuffer);
        //
        // Call the WNetEnumResource function to continue
        //  the enumeration.
        //
        dwResultEnum = WNetEnumResource(hEnum,  // resource handle
                                        &cEntries,      // defined locally as -1
                                        lpnrLocal,      // LPNETRESOURCE
                                        &cbBuffer);     // buffer size
        //
        // If the call succeeds, loop through the structures.
        //
        if (dwResultEnum == NO_ERROR) {
            for (i = 0; i < cEntries; i++) {
                // Call an application-defined function to
                //  display the contents of the NETRESOURCE structures.
                //
                DisplayStruct(i, &lpnrLocal[i]);

                // If the NETRESOURCE structure represents a container resource, 
                //  call the EnumerateFunc function recursively.

                if (RESOURCEUSAGE_CONTAINER == (lpnrLocal[i].dwUsage
                                                & RESOURCEUSAGE_CONTAINER))
//          if(!EnumerateFunc(hwnd, hdc, &lpnrLocal[i]))
                    if (!EnumerateFunc(&lpnrLocal[i]))
                        printf("EnumerateFunc returned FALSE\n");
//            TextOut(hdc, 10, 10, "EnumerateFunc returned FALSE.", 29);
            }
        }
        // Process errors.
        //
        else if (dwResultEnum != ERROR_NO_MORE_ITEMS) {
            printf("WNetEnumResource failed with error %d\n", dwResultEnum);

//      NetErrorHandler(hwnd, dwResultEnum, (LPSTR)"WNetEnumResource");
            break;
        }
    }
    //
    // End do.
    //
    while (dwResultEnum != ERROR_NO_MORE_ITEMS);
    //
    // Call the GlobalFree function to free the memory.
    //
    GlobalFree((HGLOBAL) lpnrLocal);
    //
    // Call WNetCloseEnum to end the enumeration.
    //
    dwResult = WNetCloseEnum(hEnum);

    if (dwResult != NO_ERROR) {
        //
        // Process errors.
        //
        printf("WNetCloseEnum failed with error %d\n", dwResult);
//    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetCloseEnum");
        return FALSE;
    }

    return TRUE;
}

void DisplayStruct(int i, LPNETRESOURCE lpnrLocal)
{
    printf("NETRESOURCE[%d] Scope: ", i);
    switch (lpnrLocal->dwScope) {
    case (RESOURCE_CONNECTED):
        printf("connected\n");
        break;
    case (RESOURCE_GLOBALNET):
        printf("all resources\n");
        break;
    case (RESOURCE_REMEMBERED):
        printf("remembered\n");
        break;
    default:
        printf("unknown scope %d\n", lpnrLocal->dwScope);
        break;
    }

    printf("NETRESOURCE[%d] Type: ", i);
    switch (lpnrLocal->dwType) {
    case (RESOURCETYPE_ANY):
        printf("any\n");
        break;
    case (RESOURCETYPE_DISK):
        printf("disk\n");
        break;
    case (RESOURCETYPE_PRINT):
        printf("print\n");
        break;
    default:
        printf("unknown type %d\n", lpnrLocal->dwType);
        break;
    }

    printf("NETRESOURCE[%d] DisplayType: ", i);
    switch (lpnrLocal->dwDisplayType) {
    case (RESOURCEDISPLAYTYPE_GENERIC):
        printf("generic\n");
        break;
    case (RESOURCEDISPLAYTYPE_DOMAIN):
        printf("domain\n");
        break;
    case (RESOURCEDISPLAYTYPE_SERVER):
        printf("server\n");
        break;
    case (RESOURCEDISPLAYTYPE_SHARE):
        printf("share\n");
        break;
    case (RESOURCEDISPLAYTYPE_FILE):
        printf("file\n");
        break;
    case (RESOURCEDISPLAYTYPE_GROUP):
        printf("group\n");
        break;
    case (RESOURCEDISPLAYTYPE_NETWORK):
        printf("network\n");
        break;
    default:
        printf("unknown display type %d\n", lpnrLocal->dwDisplayType);
        break;
    }

    printf("NETRESOURCE[%d] Usage: 0x%x = ", i, lpnrLocal->dwUsage);
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONNECTABLE)
        printf("connectable ");
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONTAINER)
        printf("container ");
    printf("\n");

    printf("NETRESOURCE[%d] Localname: %S\n", i, lpnrLocal->lpLocalName);
    printf("NETRESOURCE[%d] Remotename: %S\n", i, lpnrLocal->lpRemoteName);
    printf("NETRESOURCE[%d] Comment: %S\n", i, lpnrLocal->lpComment);
    printf("NETRESOURCE[%d] Provider: %S\n", i, lpnrLocal->lpProvider);
    printf("\n");
}

```



Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, vea [Recuperación de errores de red.](retrieving-network-errors.md)

 

 