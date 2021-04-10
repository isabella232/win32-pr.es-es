---
title: Conexión al servicio BITS
description: Para conectarse al servicio BITS, cree una instancia del objeto BackgroundCopyManager como se muestra en el ejemplo siguiente.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8146fa0def8c9c7dfd976784a930f35f20c965eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149384"
---
# <a name="connecting-to-the-bits-service"></a><span data-ttu-id="85f1a-103">Conexión al servicio BITS</span><span class="sxs-lookup"><span data-stu-id="85f1a-103">Connecting to the BITS Service</span></span>

<span data-ttu-id="85f1a-104">Para conectarse al servicio de sistema BITS, cree una instancia del objeto BackgroundCopyManager como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="85f1a-104">To connect to the BITS system service, create an instance of the BackgroundCopyManager object as shown in the following example.</span></span> <span data-ttu-id="85f1a-105">El servicio de sistema de BITS es el servicio de sistema de Windows que se ejecuta en el equipo cliente que implementa la capacidad de transferencia en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="85f1a-105">The BITS system service is the Windows system service running on the client computer that implements the background transfer capability.</span></span>


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



<span data-ttu-id="85f1a-106">Para probar una versión específica de BITS, use un identificador de clase simbólico para BackgroundCopyManager basándose en la versión que desea comprobar.</span><span class="sxs-lookup"><span data-stu-id="85f1a-106">To test for a specific version of BITS, use a symbolic class identifier for the BackgroundCopyManager based on the version you want to check.</span></span> <span data-ttu-id="85f1a-107">Por ejemplo, para probar los BITS 10,2, use CLSID \_ BackgroundCopyManager10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="85f1a-107">For example, to test for BITS 10.2, use CLSID\_BackgroundCopyManager10\_2.</span></span>

<span data-ttu-id="85f1a-108">En el ejemplo siguiente se muestra cómo usar uno de los identificadores de clase simbólicos.</span><span class="sxs-lookup"><span data-stu-id="85f1a-108">The following example shows how to use one of the symbolic class identifiers.</span></span>


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



<span data-ttu-id="85f1a-109">Use los métodos de la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para [crear trabajos de transferencia](creating-a-job.md), [enumerar trabajos](enumerating-jobs-in-the-transfer-queue.md) en la cola y [recuperar trabajos](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="85f1a-109">Use the methods of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to [create transfer jobs](creating-a-job.md), [enumerate jobs](enumerating-jobs-in-the-transfer-queue.md) in the queue, and [retrieve jobs](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span>



<span data-ttu-id="85f1a-110">BITS requiere que los proxies de interfaz del cliente usen el nivel de suplantación de identidad o suplantación.</span><span class="sxs-lookup"><span data-stu-id="85f1a-110">BITS requires that the client's interface proxies use either the IDENTIFY or IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="85f1a-111">Si la aplicación no llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com usa identificar de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="85f1a-111">If the application does not call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM uses IDENTIFY by default.</span></span> <span data-ttu-id="85f1a-112">BITS produce un error con E \_ ACCESSDENIED si no se establece el nivel de suplantación correcto.</span><span class="sxs-lookup"><span data-stu-id="85f1a-112">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span> <span data-ttu-id="85f1a-113">Si proporciona una biblioteca que ejecuta las interfaces BITS, y una aplicación que llama a la biblioteca establece el nivel de suplantación que se indica a continuación, deberá llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para establecer el nivel de suplantación correcto para cada interfaz de bits a la que llame.</span><span class="sxs-lookup"><span data-stu-id="85f1a-113">If you provide a library that exercises the BITS interfaces, and an application that calls your library sets the impersonation level below IDENTIFY, then you will need to call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set the correct impersonation level for each BITS interface that you call.</span></span>

<span data-ttu-id="85f1a-114">Antes de que se cierre la aplicación, libere la copia del puntero de la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="85f1a-114">Before your application exits, release your copy of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer, as shown in the following example.</span></span>


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="85f1a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85f1a-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="85f1a-116">[Llamar a bits desde .net y C#](/windows/desktop/Bits/bits-dot-net) para bits</span><span class="sxs-lookup"><span data-stu-id="85f1a-116">[Calling into BITS from .NET and C#](/windows/desktop/Bits/bits-dot-net) for BITS</span></span>
</dt> </dl>

 

 