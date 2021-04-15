---
description: El suavizado de contorno completo de la escena se refiere al desenfoque de los bordes de cada polígono de la escena a medida que se rasteriza en un solo paso; no se requiere ningún segundo paso.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Suavizado de contorno Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536837"
---
# <a name="full-scene-antialiasing-direct3d-9"></a><span data-ttu-id="4eb55-103">Suavizado de contorno Full-Scene (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4eb55-103">Full-Scene Antialiasing (Direct3D 9)</span></span>

<span data-ttu-id="4eb55-104">El suavizado de contorno completo de la escena se refiere al desenfoque de los bordes de cada polígono de la escena a medida que se rasteriza en un solo paso; no se requiere ningún segundo paso.</span><span class="sxs-lookup"><span data-stu-id="4eb55-104">Full-scene antialiasing refers to blurring the edges of each polygon in the scene as it is rasterized in a single pass; no second pass is required.</span></span> <span data-ttu-id="4eb55-105">El suavizado de contorno completo de la escena, cuando se admite, solo afecta a los triángulos y grupos de triángulos.</span><span class="sxs-lookup"><span data-stu-id="4eb55-105">Full-scene antialiasing, when supported, affects only triangles and groups of triangles.</span></span> <span data-ttu-id="4eb55-106">Las líneas no se pueden alisar con los servicios Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4eb55-106">Lines cannot be antialiased by using Direct3D services.</span></span> <span data-ttu-id="4eb55-107">El suavizado de contorno completo de la escena se realiza en Direct3D mediante el muestreo múltiple en cada píxel.</span><span class="sxs-lookup"><span data-stu-id="4eb55-107">Full-scene antialiasing is done in Direct3D by using multisampling on each pixel.</span></span> <span data-ttu-id="4eb55-108">Cuando se habilita el muestreo múltiple, todas las submuestras de un píxel se actualizan en un solo paso, pero cuando se usan para otros efectos que implican varias fases de representación, la aplicación puede especificar que solo se verán afectadas por un paso de representación determinado.</span><span class="sxs-lookup"><span data-stu-id="4eb55-108">When multisampling is enabled, all subsamples of a pixel are updated in one pass but when used for other effects that involve multiple rendering passes, the application can specify that only some subsamples are to be affected by a given rendering pass.</span></span> <span data-ttu-id="4eb55-109">Este último enfoque permite la simulación del desenfoque de movimiento, los efectos de enfoque de profundidad de campo, el desenfoque de reflexión, etc.</span><span class="sxs-lookup"><span data-stu-id="4eb55-109">This latter approach enables simulation of motion blur, depth-of-field focus effects, reflection blur, and so on.</span></span>

<span data-ttu-id="4eb55-110">En ambos casos, los distintos ejemplos registrados para cada píxel se combinan y se envían a la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4eb55-110">In both cases, the various samples recorded for each pixel are blended together and output to the screen.</span></span> <span data-ttu-id="4eb55-111">Esto permite mejorar la calidad de la imagen del suavizado de contorno u otros efectos.</span><span class="sxs-lookup"><span data-stu-id="4eb55-111">This enables the improved image quality of antialiasing or other effects.</span></span>

