---
description: Al anular el registro de un nombre del mismo nivel, se quita un nombre registrado de una nube del Protocolo de resolución de nombres del mismo nivel (PNRP).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Anulación del registro de un nombre del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ee0bd03e881f93321c31dfccd03cc71459b323f1ed356a88f829489c578a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675015"
---
# <a name="unregistering-a-peer-name"></a>Anulación del registro de un nombre del mismo nivel

Al anular el registro de un nombre del mismo nivel, se quita un nombre registrado de una nube del Protocolo de resolución de nombres del mismo nivel (PNRP).

## <a name="unregistering-a-peer-name"></a>Anulación del registro de un nombre del mismo nivel

Para anular el registro de un nombre del mismo nivel, llame [**a WSASetService**](pnrp-and-wsasetservice.md). El *parámetro essOperation* debe tener un valor **de RNRSERVICE \_ DELETE**. Use las instrucciones de las secciones siguientes de este tema para realizar las configuraciones necesarias para los parámetros **WSASetService** y la estructura [**WSAQUERYSET.**](pnrp-and-wsaqueryset.md)

## <a name="configuring-wsasetservice"></a>Configuración de WSASetService

Cuando una aplicación llama a [**WSASetService**](pnrp-and-wsasetservice.md), los parámetros deben configurarse según las especificaciones siguientes:

-   *essOperation* debe tener un valor de **RNRSERVICE \_ DELETE**.
-   *dwFlags* debe ser cero (0).
-   *lpqsRegInfo* debe apuntar a una estructura [**WSAQUERYSET,**](pnrp-and-wsaqueryset.md) que debe configurarse mediante las directrices de la sección siguiente de este tema.

## <a name="configuring-wsaqueryset"></a>Configuración de WSAQUERYSET

La [**estructura WSAQUERYSET**](pnrp-and-wsaqueryset.md) debe configurarse según las especificaciones siguientes:

-   **dwSize** debe especificar el tamaño de la [**estructura WSAQUERYSET.**](pnrp-and-wsaqueryset.md)
-   **lpszServiceInstanceName** debe apuntar al nombre del mismo nivel que se está anulando el registro.
-   **lpBlob** debe apuntar a una [**estructura PNRPINFO.**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
-   **lpcsaBuffer debe** apuntar a la lista de direcciones.

> [!Note]  
> Los miembros restantes se describen [**en PNRP y WSASetService**](pnrp-and-wsasetservice.md).

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Ejemplo de anulación del registro de un nombre del mismo nivel

El siguiente fragmento de código muestra cómo anular el registro de un nombre del mismo nivel proporcionando la información correcta al llamar a [**WSASetService**](pnrp-and-wsasetservice.md) mediante la estructura [**WSAQUERYSET.**](pnrp-and-wsaqueryset.md)


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



