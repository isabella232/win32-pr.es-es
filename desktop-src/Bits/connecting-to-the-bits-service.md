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
# <a name="connecting-to-the-bits-service"></a>Conexión al servicio BITS

Para conectarse al servicio de sistema BITS, cree una instancia del objeto BackgroundCopyManager como se muestra en el ejemplo siguiente. El servicio de sistema de BITS es el servicio de sistema de Windows que se ejecuta en el equipo cliente que implementa la capacidad de transferencia en segundo plano.


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



Para probar una versión específica de BITS, use un identificador de clase simbólico para BackgroundCopyManager basándose en la versión que desea comprobar. Por ejemplo, para probar los BITS 10,2, use CLSID \_ BackgroundCopyManager10 \_ 2.

En el ejemplo siguiente se muestra cómo usar uno de los identificadores de clase simbólicos.


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



Use los métodos de la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para [crear trabajos de transferencia](creating-a-job.md), [enumerar trabajos](enumerating-jobs-in-the-transfer-queue.md) en la cola y [recuperar trabajos](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



BITS requiere que los proxies de interfaz del cliente usen el nivel de suplantación de identidad o suplantación. Si la aplicación no llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com usa identificar de forma predeterminada. BITS produce un error con E \_ ACCESSDENIED si no se establece el nivel de suplantación correcto. Si proporciona una biblioteca que ejecuta las interfaces BITS, y una aplicación que llama a la biblioteca establece el nivel de suplantación que se indica a continuación, deberá llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para establecer el nivel de suplantación correcto para cada interfaz de bits a la que llame.

Antes de que se cierre la aplicación, libere la copia del puntero de la interfaz [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , tal como se muestra en el ejemplo siguiente.


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a bits desde .net y C#](/windows/desktop/Bits/bits-dot-net) para bits
</dt> </dl>

 

 