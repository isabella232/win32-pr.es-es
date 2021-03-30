---
description: Administrar operaciones asincrónicas
ms.assetid: e5136e15-3ae1-4e0a-ae97-fcf16203b21d
title: Administrar operaciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d220c5633f9ee044dbf9cdb6a63b563747620afd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002317"
---
# <a name="managing-asynchronous-operations"></a><span data-ttu-id="1863f-103">Administrar operaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="1863f-103">Managing Asynchronous Operations</span></span>

<span data-ttu-id="1863f-104">\[A partir de Windows 8 y Windows Server 2012, el [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1863f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1863f-105">En el ejemplo de código siguiente se muestra cómo funciona un llamador con un objeto Async.</span><span class="sxs-lookup"><span data-stu-id="1863f-105">The code example that follows demonstrates how a caller works with an async object.</span></span> <span data-ttu-id="1863f-106">Aquí, la función **SynchronousCreateLun** llama al método [**IVdsSubSystem:: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) asincrónico con los parámetros especificados.</span><span class="sxs-lookup"><span data-stu-id="1863f-106">Here, the **SynchronousCreateLun** function calls the asynchronous [**IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) method using the given parameters.</span></span> <span data-ttu-id="1863f-107">La función esperará en el objeto asincrónico para que finalice la llamada asincrónica al método **CreateLun** .</span><span class="sxs-lookup"><span data-stu-id="1863f-107">The function will wait on the async object for the asynchronous **CreateLun** method call to finish.</span></span> <span data-ttu-id="1863f-108">Cuando el método [**IVdsAsync:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) devuelve, **SynchronousCreateLun** obtiene la interfaz [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) para el LUN recién creado y lo devuelve como un argumento out.</span><span class="sxs-lookup"><span data-stu-id="1863f-108">When the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method returns, **SynchronousCreateLun** gets the [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) interface for the newly created LUN and returns it as an out argument.</span></span>


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT SynchronousCreateLun(
    IVdsSubSystem *pSubsystem,
    VDS_LUN_TYPE  type,
    ULONGLONG     ullSize,
    VDS_OBJECT_ID *pDriveIdArray,
    LONG          lNumberOfDrives,
    LPWSTR        pwszUnmaskingList,
    VDS_HINTS     *pHints,
    IVdsLun       **ppLun)
{
    HRESULT hResult = S_OK;
    HRESULT hResult2 = S_OK;
    IVdsAsync *pAsync = NULL;
    VDS_ASYNC_OUTPUT AsyncOut;
    IUnknown* pUnknown = NULL;

    ZeroMemory( &AsyncOut, sizeof(VDS_ASYNC_OUTPUT));

    hResult = pSubsystem->CreateLun(
        type,
        ullSize,
        pDriveIdArray,
        lNumberOfDrives,
        pwszUnmaskingList,
        pHints,
        &pAsync);

    if (SUCCEEDED(hResult) && (!pAsync)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK 
                                // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) {
        // Wait until the Async is done.
        hResult2 = pAsync->Wait( &hResult, &AsyncOut);
        if (SUCCEEDED(hResult) && FAILED(hResult2)) {
            hResult = hResult2;
        }
    }

    if (SUCCEEDED(hResult) && (VDS_ASYNCOUT_CREATELUN != AsyncOut.type)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK  
                                // with an unexpected type.
    }

    if (SUCCEEDED(hResult)) {
        pUnknown = AsyncOut.cl.pLunUnk;
        if (!pUnknown) {
            hResult = E_UNEXPECTED; // Errant provider, returned 
                                    // S_OK with a NULL pointer.
        }
    }

    if (SUCCEEDED(hResult)) {
        hResult = pUnknown->QueryInterface(IID_IVdsLun, (void **)ppLun);
    }

    _SafeRelease(pAsync);
    _SafeRelease(pUnknown);

    return hResult;
}
```



## <a name="related-topics"></a><span data-ttu-id="1863f-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1863f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1863f-110">Uso de VDS</span><span class="sxs-lookup"><span data-stu-id="1863f-110">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="1863f-111">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="1863f-111">Helper Objects</span></span>](helper-objects.md)
</dt> <dt>

[<span data-ttu-id="1863f-112">**IVdsSubSystem::CreateLun**</span><span class="sxs-lookup"><span data-stu-id="1863f-112">**IVdsSubSystem::CreateLun**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[<span data-ttu-id="1863f-113">**IVdsAsync:: wait**</span><span class="sxs-lookup"><span data-stu-id="1863f-113">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="1863f-114">**IVdsLun**</span><span class="sxs-lookup"><span data-stu-id="1863f-114">**IVdsLun**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
