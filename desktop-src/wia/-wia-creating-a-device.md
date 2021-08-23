---
description: Una vez que una aplicación tiene el identificador de dispositivo de un dispositivo determinado, puede llamar a IWiaDevMgr::CreateDevice o IWiaDevMgr2::CreateDevicemethod, que crea un árbol jerárquico de objetos IWiaItem o IWiaItem2 que representan un dispositivo de creación de imágenes y el examen de imágenes y las carpetas contenidas en ese dispositivo.
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Creación de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6319e493c6b99e1f23d8f4ccb9be1e10628fae45e8d4ba7df0aa8112be39dba6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965904"
---
# <a name="creating-a-device"></a>Creación de un dispositivo

Una vez que una aplicación tiene el identificador de dispositivo de un dispositivo determinado, puede llamar al método [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2::CreateDevice,**](-wia-iwiadevmgr2-createdevice.md)que crea un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) que representan un dispositivo de creación de imágenes y el examen de imágenes y las carpetas contenidas en ese dispositivo.

En el ejemplo siguiente de la aplicación de ejemplo WiaSSamp se implementa una función que toma un identificador de dispositivo como parámetro. Para obtener información sobre cómo obtener un identificador de dispositivo para un dispositivo determinado, consulte [Lectura de las propiedades del dispositivo.](-wia-reading-device-properties.md)


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



En este ejemplo, **pWiaDevMgr** es un puntero a la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2,**](-wia-iwiadevmgr2.md) y **ppWiaDevice** es una variable que, después de la llamada a [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o a [**IWiaDevMgr2::CreateDevice),**](-wia-iwiadevmgr2-createdevice.md)contiene la dirección de un puntero al elemento raíz del árbol que representa el dispositivo recién creado.

 

 



