---
title: Conexión al servicio BITS
description: Para conectarse al servicio BITS, cree una instancia del objeto BackgroundCopyManager como se muestra en el ejemplo siguiente.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dacd97b78fa9c5d3a1e410a44e3c376368654e99a6f4ace9161d36b127d9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528945"
---
# <a name="connecting-to-the-bits-service"></a>Conexión al servicio BITS

Para conectarse al servicio del sistema BITS, cree una instancia del objeto BackgroundCopyManager como se muestra en el ejemplo siguiente. El servicio del sistema BITS es el Windows sistema que se ejecuta en el equipo cliente que implementa la funcionalidad de transferencia en segundo plano.


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



Para probar una versión específica de BITS, use un identificador de clase simbólico para BackgroundCopyManager en función de la versión que desea comprobar. Por ejemplo, para probar BITS 10.2, use CLSID \_ BackgroundCopyManager10 \_ 2.

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



Use los métodos de la [**interfaz IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para crear trabajos de [transferencia,](creating-a-job.md) [enumerar](enumerating-jobs-in-the-transfer-queue.md) trabajos en la cola y [recuperar trabajos](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



BITS requiere que los servidores proxy de interfaz del cliente usen el nivel IDENTIFY o IMPERSONATE de suplantación. Si la aplicación no llama a [**CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)COM usa IDENTIFY de forma predeterminada. BITS produce un error con E ACCESSDENIED si no se establece el nivel de \_ suplantación correcto. Si proporciona una biblioteca que ejercicio las interfaces BITS y una aplicación que llama a la biblioteca establece el nivel de suplantación por debajo de IDENTIFY, deberá llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para establecer el nivel de suplantación correcto para cada interfaz bits a la que llame.

Antes de que se cierre la aplicación, suelte la copia del puntero de interfaz [**IBackgroundCopyManager,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) como se muestra en el ejemplo siguiente.


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

[Llamada a BITS desde .NET y C#](/windows/desktop/Bits/bits-dot-net) para BITS
</dt> </dl>

 

 