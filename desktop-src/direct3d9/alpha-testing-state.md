---
description: Las aplicaciones de C++ pueden usar las pruebas alfa para controlar el momento en que se escriben los píxeles en la superficie de representación-destino.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Estado de la prueba alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714863"
---
# <a name="alpha-testing-state-direct3d-9"></a><span data-ttu-id="b7f00-103">Estado de la prueba alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b7f00-103">Alpha Testing State (Direct3D 9)</span></span>

<span data-ttu-id="b7f00-104">Las aplicaciones de C++ pueden usar las pruebas alfa para controlar el momento en que se escriben los píxeles en la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="b7f00-104">C++ applications can use alpha testing to control when pixels are written to the render-target surface.</span></span> <span data-ttu-id="b7f00-105">Mediante el estado de representación de [**D3DRS \_ ALPHATESTENABLE**](./d3drenderstatetype.md) , la aplicación establece el dispositivo Direct3D actual para que pruebe cada píxel según una función de prueba alfa.</span><span class="sxs-lookup"><span data-stu-id="b7f00-105">By using the [**D3DRS\_ALPHATESTENABLE**](./d3drenderstatetype.md) render state, your application sets the current Direct3D device so that it tests each pixel according to an alpha test function.</span></span> <span data-ttu-id="b7f00-106">Si la prueba se realiza correctamente, el píxel se escribe en la superficie.</span><span class="sxs-lookup"><span data-stu-id="b7f00-106">If the test succeeds, the pixel is written to the surface.</span></span> <span data-ttu-id="b7f00-107">Si no es así, Direct3D omite el píxel.</span><span class="sxs-lookup"><span data-stu-id="b7f00-107">If it does not, Direct3D ignores the pixel.</span></span> <span data-ttu-id="b7f00-108">Seleccione la función de prueba alfa con el estado de representación de **D3DRS \_ ALPHAFUNC** .</span><span class="sxs-lookup"><span data-stu-id="b7f00-108">Select the alpha test function with the **D3DRS\_ALPHAFUNC** render state.</span></span> <span data-ttu-id="b7f00-109">La aplicación puede establecer un valor alfa de referencia para todos los píxeles que se van a comparar mediante el estado de representación de **\_ ALPHAREF de D3DRS** .</span><span class="sxs-lookup"><span data-stu-id="b7f00-109">Your application can set a reference alpha value for all pixels to compare against by using the **D3DRS\_ALPHAREF** render state.</span></span>

<span data-ttu-id="b7f00-110">El uso más común de las pruebas alfa es mejorar el rendimiento al rasterizar objetos que son casi transparentes.</span><span class="sxs-lookup"><span data-stu-id="b7f00-110">The most common use for alpha testing is to improve performance when rasterizing objects that are nearly transparent.</span></span> <span data-ttu-id="b7f00-111">Si los datos de color que se están rasterizando son más opacos que el color de un píxel determinado (D3DPCMPCAPS \_ mayor criticalthreshold), se escribe el píxel.</span><span class="sxs-lookup"><span data-stu-id="b7f00-111">If the color data being rasterized is more opaque than the color at a given pixel (D3DPCMPCAPS\_GREATEREQUAL), then the pixel is written.</span></span> <span data-ttu-id="b7f00-112">De lo contrario, el rasterizador omite el píxel por completo, lo que ahorra el procesamiento necesario para combinar los dos colores.</span><span class="sxs-lookup"><span data-stu-id="b7f00-112">Otherwise, the rasterizer ignores the pixel altogether, saving the processing required to blend the two colors.</span></span> <span data-ttu-id="b7f00-113">En el ejemplo de código siguiente se comprueba si se admite una función de comparación determinada y, si es así, se establecen los parámetros de función de comparación necesarios para mejorar el rendimiento durante la representación.</span><span class="sxs-lookup"><span data-stu-id="b7f00-113">The following code example checks if a given comparison function is supported and, if so, it sets the comparison function parameters required to improve performance during rendering.</span></span>


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



<span data-ttu-id="b7f00-114">No todo el hardware es compatible con todas las características de pruebas alfa.</span><span class="sxs-lookup"><span data-stu-id="b7f00-114">Not all hardware supports all alpha-testing features.</span></span> <span data-ttu-id="b7f00-115">Puede comprobar las funcionalidades del dispositivo llamando al método [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="b7f00-115">You can check the device capabilities by calling the [**IDirect3D9::GetDeviceCaps**](/windows/desktop/api) method.</span></span> <span data-ttu-id="b7f00-116">Después de recuperar las funcionalidades del dispositivo, compruebe el miembro AlphaCmpCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) asociada para la función de comparación deseada.</span><span class="sxs-lookup"><span data-stu-id="b7f00-116">After retrieving the device capabilities, check the associated [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's AlphaCmpCaps member for the desired comparison function.</span></span> <span data-ttu-id="b7f00-117">Si el miembro AlphaCmpCaps contiene solo la capacidad de D3DPCMPCAPS \_ siempre o solo la \_ capacidad de D3DPCMPCAPS nunca, el controlador no admite pruebas alfa.</span><span class="sxs-lookup"><span data-stu-id="b7f00-117">If the AlphaCmpCaps member contains only the D3DPCMPCAPS\_ALWAYS capability or only the D3DPCMPCAPS\_NEVER capability, the driver does not support alpha tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7f00-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7f00-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7f00-119">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="b7f00-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
