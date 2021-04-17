---
description: El primer paso para usar los servicios de adquisición de imágenes de Windows (WIA) es obtener un puntero de interfaz IWiaDevMgr (si está programando para Windows XP o versiones anteriores) o un puntero de interfaz IWiaDevMgr2 (si está programando para Windows Vista o posterior).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Crear un Administrador de dispositivos WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697177"
---
# <a name="creating-a-wia-device-manager"></a><span data-ttu-id="c67ad-103">Crear un Administrador de dispositivos WIA</span><span class="sxs-lookup"><span data-stu-id="c67ad-103">Creating a WIA Device Manager</span></span>

<span data-ttu-id="c67ad-104">El primer paso para usar los servicios de adquisición de imágenes de Windows (WIA) es obtener un puntero de interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (si está programando para Windows XP o versiones anteriores) o un puntero de interfaz [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (si está programando para Windows Vista o posterior).</span><span class="sxs-lookup"><span data-stu-id="c67ad-104">The first step in using Windows Image Acquisition (WIA) services is to obtain an [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) interface pointer (if you are programming for Windows XP or earlier) or an [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface pointer (if you are programming for Windows Vista or later).</span></span> <span data-ttu-id="c67ad-105">Para ello, llame a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con los parámetros adecuados.</span><span class="sxs-lookup"><span data-stu-id="c67ad-105">To do this, call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the appropriate parameters.</span></span> <span data-ttu-id="c67ad-106">La aplicación de ejemplo WiaSSamp crea un administrador de dispositivos dentro de una función global implementada por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="c67ad-106">The sample application WiaSSamp creates a device manager within a global function implemented by the following code:</span></span>


```
    HRESULT CreateWiaDeviceManager( IWiaDevMgr **ppWiaDevMgr ) //XP or earlier
    HRESULT CreateWiaDeviceManager( IWiaDevMgr2 **ppWiaDevMgr ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == ppWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevMgr = NULL;

        //
        // Create an instance of the device manager
        //
        
        //XP or earlier:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr, (void**)ppWiaDevMgr );

        //Vista or later:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr2, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr2, (void**)ppWiaDevMgr ); 

        //
        // Return the result of creating the device manager
        //
        return hr;
    }
```



<span data-ttu-id="c67ad-107">En este ejemplo, CLSID \_ WiaDevMgr y IID \_ IWiaDevMgr son constantes de WIA que representan el identificador de clase y el identificador de interfaz de [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c67ad-107">In this example, CLSID\_WiaDevMgr and IID\_IWiaDevMgr are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectively.</span></span> <span data-ttu-id="c67ad-108">CLSID \_ WiaDevMgr2 y IID \_ IWiaDevMgr2 son constantes de WIA que representan el identificador de clase y el identificador de interfaz de [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c67ad-108">CLSID\_WiaDevMgr2 and IID\_IWiaDevMgr2 are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectively.</span></span>

<span data-ttu-id="c67ad-109">El valor del argumento *dwClsContext* de la llamada a [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) debe ser CLSCTX \_ local \_ Server.</span><span class="sxs-lookup"><span data-stu-id="c67ad-109">The value for the *dwClsContext* argument of the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call must be CLSCTX\_LOCAL\_SERVER.</span></span> <span data-ttu-id="c67ad-110">No se admite ningún otro tipo de servidor y el modelo de objetos componentes (COM) rechaza cualquier otro valor para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="c67ad-110">No other server type is supported, and Component Object Model (COM) rejects any other value for this parameter.</span></span>

 

 
