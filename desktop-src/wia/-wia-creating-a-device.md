---
description: 'Una vez que una aplicación tiene el identificador de dispositivo de un dispositivo determinado, puede llamar a IWiaDevMgr:: CreateDevice o IWiaDevMgr2:: CreateDevicemethod, que crea un árbol jerárquico de objetos IWiaItem o IWiaItem2 que representan un dispositivo de creación de imágenes y las camas de digitalización de imágenes, y las carpetas contenidas en ese dispositivo.'
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Creación de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622d22a55c4273dcc13cc1421537b94037a3bb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697176"
---
# <a name="creating-a-device"></a><span data-ttu-id="bbec9-103">Creación de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="bbec9-103">Creating a Device</span></span>

<span data-ttu-id="bbec9-104">Una vez que una aplicación tiene el identificador de dispositivo de un dispositivo determinado, puede llamar al método [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md), que crea un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) que representan un dispositivo de creación de imágenes y las bases de análisis de imágenes y las carpetas contenidas en ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbec9-104">Once an application has the device ID of a given device, it can call the [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)method, which creates a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects that represent an imaging device and the image scanning beds, and folders contained on that device.</span></span>

<span data-ttu-id="bbec9-105">En el ejemplo siguiente de la aplicación de ejemplo WiaSSamp se implementa una función que toma un identificador de dispositivo como parámetro.</span><span class="sxs-lookup"><span data-stu-id="bbec9-105">The following example from the sample application WiaSSamp implements a function that takes a device ID as a parameter.</span></span> <span data-ttu-id="bbec9-106">Para obtener información sobre cómo obtener un identificador de dispositivo para un dispositivo determinado, consulte [lectura de las propiedades del dispositivo](-wia-reading-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bbec9-106">For information about how to obtain a device ID for a particular device, see [Reading Device Properties](-wia-reading-device-properties.md).</span></span>


```
    //XP or earlier:
    HRESULT CreateWiaDevice( IWiaDevMgr *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem **ppWiaDevice ) 
    //Vista or later:
    HRESULT CreateWiaDevice( IWiaDevMgr2 *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem2 **ppWiaDevice ) 
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr || NULL == bstrDeviceID || NULL == ppWiaDevice)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevice = NULL;

        //
        // Create the WIA Device
        //
        HRESULT hr = pWiaDevMgr->CreateDevice( bstrDeviceID, ppWiaDevice );

        //
        // Return the result of creating the device
        //
        return hr;
    }
```



<span data-ttu-id="bbec9-107">En este ejemplo, **pWiaDevMgr** es un puntero a la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) y **ppWiaDevice** es una variable que, después de la llamada a [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o a [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contiene la dirección de un puntero al elemento raíz del árbol que representa el dispositivo recién creado.</span><span class="sxs-lookup"><span data-stu-id="bbec9-107">In this example, **pWiaDevMgr** is a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface, and **ppWiaDevice** is a variable that, after the call to [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or to [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contains the address of a pointer to the root item of the tree that represents the newly created device.</span></span>

 

 



