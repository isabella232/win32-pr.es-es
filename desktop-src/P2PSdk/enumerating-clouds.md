---
description: Al enumerar las nubes, una aplicación debe proporcionar el ámbito de la búsqueda de nubes. Una vez identificado el ámbito, la aplicación puede comenzar el proceso de enumeración.
ms.assetid: efd16cca-ac63-4bfa-bc6c-d7465cc374ee
title: Enumerar nubes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f958a2cc958c10bd85e674b43a3b41354fc344c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667442"
---
# <a name="enumerating-clouds"></a><span data-ttu-id="2a249-104">Enumerar nubes</span><span class="sxs-lookup"><span data-stu-id="2a249-104">Enumerating Clouds</span></span>

<span data-ttu-id="2a249-105">Al enumerar las nubes, una aplicación debe proporcionar el ámbito de la búsqueda de nubes.</span><span class="sxs-lookup"><span data-stu-id="2a249-105">When enumerating clouds, an application must provide the scope of the search for clouds.</span></span> <span data-ttu-id="2a249-106">Una vez identificado el ámbito, la aplicación puede comenzar el proceso de enumeración.</span><span class="sxs-lookup"><span data-stu-id="2a249-106">After the scope is identified, the application can begin the enumeration process.</span></span>

<span data-ttu-id="2a249-107">En el procedimiento siguiente se identifican las llamadas que deben realizarse para enumerar nubes.</span><span class="sxs-lookup"><span data-stu-id="2a249-107">The following procedure identifies the calls that need to be made to enumerate clouds.</span></span>

<span data-ttu-id="2a249-108">**Para enumerar nubes**</span><span class="sxs-lookup"><span data-stu-id="2a249-108">**To enumerate clouds**</span></span>

1.  <span data-ttu-id="2a249-109">Llame a [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) para iniciar el proceso y devolver un identificador.</span><span class="sxs-lookup"><span data-stu-id="2a249-109">Call [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) to begin the process and return a handle.</span></span>
2.  <span data-ttu-id="2a249-110">Llame a [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) para recuperar un conjunto de nubes y, a continuación, llame a esta función hasta que la aplicación haya recuperado todas las nubes.</span><span class="sxs-lookup"><span data-stu-id="2a249-110">Call [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) to retrieve a set of clouds, and then call this function until the application has retrieved all the clouds.</span></span>
3.  <span data-ttu-id="2a249-111">Llame a [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) para finalizar la enumeración.</span><span class="sxs-lookup"><span data-stu-id="2a249-111">Call [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) to finish the enumeration.</span></span>

## <a name="example-enumerating-and-printing-the-names-of-available-link-local-clouds"></a><span data-ttu-id="2a249-112">Ejemplo: enumerar e imprimir los nombres de las nubes locales de vínculo disponibles</span><span class="sxs-lookup"><span data-stu-id="2a249-112">Example: Enumerating and Printing the Names of Available Link-Local Clouds</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "ws2_32.lib")

DWORD PrintLinkLocalClouds()
{

    WSAQUERYSETW    qset;
    BLOB            Blob;
    PNRPCLOUDINFO   CloudInfo;
    HANDLE          hLookup = NULL;
    int             err;
    DWORD           dwErr = NO_ERROR;
    DWORD           dwSize;
    WSAQUERYSETW    *pResults = NULL;

    ZeroMemory(&qset, sizeof(qset));
    ZeroMemory(&CloudInfo, sizeof(CloudInfo));

    CloudInfo.dwSize = sizeof(PNRPCLOUDINFO);
    CloudInfo.Cloud.Scope = PNRP_LINK_LOCAL_SCOPE;

    Blob.cbSize = sizeof(PNRPCLOUDINFO);
    Blob.pBlobData = (LPBYTE)&CloudInfo;

    qset.dwSize = sizeof(WSAQUERYSET);
    qset.dwNameSpace = NS_PNRPCLOUD;
    qset.lpServiceClassId = (LPGUID)&SVCID_PNRPCLOUD;
    qset.lpBlob = &Blob;

    //
    // Start enumeration
    //
    err = WSALookupServiceBegin(
            &qset,
            LUP_RETURN_NAME,
            &hLookup);
                
    if(err !=0)
    {
        return WSAGetLastError();
    }

    // getting results
    while(TRUE)
    {

        //
        // Get size
        //
        ZeroMemory(&qset, sizeof(qset));
        dwSize = sizeof(qset);

        pResults = &qset;

        err = WSALookupServiceNext(
                hLookup,
                0,
                &dwSize,
                pResults
                );
        if(err != 0)
        {
            dwErr = WSAGetLastError();
        }

        if(dwErr != NO_ERROR)
        {
            if(dwErr == WSA_E_NO_MORE)
            {
                //
                // No more entries
                //
                dwErr = ERROR_SUCCESS;
                break;
            }
            else if (dwErr == WSAEFAULT)
            {
                //
                // This usually means result buffer too small. Allocate space
                //
                pResults = (WSAQUERYSET *)malloc(dwSize);
                if(pResults == NULL)
                {
                    dwErr = ERROR_OUTOFMEMORY;
                    break;
                }

                //
                // Get cloud name
                //
                err = WSALookupServiceNext(
                        hLookup,
                        0,
                        &dwSize,
                        pResults
                        );
                if(err == 0)
                {
                    wprintf(L"%s\n", pResults->lpszServiceInstanceName);

                    dwErr = NO_ERROR;
                }
                else
                {
                    dwErr = WSAGetLastError();
                }

                free(pResults);

                if(dwErr != NO_ERROR)
                {
                    break;
                }
            }
            else
            {
                //
                // Some other unexpected error
                //
                break;
            }
        }
        else
        {
            //
            // Should never happen
            //
            dwErr = ERROR_GEN_FAILURE;
            break;
        }
    }

    //
    // Close the enumeration
    //
    WSALookupServiceEnd(hLookup);
                
    return dwErr;
}
```



 

 



