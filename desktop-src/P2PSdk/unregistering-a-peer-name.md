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
# <a name="unregistering-a-peer-name"></a><span data-ttu-id="e50c8-103">Anular el registro de un nombre de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="e50c8-103">Unregistering a Peer Name</span></span>

<span data-ttu-id="e50c8-104">Al anular el registro de un nombre de mismo nivel, se quita un nombre registrado de una nube de protocolo de resolución de nombres de mismo nivel (PNRP).</span><span class="sxs-lookup"><span data-stu-id="e50c8-104">When you unregister a peer name, a registered name is removed from a Peer Name Resolution Protocol (PNRP) cloud.</span></span>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="e50c8-105">Anular el registro de un nombre de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="e50c8-105">Unregistering a Peer Name</span></span>

<span data-ttu-id="e50c8-106">Para anular el registro de un nombre de mismo nivel, llame a [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="e50c8-106">To unregister a peer name, call [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="e50c8-107">El parámetro *essOperation* debe tener un valor de **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="e50c8-107">The *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span> <span data-ttu-id="e50c8-108">Siga las instrucciones de las siguientes secciones de este tema para realizar las configuraciones necesarias para los parámetros **WSASetService** y la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="e50c8-108">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

## <a name="configuring-wsasetservice"></a><span data-ttu-id="e50c8-109">Configuración de WSASetService</span><span class="sxs-lookup"><span data-stu-id="e50c8-109">Configuring WSASetService</span></span>

<span data-ttu-id="e50c8-110">Cuando una aplicación llama a [**WSASetService**](pnrp-and-wsasetservice.md), los parámetros deben configurarse de acuerdo con las especificaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e50c8-110">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="e50c8-111">*essOperation* debe tener un valor de **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="e50c8-111">*essOperation* must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="e50c8-112">*dwFlags* debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="e50c8-112">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="e50c8-113">*lpqsRegInfo* debe apuntar a una estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que debe configurarse siguiendo las instrucciones de la siguiente sección de este tema.</span><span class="sxs-lookup"><span data-stu-id="e50c8-113">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following section of this topic.</span></span>

## <a name="configuring-wsaqueryset"></a><span data-ttu-id="e50c8-114">Configuración de WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="e50c8-114">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="e50c8-115">La estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) se debe configurar de acuerdo con las especificaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e50c8-115">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="e50c8-116">**dwSize** debe especificar el tamaño de la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="e50c8-116">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="e50c8-117">**lpszServiceInstanceName** debe apuntar al nombre del mismo nivel cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="e50c8-117">**lpszServiceInstanceName** must point to the peer name that is being unregistered.</span></span>
-   <span data-ttu-id="e50c8-118">**lpBlob** debe apuntar a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="e50c8-118">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="e50c8-119">**lpcsaBuffer** debe apuntar a la lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e50c8-119">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="e50c8-120">Los miembros restantes se describen en [**PNRP y WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="e50c8-120">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

## <a name="an-example-of-unregistering-a-peer-name"></a><span data-ttu-id="e50c8-121">Ejemplo de anulación del registro de un nombre de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="e50c8-121">An Example of Unregistering a Peer Name</span></span>

<span data-ttu-id="e50c8-122">En el fragmento de código siguiente se muestra cómo anular el registro de un nombre del mismo nivel proporcionando la información correcta al llamar a [**WSASetService**](pnrp-and-wsasetservice.md) mediante la estructura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="e50c8-122">The following code snippet shows you how to unregister a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



