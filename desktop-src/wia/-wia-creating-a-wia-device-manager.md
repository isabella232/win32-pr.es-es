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
# <a name="creating-a-wia-device-manager"></a>Crear un Administrador de dispositivos WIA

El primer paso para usar los servicios de adquisición de imágenes de Windows (WIA) es obtener un puntero de interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (si está programando para Windows XP o versiones anteriores) o un puntero de interfaz [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (si está programando para Windows Vista o posterior). Para ello, llame a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con los parámetros adecuados. La aplicación de ejemplo WiaSSamp crea un administrador de dispositivos dentro de una función global implementada por el código siguiente:


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



En este ejemplo, CLSID \_ WiaDevMgr y IID \_ IWiaDevMgr son constantes de WIA que representan el identificador de clase y el identificador de interfaz de [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectivamente. CLSID \_ WiaDevMgr2 y IID \_ IWiaDevMgr2 son constantes de WIA que representan el identificador de clase y el identificador de interfaz de [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectivamente.

El valor del argumento *dwClsContext* de la llamada a [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) debe ser CLSCTX \_ local \_ Server. No se admite ningún otro tipo de servidor y el modelo de objetos componentes (COM) rechaza cualquier otro valor para este parámetro.

 

 
