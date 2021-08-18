---
title: Creación del buscador de dispositivos
description: En los ejemplos siguientes se muestra cómo crear una instancia del objeto Device Finder en C++, Visual Basic y VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6af75ea5c267e156f89f1ae1e27a08928c097bbfea731f59add575397fbc00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137364"
---
# <a name="creating-the-device-finder"></a>Creación del buscador de dispositivos

En los ejemplos siguientes se muestra cómo crear una instancia del objeto Device Finder en C++, Visual Basic y VBScript. Los lenguajes de script usan el identificador de programación (ProgID) [**UPnP.UPnPDeviceDevice Para**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) identificar la clase Device Finder. El código de C++ usa el identificador de clase.

## <a name="c-example"></a>Ejemplo de C++


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



Como indica este ejemplo de C++, el objeto Device Finder expone una interfaz predeterminada, [**IUPnPDeviceDevice .**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) Los métodos de esta interfaz realizan búsquedas según los criterios de búsqueda válidos para un dispositivo basado en UPnP. Esta interfaz es compatible con Automation, por lo que se puede llamar a sus métodos mediante código de scripting.

## <a name="vbscript-example"></a>Ejemplo de VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




