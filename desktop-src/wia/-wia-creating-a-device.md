---
description: Una vez que una aplicación tiene el identificador de dispositivo de un dispositivo determinado, puede llamar a IWiaDevMgr::CreateDevice o IWiaDevMgr2::CreateDevicemethod, que crea un árbol jerárquico de objetos IWiaItem o IWiaItem2 que representan un dispositivo de creación de imágenes y la exploración de imágenes y carpetas contenidas en ese dispositivo.
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Creación de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622d22a55c4273dcc13cc1421537b94037a3bb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359628"
---
# <a name="creating-a-device"></a>Creación de un dispositivo

Una vez que una aplicación tiene el identificador de dispositivo de un dispositivo determinado, puede llamar al método [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2::CreateDevice,**](-wia-iwiadevmgr2-createdevice.md)que crea un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) que representan un dispositivo de creación de imágenes y la exploración de imágenes y carpetas contenidas en ese dispositivo.

En el ejemplo siguiente de la aplicación de ejemplo WiaSSamp se implementa una función que toma un identificador de dispositivo como parámetro. Para obtener información sobre cómo obtener un identificador de dispositivo para un dispositivo determinado, vea [Leer las propiedades del dispositivo.](-wia-reading-device-properties.md)


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



En este ejemplo, **pWiaDevMgr** es un puntero a la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) y **ppWiaDevice** es una variable que, después de la llamada a [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o a [**IWiaDevMgr2::CreateDevice),**](-wia-iwiadevmgr2-createdevice.md)contiene la dirección de un puntero al elemento raíz del árbol que representa el dispositivo recién creado.

 

 



