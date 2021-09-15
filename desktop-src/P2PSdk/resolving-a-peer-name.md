---
description: En este tema se de abordan los métodos para resolver un nombre del mismo nivel mediante las API del proveedor de espacios de nombres PNRP.
ms.assetid: 7b21ec52-bc29-447e-9c46-34b9115574e0
title: Resolución de un nombre de mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7f3aa59d3dc3be89f35ce9d6eca58bed1ce137
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473664"
---
# <a name="resolving-a-peer-name"></a>Resolución de un nombre de mismo nivel

En este tema se de abordan los métodos para resolver un nombre del mismo nivel mediante las API del proveedor de espacios de nombres PNRP.

Al resolver un nombre del mismo nivel, debe proporcionar la siguiente información:

-   [Nombre del mismo nivel](peer-names.md)
-   [Resolución de criterios](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)
-   Nombre de nube en el que se va a resolver el nombre del mismo nivel
-   Dirección IP, que es opcional y se usa como sugerencia

## <a name="resolving-a-peer-name"></a>Resolución de un nombre de mismo nivel

Después de proporcionar un nombre del mismo nivel, resolver criterios, nombre de nube y la dirección IP opcional, se deben realizar los pasos siguientes para completar la resolución de un nombre del mismo nivel:

-   Llame a [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) para comenzar el proceso y devolver un identificador.
-   Llame [**a WSALookupServiceNext para**](pnrp-and-wsalookupservicenext.md) resolver el nombre del mismo nivel.
-   Llame [**a WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) para completar el proceso.

## <a name="an-example-of-resolving-a-peer-name"></a>Un ejemplo de resolución de un nombre del mismo nivel

El siguiente fragmento de código muestra cómo resolver un nombre del mismo nivel. En el ejemplo se supone que se devolverá una dirección TCP/IP.


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment( lib, "ws2_32.lib")

// Function: PnrpResolve
//
// Purpose:  Resolve the given name within a PNRP cloud
//
// Arguments:
//   pwzName  : name to resolve in PNRP, generally the graph id
//   pwzCloud : name of cloud to resolve in, NULL = global cloud
//   pAddr    : pointer to result buffer
//
// Returns:  HRESULT
//
HRESULT PnrpResolve(PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddr)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    WSAQUERYSET*    pResults = NULL;
    WSAQUERYSET     tempResultSet = {0};
    HANDLE          hLookup = NULL;
    BOOL            fFound = FALSE;
    DWORD           dwError;
    INT             iRet;
    ULONG           i;
    DWORD           dwSize = 0;

    //
    // fill in the WSAQUERYSET
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.nMaxResolve = 1;
    pnrpInfo.dwTimeout = 30;
    pnrpInfo.enResolveCriteria = PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;
    // start resolve
    iRet = WSALookupServiceBegin(
            &querySet,
            LUP_RETURN_NAME | LUP_RETURN_ADDR | LUP_RETURN_COMMENT,
            &hLookup);


    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    if (SUCCEEDED(hr))
    {
        dwSize = sizeof(tempResultSet);

        // retrieve the required size
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, &tempResultSet);
        dwError = WSAGetLastError();

        if (dwError == WSAEFAULT)
        {
            // allocate space for the results
            pResults = (WSAQUERYSET*)malloc(dwSize);
            if (pResults == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }
        else
        {
            hr = HRESULT_FROM_WIN32(dwError);
        }
    }

    if (SUCCEEDED(hr))
    {
        // retrieve the addresses
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, pResults);
        if (iRet != 0)
        {
            hr = HRESULT_FROM_WIN32(WSAGetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // return the first IPv6 address found
        for (i = 0; i < pResults->dwNumberOfCsAddrs; i++)
        {
            if (pResults->lpcsaBuffer[i].iProtocol == IPPROTO_TCP &&
                pResults->lpcsaBuffer[i].RemoteAddr.iSockaddrLength == sizeof(SOCKADDR_IN6))
            {
                CopyMemory(pAddr, pResults->lpcsaBuffer[i].RemoteAddr.lpSockaddr, sizeof(SOCKADDR_IN6));
                fFound = TRUE;
                break;
            }
        }

        if (!fFound)
        {
            // unable to find an IPv6 address
            hr = HRESULT_FROM_WIN32(WSA_E_NO_MORE);
        }
    }

    if (hLookup != NULL)
    {
        WSALookupServiceEnd(hLookup);
    }

    if (pResults != NULL)
    {
        free(pResults);
    }

    return hr;
}
```



 

 



