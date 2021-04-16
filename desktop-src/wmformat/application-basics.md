---
title: Aspectos básicos de la aplicación
description: Aspectos básicos de la aplicación
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- SDK de Windows Media Format, conceptos básicos de la aplicación DRM
- Administración de derechos digitales (DRM), aspectos básicos de la aplicación
- DRM (administración de derechos digitales), aspectos básicos de la aplicación
- Administración de derechos digitales (DRM), función WMDRMStartup
- DRM (administración de derechos digitales), función WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268326"
---
# <a name="application-basics"></a>Aspectos básicos de la aplicación

Hay algún procesamiento adicional que debe realizar para cualquier aplicación que use las API extendidas del cliente DRM de Windows Media. En este tema se describen los requisitos para una aplicación sencilla.

En primer lugar, debe inicializar las API extendidas del cliente DRM de Windows Media mediante una llamada a la función [**WMDRMStartup**](wmdrmstartup.md) . Los objetos del SDK son objetos COM, pero no es necesario llamar a **CoIntialize**, porque la función **WMDRMStatup** inicializa com automáticamente.

> [!Note]  
> El SDK de Windows Media Format solo usa un subconjunto de COM, por lo que si usa objetos COM distintos de los de la API extendida del cliente DRM de Windows Media, debe seguir llamando a **CoInitialize**.

 

Todos los objetos de las API extendidas del cliente DRM de Windows Media se crean mediante funciones y métodos auxiliares. Nunca necesita llamar a **CoCreateInstance** para crear un objeto. La primera interfaz en la que se crean instancias para cualquier aplicación que use el SDK es [**IWMDRMProvider**](iwmdrmprovider.md), que se puede usar para crear instancias de todas las demás interfaces base. Para obtener una instancia de **IWMDRMProvider**, debe llamar a [**WMDRMCreateProvider**](wmdrmcreateprovider.md) o [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md). La diferencia entre estas funciones es que **WMDRMCreateProvider** crea un objeto que, a su vez, solo puede crear objetos que no admiten métodos que requieran la biblioteca de código auxiliar.

Después de tener una instancia de **IWMDRMProvider**, puede crear los otros objetos que necesita llamando a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).

Cuando esté listo para salir de la aplicación, debe liberar los recursos del subsistema DRM mediante una llamada a la función [**WMDRMShutdown**](wmdrmshutdown.md) . Esta función también cierra COM automáticamente.

En el ejemplo de código siguiente se muestra cómo inicializar y concluir una aplicación que usa las API extendidas del cliente DRM de Windows Media.


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción**](drm-getting-started.md)
</dt> </dl>

 

 




