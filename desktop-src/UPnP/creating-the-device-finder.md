---
title: Crear el buscador de dispositivos
description: En los siguientes ejemplos se muestra cómo crear una instancia del objeto de buscador de dispositivos en C++, Visual Basic y VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903725"
---
# <a name="creating-the-device-finder"></a>Crear el buscador de dispositivos

En los siguientes ejemplos se muestra cómo crear una instancia del objeto de buscador de dispositivos en C++, Visual Basic y VBScript. Los lenguajes de script usan el identificador de programación (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para identificar la clase de buscador de dispositivos. El código de C++ usa el identificador de clase.

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



Como indica este ejemplo de C++, el objeto de buscador de dispositivos expone una interfaz predeterminada, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder). Los métodos de esta interfaz realizan búsquedas según los criterios de búsqueda válidos para un dispositivo basado en UPnP. Esta interfaz es compatible con la automatización, por lo que se puede llamar a sus métodos mediante código de scripting.

## <a name="vbscript-example"></a>Ejemplo de VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




