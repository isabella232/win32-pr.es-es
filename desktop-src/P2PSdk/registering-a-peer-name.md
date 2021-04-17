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
# <a name="registering-a-peer-name"></a><span data-ttu-id="f924f-103">Registrar un nombre de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="f924f-103">Registering a Peer Name</span></span>

<span data-ttu-id="f924f-104">Para registrar un nombre del mismo nivel, una aplicación debe proporcionar la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="f924f-104">To register a peer name, an application must provide the following information:</span></span>

-   <span data-ttu-id="f924f-105">Lista de direcciones IP</span><span class="sxs-lookup"><span data-stu-id="f924f-105">IP address list</span></span>
-   [<span data-ttu-id="f924f-106">Identidad del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="f924f-106">Peer identity</span></span>](creating-a-peer-identity.md)
-   [<span data-ttu-id="f924f-107">Nombre del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="f924f-107">Peer name</span></span>](peer-names.md)

<span data-ttu-id="f924f-108">Si un nombre del mismo nivel no es seguro, una identidad es opcional.</span><span class="sxs-lookup"><span data-stu-id="f924f-108">If a peer name is unsecured, an identity is optional.</span></span> <span data-ttu-id="f924f-109">Si una identidad del mismo nivel se especifica como **null**, el protocolo de resolución de nombres de mismo nivel (PNRP) utiliza una identidad del mismo nivel interna y predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f924f-109">If a peer identity is specified as **NULL**, the Peer Name Resolution Protocol (PNRP) uses an internal, default peer identity.</span></span>

## <a name="registering-a-peer-name"></a><span data-ttu-id="f924f-110">Registrar un nombre de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="f924f-110">Registering a Peer Name</span></span>

<span data-ttu-id="f924f-111">Una vez identificadas la lista de direcciones IP, la identidad del mismo nivel y el nombre del mismo nivel, la aplicación puede registrar un nombre del mismo nivel llamando a [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="f924f-111">After the IP address list, peer identity, and peer name are identified, the application can register a peer name by calling [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="f924f-112">Siga las instrucciones de las siguientes secciones de este tema para realizar las configuraciones necesarias para los parámetros **WSASetService** y la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="f924f-112">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

### <a name="configuring-wsasetservice"></a><span data-ttu-id="f924f-113">Configuración de WSASetService</span><span class="sxs-lookup"><span data-stu-id="f924f-113">Configuring WSASetService</span></span>

<span data-ttu-id="f924f-114">Cuando una aplicación llama a [**WSASetService**](pnrp-and-wsasetservice.md), los parámetros deben configurarse de acuerdo con las especificaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f924f-114">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="f924f-115">*essOperation* debe tener un valor de **RNRSERVICE \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="f924f-115">*essOperation* must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="f924f-116">*dwFlags* debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="f924f-116">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="f924f-117">*lpqsRegInfo* debe apuntar a una estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que debe configurarse mediante las instrucciones de la sección siguiente **configuración de WSAQUERYSET** de este tema.</span><span class="sxs-lookup"><span data-stu-id="f924f-117">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following **Configuring WSAQUERYSET** section of this topic.</span></span>

### <a name="configuring-wsaqueryset"></a><span data-ttu-id="f924f-118">Configuración de WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="f924f-118">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="f924f-119">La estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) se debe configurar de acuerdo con las especificaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f924f-119">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="f924f-120">**dwSize** debe especificar el tamaño de la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="f924f-120">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="f924f-121">**lpszServiceInstanceName** debe apuntar al nombre del mismo nivel que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="f924f-121">**lpszServiceInstanceName** must point to the peer name that is being registered.</span></span>
-   <span data-ttu-id="f924f-122">**lpBlob** debe apuntar a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="f924f-122">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="f924f-123">**lpcsaBuffer** debe apuntar a la lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f924f-123">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="f924f-124">Los miembros restantes se describen en [**PNRP y WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="f924f-124">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

<span data-ttu-id="f924f-125">Una vez registrado un nombre de mismo nivel, la información está disponible para la infraestructura del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="f924f-125">After a peer name is registered, the information is available to the Peer Infrastructure.</span></span> <span data-ttu-id="f924f-126">Sin embargo, hay un retraso entre el tiempo de registro y la propagación de la información de registro a otros nodos.</span><span class="sxs-lookup"><span data-stu-id="f924f-126">However, there is a delay between the registration time and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="f924f-127">Durante ese tiempo, es posible que otros nodos no puedan resolver el elemento del mismo nivel registrado recientemente.</span><span class="sxs-lookup"><span data-stu-id="f924f-127">During that time, other nodes may not be able to resolve the newly registered peer.</span></span>

## <a name="example-of-registering-a-peer-name"></a><span data-ttu-id="f924f-128">Ejemplo de registro de un nombre de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="f924f-128">Example of Registering a Peer Name</span></span>

<span data-ttu-id="f924f-129">En el fragmento de código siguiente se muestra cómo registrar un nombre del mismo nivel proporcionando la información correcta al llamar a [**WSASetService**](pnrp-and-wsasetservice.md) mediante la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="f924f-129">The following code snippet shows you how to register a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



