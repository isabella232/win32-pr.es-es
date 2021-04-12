---
description: En Direct3D 9, Direct3D permitirá que el controlador devuelva códigos de error como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY y D3DERR UNSUPPORTEDCOLORARG, de \_ modo que una aplicación pueda responder a ellos.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Errores internos del controlador (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152416"
---
# <a name="driver-internal-errors-direct3d-9"></a><span data-ttu-id="43245-103">Errores internos del controlador (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="43245-103">Driver Internal Errors (Direct3D 9)</span></span>

<span data-ttu-id="43245-104">En Direct3D 9, Direct3D permitirá que el controlador devuelva códigos de error como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY y D3DERR UNSUPPORTEDCOLORARG, de \_ modo que una aplicación pueda responder a ellos.</span><span class="sxs-lookup"><span data-stu-id="43245-104">In Direct3D 9, Direct3D will allow the driver to return error codes such as E\_OUTOFMEMORY, D3DERR\_OUTOFVIDEOMEMORY, and D3DERR\_UNSUPPORTEDCOLORARG so that an application would be able to respond to them.</span></span> <span data-ttu-id="43245-105">Sin embargo, a veces, las llamadas a la API que generaron estos tipos de valor devueltos se cargan en un búfer de comandos y se envían por lotes para enviarlos a la GPU (consulte [control del tiempo de ejecución y optimización](accurately-profiling-direct3d-api-calls.md)de los controladores).</span><span class="sxs-lookup"><span data-stu-id="43245-105">However, sometimes the API calls that generated these return types get loaded into a command buffer and are batched up to be sent to the GPU (see [Controlling Runtime and Driver Optimizations](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="43245-106">En este caso, los errores no se pueden retransmitir a la aplicación cuando es necesario realizar una acción, por lo que el tiempo de ejecución consume el código de error y se realiza una nota en el objeto de dispositivo que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="43245-106">In this case, the errors cannot be relayed to the application when action needs to be taken, so the error code is consumed by the runtime and a note is made on the device object that this happened.</span></span> <span data-ttu-id="43245-107">Más adelante, cuando la aplicación invoque [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::P reenviar** devolverá D3DERR \_ DRIVERINTERNALERROR.</span><span class="sxs-lookup"><span data-stu-id="43245-107">Later when the application invokes [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::Present** will return D3DERR\_DRIVERINTERNALERROR.</span></span> <span data-ttu-id="43245-108">Este es el motivo por el que la mejor opción para que una aplicación lleve a cabo al recibir un \_ DRIVERINTERNALERROR de D3DERR de **IDirect3DDevice9::P reenviados** es destruir y volver a crear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43245-108">This is why the best approach for an application to take when receiving a D3DERR\_DRIVERINTERNALERROR from **IDirect3DDevice9::Present** is to destroy and recreate the device.</span></span>

<span data-ttu-id="43245-109">Si desea intentar depurar más, aquí hay un par de sugerencias para intentar averiguar qué llamada API está generando el error:</span><span class="sxs-lookup"><span data-stu-id="43245-109">If you want to try to debug further, here are a couple of suggestions for trying to figure out which API call is generating the error:</span></span>

-   <span data-ttu-id="43245-110">Dado que la lista de valores devueltos posibles no está completa, puede intentar averiguar en qué llamada se produce un error incluyendo cada llamada de API de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="43245-110">Because the list of possible return values is not complete, you can try to find which call is failing by surrounding each API call like this:</span></span>

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    <span data-ttu-id="43245-111">A continuación, el flujo de depuración de salida debería mostrar la llamada que está causando el problema.</span><span class="sxs-lookup"><span data-stu-id="43245-111">The output debug stream should then show the call that is causing the problem.</span></span>

-   <span data-ttu-id="43245-112">Además, para fines de depuración, intente llamar a [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) inmediatamente antes de cada [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para ver si hay un problema adicional con el controlador de dispositivo (operación no compatible, combinación inutilizable de formatos de textura, etc.).</span><span class="sxs-lookup"><span data-stu-id="43245-112">Additionally, for debugging purposes, try calling [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediately before each [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to see if there is an additional problem with the device driver (unsupported operation, unusable combination of texture formats, etc).</span></span>

    > [!Note]  
    > <span data-ttu-id="43245-113">[**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) debe usarse con cuidado y con moderación debido a la cantidad de trabajo de validación que el controlador debe realizar para devolver una respuesta.</span><span class="sxs-lookup"><span data-stu-id="43245-113">[**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) should be used carefully and sparingly because of the amount of validation work the driver needs to perform to return an answer.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="43245-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43245-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43245-115">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="43245-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
