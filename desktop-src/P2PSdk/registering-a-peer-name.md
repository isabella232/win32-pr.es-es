---
description: 'Para registrar un nombre del mismo nivel, una aplicación debe proporcionar la siguiente información: dirección IP listPeer identityPeer nameIf un nombre del mismo nivel no es seguro, una identidad es opcional.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrar un nombre de mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668061"
---
# <a name="registering-a-peer-name"></a>Registrar un nombre de mismo nivel

Para registrar un nombre del mismo nivel, una aplicación debe proporcionar la siguiente información:

-   Lista de direcciones IP
-   [Identidad del mismo nivel](creating-a-peer-identity.md)
-   [Nombre del mismo nivel](peer-names.md)

Si un nombre del mismo nivel no es seguro, una identidad es opcional. Si una identidad del mismo nivel se especifica como **null**, el protocolo de resolución de nombres de mismo nivel (PNRP) utiliza una identidad del mismo nivel interna y predeterminada.

## <a name="registering-a-peer-name"></a>Registrar un nombre de mismo nivel

Una vez identificadas la lista de direcciones IP, la identidad del mismo nivel y el nombre del mismo nivel, la aplicación puede registrar un nombre del mismo nivel llamando a [**WSASetService**](pnrp-and-wsasetservice.md). Siga las instrucciones de las siguientes secciones de este tema para realizar las configuraciones necesarias para los parámetros **WSASetService** y la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

### <a name="configuring-wsasetservice"></a>Configuración de WSASetService

Cuando una aplicación llama a [**WSASetService**](pnrp-and-wsasetservice.md), los parámetros deben configurarse de acuerdo con las especificaciones siguientes:

-   *essOperation* debe tener un valor de **RNRSERVICE \_ Register**.
-   *dwFlags* debe ser cero (0).
-   *lpqsRegInfo* debe apuntar a una estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que debe configurarse mediante las instrucciones de la sección siguiente **configuración de WSAQUERYSET** de este tema.

### <a name="configuring-wsaqueryset"></a>Configuración de WSAQUERYSET

La estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) se debe configurar de acuerdo con las especificaciones siguientes:

-   **dwSize** debe especificar el tamaño de la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** debe apuntar al nombre del mismo nivel que se está registrando.
-   **lpBlob** debe apuntar a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** debe apuntar a la lista de direcciones.

> [!Note]  
> Los miembros restantes se describen en [**PNRP y WSASetService**](pnrp-and-wsasetservice.md).

 

Una vez registrado un nombre de mismo nivel, la información está disponible para la infraestructura del mismo nivel. Sin embargo, hay un retraso entre el tiempo de registro y la propagación de la información de registro a otros nodos. Durante ese tiempo, es posible que otros nodos no puedan resolver el elemento del mismo nivel registrado recientemente.

## <a name="example-of-registering-a-peer-name"></a>Ejemplo de registro de un nombre de mismo nivel

En el fragmento de código siguiente se muestra cómo registrar un nombre del mismo nivel proporcionando la información correcta al llamar a [**WSASetService**](pnrp-and-wsasetservice.md) mediante la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



