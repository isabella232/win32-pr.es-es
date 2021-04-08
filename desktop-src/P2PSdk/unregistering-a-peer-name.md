---
description: Al anular el registro de un nombre de mismo nivel, se quita un nombre registrado de una nube de protocolo de resolución de nombres de mismo nivel (PNRP).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Anular el registro de un nombre de mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001992"
---
# <a name="unregistering-a-peer-name"></a>Anular el registro de un nombre de mismo nivel

Al anular el registro de un nombre de mismo nivel, se quita un nombre registrado de una nube de protocolo de resolución de nombres de mismo nivel (PNRP).

## <a name="unregistering-a-peer-name"></a>Anular el registro de un nombre de mismo nivel

Para anular el registro de un nombre de mismo nivel, llame a [**WSASetService**](pnrp-and-wsasetservice.md). El parámetro *essOperation* debe tener un valor de **RNRSERVICE \_ Delete**. Siga las instrucciones de las siguientes secciones de este tema para realizar las configuraciones necesarias para los parámetros **WSASetService** y la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

## <a name="configuring-wsasetservice"></a>Configuración de WSASetService

Cuando una aplicación llama a [**WSASetService**](pnrp-and-wsasetservice.md), los parámetros deben configurarse de acuerdo con las especificaciones siguientes:

-   *essOperation* debe tener un valor de **RNRSERVICE \_ Delete**.
-   *dwFlags* debe ser cero (0).
-   *lpqsRegInfo* debe apuntar a una estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que debe configurarse siguiendo las instrucciones de la siguiente sección de este tema.

## <a name="configuring-wsaqueryset"></a>Configuración de WSAQUERYSET

La estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) se debe configurar de acuerdo con las especificaciones siguientes:

-   **dwSize** debe especificar el tamaño de la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** debe apuntar al nombre del mismo nivel cuyo registro se va a anular.
-   **lpBlob** debe apuntar a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** debe apuntar a la lista de direcciones.

> [!Note]  
> Los miembros restantes se describen en [**PNRP y WSASetService**](pnrp-and-wsasetservice.md).

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Ejemplo de anulación del registro de un nombre de mismo nivel

En el fragmento de código siguiente se muestra cómo anular el registro de un nombre del mismo nivel proporcionando la información correcta al llamar a [**WSASetService**](pnrp-and-wsasetservice.md) mediante la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


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



 

 



