---
description: Describe cómo incluir el proveedor COM de WMI como componente dentro de una aplicación en lugar de en el proceso de WMI. Denominado proveedor desacoplado, este es el tipo recomendado de proveedor COM de WMI que se va a crear para los sistemas operativos Windows 2000 y versiones posteriores.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Incorporación de un proveedor en una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104549909"
---
# <a name="incorporating-a-provider-in-an-application"></a>Incorporación de un proveedor en una aplicación

Al crear una aplicación que se va a instrumentar, el procedimiento recomendado consiste en incluir el proveedor como un componente dentro de la propia aplicación. Esta práctica permite que Instrumental de administración de Windows (WMI) interactúe directamente con el proveedor de servicios en lugar de hacerlo indirectamente a través de la API de programa. Desacoplar el proveedor de WMI también pone a la aplicación en el control de la duración del proveedor, en lugar de WMI. Para obtener más información sobre cómo escribir un proveedor que se ejecuta en el proceso WMI, vea [proporcionar datos a WMI escribiendo un proveedor](supplying-data-to-wmi-by-writing-a-provider.md). Para obtener más información sobre el modelo de hospedaje y la configuración de seguridad para el proveedor, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

En el diagrama siguiente se ilustra la relación entre WMI, un proveedor desacoplado y una aplicación.

![relación entre WMI, el proveedor desacoplado y la aplicación](images/decoupledprov.png)

Para obtener más información sobre los métodos de proveedor desacoplados, vea [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) y [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).

> [!Note]  
> El proveedor desacoplado admite la instancia, el método, los proveedores de eventos y los consumidores de eventos. No admite proveedores de clases y propiedades. Para obtener más información, consulte [escribir un proveedor de clases](writing-a-class-provider.md) y [escribir un proveedor de propiedades](writing-a-property-provider.md).

 

Los ejemplos de código de este tema requieren las siguientes referencias e \# incluyen instrucciones para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



En el procedimiento siguiente se usan ejemplos de código de C++ para describir cómo incorporar un proveedor desacoplado en la aplicación. El método de inicialización de la aplicación realiza los pasos siguientes para que WMI solo interactúe con un proveedor desacoplado registrado.

**Para implementar un proveedor desacoplado en una aplicación de C++**

1.  Inicializa la biblioteca COM para que la use el subproceso que realiza la llamada.

    En el ejemplo de código siguiente se muestra cómo inicializar la biblioteca COM.

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  Establezca el nivel de seguridad de proceso predeterminado.

    Este nivel establece el nivel de seguridad necesario para que otros procesos tengan acceso a la información del proceso del cliente. El nivel de autenticación debe ser el nivel predeterminado de autenticación de RPC \_ C \_ \_ \_ . Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).

    En el ejemplo de código siguiente se muestra cómo establecer el nivel de seguridad predeterminado.

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  Registra el registrador de proveedores desacoplado.

    En el ejemplo de código siguiente se muestra cómo registrar el registrador de proveedores desacoplado.

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  Registre el proveedor de eventos desacoplado.

    En el ejemplo de código siguiente se muestra cómo registrar el proveedor de eventos desacoplado.

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  Realice las [llamadas a WMI](making-calls-to-wmi.md) requeridas por la funcionalidad del proveedor. Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md). Para obtener más información si el proveedor presta servicio a una solicitud de datos de un script o una aplicación, consulte [Suplantar a un cliente](impersonating-a-client.md).

Justo antes de finalizar, la aplicación debe limpiarse después. En el procedimiento siguiente se describe cómo anular el registro del proveedor desacoplado para que WMI no intente consultarlo para obtener información.

En el procedimiento siguiente se describe cómo anular el registro del proveedor desacoplado.

**Para anular el registro del proveedor desacoplado**

1.  Anular el registro y liberar el registrador.

    En el ejemplo de código siguiente se muestra cómo anular el registro y liberar el registrador.

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  Anule el registro del proveedor de eventos y suéltelo.

    En el ejemplo de código siguiente se muestra cómo anular el registro del proveedor de eventos y liberarlo.

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  Limpie el servidor COM.

    En el ejemplo de código siguiente se muestra cómo anular la inicialización de la biblioteca COM.

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 