<span data-ttu-id="4eb55-112">Antes de crear un dispositivo con el método [**IDirect3D9:: CreateDevice**](/windows/desktop/api) , debe determinar si se admite el suavizado de contorno completo de la escena.</span><span class="sxs-lookup"><span data-stu-id="4eb55-112">Before creating a device with the [**IDirect3D9::CreateDevice**](/windows/desktop/api) method, you need to determine if full-scene antialiasing is supported.</span></span> <span data-ttu-id="4eb55-113">Para ello, llame al método [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="4eb55-113">Do this by calling the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method as shown in the code example below.</span></span>


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



<span data-ttu-id="4eb55-114">El primer parámetro que [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) acepta es un número ordinal que denota el adaptador de pantalla que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="4eb55-114">The first parameter that [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepts is an ordinal number that denotes the display adapter to query.</span></span> <span data-ttu-id="4eb55-115">En este ejemplo \_ se usa el valor predeterminado de D3DADAPTER para especificar el adaptador de pantalla principal.</span><span class="sxs-lookup"><span data-stu-id="4eb55-115">This sample uses D3DADAPTER\_DEFAULT to specify the primary display adapter.</span></span> <span data-ttu-id="4eb55-116">El segundo parámetro es un valor del tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) , que especifica el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4eb55-116">The second parameter is a value from the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type, specifying the device type.</span></span> <span data-ttu-id="4eb55-117">El tercer parámetro especifica el formato de la superficie.</span><span class="sxs-lookup"><span data-stu-id="4eb55-117">The third parameter specifies the format of the surface.</span></span> <span data-ttu-id="4eb55-118">El cuarto parámetro indica a Direct3D si se debe consultar sobre el suavizado de contorno completo (**true**) de la ventana completa o el suavizado de contorno de la escena completa (**false**).</span><span class="sxs-lookup"><span data-stu-id="4eb55-118">The fourth parameter tells Direct3D whether to inquire about full-windowed multisampling (**TRUE**) or full-scene antialiasing (**FALSE**).</span></span> <span data-ttu-id="4eb55-119">En este ejemplo se usa **false** para indicar a Direct3D que está consultando el suavizado de contorno completo de la escena.</span><span class="sxs-lookup"><span data-stu-id="4eb55-119">This sample uses **FALSE** to tell Direct3D that it is inquiring about full-scene antialiasing.</span></span> <span data-ttu-id="4eb55-120">El último parámetro especifica la técnica de muestreo múltiple que desea probar.</span><span class="sxs-lookup"><span data-stu-id="4eb55-120">The last parameter specifies the multisampling technique that you want to test.</span></span> <span data-ttu-id="4eb55-121">Use un valor del tipo enumerado [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb55-121">Use a value from the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="4eb55-122">Este ejemplo prueba para ver si se admiten dos niveles de muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="4eb55-122">This sample tests to see if two levels of multisampling are supported.</span></span>

<span data-ttu-id="4eb55-123">Si el dispositivo admite el nivel de muestreo múltiple que quiere usar, el siguiente paso es establecer los parámetros de presentación rellenando los miembros adecuados de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) para crear una superficie de representación de ejemplo múltiple.</span><span class="sxs-lookup"><span data-stu-id="4eb55-123">If the device supports the level of multisampling that you want to use, the next step is to set the presentation parameters by filling in the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to create a multisample rendering surface.</span></span> <span data-ttu-id="4eb55-124">Después, puede crear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4eb55-124">After that, you can create the device.</span></span> <span data-ttu-id="4eb55-125">En el código de ejemplo siguiente se muestra cómo configurar un dispositivo con una superficie de representación de muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="4eb55-125">The sample code below shows how to set up a device with a multisampling render surface.</span></span>


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



<span data-ttu-id="4eb55-126">Para usar el muestreo múltiple, el miembro SwapEffect del \_ parámetro D3DPRESENT debe establecerse en D3DSWAPEFFECT \_ discard.</span><span class="sxs-lookup"><span data-stu-id="4eb55-126">To use multisampling, the SwapEffect member of D3DPRESENT\_PARAMETER must be set to D3DSWAPEFFECT\_DISCARD.</span></span>

<span data-ttu-id="4eb55-127">El último paso es habilitar el suavizado de contorno múltiple llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y establecer el valor de D3DRS \_ MULTISAMPLEANTIALIAS en **true**.</span><span class="sxs-lookup"><span data-stu-id="4eb55-127">The last step is to enable multisampling antialiasing by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and setting the D3DRS\_MULTISAMPLEANTIALIAS to **TRUE**.</span></span> <span data-ttu-id="4eb55-128">Después de establecer este valor en **true**, cualquier representación que realice tendrá aplicado un muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="4eb55-128">After setting this value to **TRUE**, any rendering that you do will have multisampling applied to it.</span></span> <span data-ttu-id="4eb55-129">Puede habilitar y deshabilitar el muestreo múltiple, en función de lo que esté representando.</span><span class="sxs-lookup"><span data-stu-id="4eb55-129">You might want to enable and disable multisampling, depending on what you are rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eb55-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4eb55-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb55-131">Suavizado</span><span class="sxs-lookup"><span data-stu-id="4eb55-131">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 
