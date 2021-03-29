---
description: Como con cualquier característica, es posible que el controlador que utiliza la aplicación no admita todos los tipos de almacenamiento en búfer de profundidad.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Consultar la compatibilidad de búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805293"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a><span data-ttu-id="8e77f-103">Consultar la compatibilidad de búfer de profundidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8e77f-103">Querying for Depth Buffer Support (Direct3D 9)</span></span>

<span data-ttu-id="8e77f-104">Como con cualquier característica, es posible que el controlador que utiliza la aplicación no admita todos los tipos de almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="8e77f-104">As with any feature, the driver that your application uses might not support all types of depth buffering.</span></span> <span data-ttu-id="8e77f-105">Compruebe siempre las capacidades del controlador.</span><span class="sxs-lookup"><span data-stu-id="8e77f-105">Always check the driver's capabilities.</span></span> <span data-ttu-id="8e77f-106">Aunque la mayoría de los controladores admiten el almacenamiento en búfer de profundidad basado en z, no todos admiten el almacenamiento en búfer de profundidad basado en w.</span><span class="sxs-lookup"><span data-stu-id="8e77f-106">Although most drivers support z-based depth buffering, not all will support w-based depth buffering.</span></span> <span data-ttu-id="8e77f-107">Los controladores no producen errores si intenta habilitar un esquema no compatible.</span><span class="sxs-lookup"><span data-stu-id="8e77f-107">Drivers do not fail if you attempt to enable an unsupported scheme.</span></span> <span data-ttu-id="8e77f-108">En su lugar, revierten a otro método de almacenamiento en búfer de profundidad o deshabilitan el almacenamiento en búfer de profundidad por completo, lo que puede dar lugar a que las escenas se representen con artefactos extremos de ordenación de profundidad.</span><span class="sxs-lookup"><span data-stu-id="8e77f-108">They fall back on another depth buffering method instead, or sometimes disable depth buffering altogether, which can result in scenes rendered with extreme depth-sorting artifacts.</span></span>

<span data-ttu-id="8e77f-109">Puede comprobar la compatibilidad general con los búferes de profundidad consultando en Direct3D el dispositivo de pantalla que utilizará la aplicación antes de crear un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8e77f-109">You can check for general support for depth buffers by querying Direct3D for the display device that your application will use before you create a Direct3D device.</span></span> <span data-ttu-id="8e77f-110">Si el objeto de Direct3D informa de que admite el almacenamiento en búfer de profundidad, los dispositivos de hardware que cree a partir de este objeto de Direct3D serán compatibles con el almacenamiento en búfer z.</span><span class="sxs-lookup"><span data-stu-id="8e77f-110">If the Direct3D object reports that it supports depth buffering, any hardware devices you create from this Direct3D object will support z-buffering.</span></span>

<span data-ttu-id="8e77f-111">Para consultar la compatibilidad con el almacenamiento en búfer de profundidad, puede usar el método [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="8e77f-111">To query for depth buffering support, you can use the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) method, as shown in the following code example.</span></span>


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



<span data-ttu-id="8e77f-112">[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) permite elegir un dispositivo para crearlo en función de las capacidades de dicho dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e77f-112">[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="8e77f-113">En este caso, se rechazan los dispositivos que no admiten búferes de profundidad de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e77f-113">In this case, devices that do not support 16-bit depth buffers are rejected.</span></span>

<span data-ttu-id="8e77f-114">En el siguiente ejemplo de código se muestra el uso de [**IDirect3D9:: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) para determinar la compatibilidad de la galería de símbolos de profundidad con un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="8e77f-114">Using [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) to determine depth-stencil compatibility with a render target is illustrated in the following code example.</span></span>


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



<span data-ttu-id="8e77f-115">Cuando sepa que el controlador admite búferes de profundidad, puede comprobar la compatibilidad con el búfer w.</span><span class="sxs-lookup"><span data-stu-id="8e77f-115">When you know that the driver supports depth buffers, you can verify w-buffer support.</span></span> <span data-ttu-id="8e77f-116">Aunque los búferes de profundidad se admiten para todos los rasterizadores de software, los búferes de w solo se admiten en el rasterizador de referencia, que no es adecuado para su uso por parte de aplicaciones del mundo real.</span><span class="sxs-lookup"><span data-stu-id="8e77f-116">Although depth buffers are supported for all software rasterizers, w-buffers are supported only by the reference rasterizer, which is not suited for use by real-world applications.</span></span> <span data-ttu-id="8e77f-117">Independientemente del tipo de dispositivo que use la aplicación, Compruebe la compatibilidad con búferes w antes de intentar habilitar el almacenamiento en búfer de profundidad basado en w.</span><span class="sxs-lookup"><span data-stu-id="8e77f-117">Regardless of the type of device your application uses, verify support for w-buffers before you attempt to enable w-based depth buffering.</span></span>

1.  <span data-ttu-id="8e77f-118">Después de crear el dispositivo, llame al método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) , pasando una estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) inicializada.</span><span class="sxs-lookup"><span data-stu-id="8e77f-118">After creating your device, call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/desktop/api) method, passing an initialized [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>
2.  <span data-ttu-id="8e77f-119">Después de la llamada, el miembro LineCaps contiene información sobre la compatibilidad del controlador con la representación de primitivas.</span><span class="sxs-lookup"><span data-stu-id="8e77f-119">After the call, the LineCaps member contains information about the driver's support for rendering primitives.</span></span>
3.  <span data-ttu-id="8e77f-120">Si el miembro RasterCaps de esta estructura contiene la \_ marca D3DPRASTERCAPS WBUFFER, el controlador admite el almacenamiento en búfer de profundidad basado en w para ese tipo primitivo.</span><span class="sxs-lookup"><span data-stu-id="8e77f-120">If the RasterCaps member of this structure contains the D3DPRASTERCAPS\_WBUFFER flag, then the driver supports w-based depth buffering for that primitive type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e77f-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e77f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e77f-122">Búferes de profundidad</span><span class="sxs-lookup"><span data-stu-id="8e77f-122">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
