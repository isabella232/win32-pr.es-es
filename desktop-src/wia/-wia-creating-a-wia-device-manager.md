---
description: El primer paso para usar los servicios de adquisición de imágenes (WIA) de Windows es obtener un puntero de interfaz IWiaDevMgr (si está programando para Windows XP o versiones anteriores) o un puntero de interfaz IWiaDevMgr2 (si está programando para Windows Vista o posterior).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Creación de un Administrador de dispositivos WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360631"
---
# <a name="creating-a-wia-device-manager"></a>Creación de un Administrador de dispositivos WIA

El primer paso para usar los servicios de adquisición de imágenes (WIA) de Windows es obtener un puntero de interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (si está programando para Windows XP o versiones anteriores) o un puntero de interfaz [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (si está programando para Windows Vista o posterior). Para ello, llame a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con los parámetros adecuados. La aplicación de ejemplo WiaSSamp crea un administrador de dispositivos dentro de una función global implementada por el código siguiente:


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



En este ejemplo, CLSID WiaDevMgr e IID IWiaDevMgr son constantes WIA que representan el identificador de clase y el identificador de interfaz de \_ \_ [**IWiaDevMgr,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)respectivamente. CLSID WiaDevMgr2 e IID IWiaDevMgr2 son constantes WIA que representan el identificador de clase y el identificador de interfaz de \_ \_ [**IWiaDevMgr2,**](-wia-iwiadevmgr2.md)respectivamente.

El valor del argumento *dwClsContext* de la [llamada a CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) debe ser CLSCTX \_ LOCAL \_ SERVER. No se admite ningún otro tipo de servidor y el Modelo de objetos componentes (COM) rechaza cualquier otro valor para este parámetro.

 

 
