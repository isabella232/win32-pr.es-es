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
# <a name="creating-the-device-finder"></a><span data-ttu-id="738af-103">Crear el buscador de dispositivos</span><span class="sxs-lookup"><span data-stu-id="738af-103">Creating the Device Finder</span></span>

<span data-ttu-id="738af-104">En los siguientes ejemplos se muestra cómo crear una instancia del objeto de buscador de dispositivos en C++, Visual Basic y VBScript.</span><span class="sxs-lookup"><span data-stu-id="738af-104">The following examples demonstrate how to create an instance of the Device Finder object in C++, Visual Basic, and VBScript.</span></span> <span data-ttu-id="738af-105">Los lenguajes de script usan el identificador de programación (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para identificar la clase de buscador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="738af-105">The script languages use the programmatic ID (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) to identify the Device Finder class.</span></span> <span data-ttu-id="738af-106">El código de C++ usa el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="738af-106">The C++ code uses the class identifier.</span></span>

## <a name="c-example"></a><span data-ttu-id="738af-107">Ejemplo de C++</span><span class="sxs-lookup"><span data-stu-id="738af-107">C++ Example</span></span>


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



<span data-ttu-id="738af-108">Como indica este ejemplo de C++, el objeto de buscador de dispositivos expone una interfaz predeterminada, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span><span class="sxs-lookup"><span data-stu-id="738af-108">As this C++ example indicates, the Device Finder object exposes a default interface, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span></span> <span data-ttu-id="738af-109">Los métodos de esta interfaz realizan búsquedas según los criterios de búsqueda válidos para un dispositivo basado en UPnP.</span><span class="sxs-lookup"><span data-stu-id="738af-109">The methods of this interface perform searches according to the valid search criteria for a UPnP-based device.</span></span> <span data-ttu-id="738af-110">Esta interfaz es compatible con la automatización, por lo que se puede llamar a sus métodos mediante código de scripting.</span><span class="sxs-lookup"><span data-stu-id="738af-110">This interface is Automation capable, so its methods can be called by scripting code.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="738af-111">Ejemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="738af-111">VBScript Example</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




