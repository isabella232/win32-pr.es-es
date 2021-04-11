---
description: Un búfer de profundidad es una propiedad del dispositivo. Para crear un búfer de profundidad administrado por Direct3D, establezca los miembros adecuados de la estructura de \_ parámetros D3DPRESENT como se muestra en el ejemplo de código siguiente.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Crear un búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152882"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a><span data-ttu-id="6c103-104">Crear un búfer de profundidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6c103-104">Creating a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="6c103-105">Un búfer de profundidad es una propiedad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c103-105">A depth buffer is a property of the device.</span></span> <span data-ttu-id="6c103-106">Para crear un búfer de profundidad administrado por Direct3D, establezca los miembros adecuados de la estructura [**de \_ parámetros D3DPRESENT**](d3dpresent-parameters.md) como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="6c103-106">To create a depth buffer that is managed by Direct3D, set the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure as shown in the following code example.</span></span>


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



<span data-ttu-id="6c103-107">Al establecer el miembro EnableAutoDepthStencil en **true**, se indica a Direct3D que administre los búferes de profundidad para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c103-107">By setting the EnableAutoDepthStencil member to **TRUE**, you instruct Direct3D to manage depth buffers for the application.</span></span> <span data-ttu-id="6c103-108">Tenga en cuenta que AutoDepthStencilFormat debe establecerse en un formato de búfer de profundidad válido.</span><span class="sxs-lookup"><span data-stu-id="6c103-108">Note that AutoDepthStencilFormat must be set to a valid depth buffer format.</span></span> <span data-ttu-id="6c103-109">La \_ marca D3DFMT D16 especifica un búfer de profundidad de 16 bits, si hay alguno disponible.</span><span class="sxs-lookup"><span data-stu-id="6c103-109">The D3DFMT\_D16 flag specifies a 16-bit depth buffer, if one is available.</span></span>

<span data-ttu-id="6c103-110">La siguiente llamada al método [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea un dispositivo que después crea un búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6c103-110">The following call to the [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method creates a device that then creates a depth buffer.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



<span data-ttu-id="6c103-111">El búfer de profundidad se establece automáticamente como el destino de representación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c103-111">The depth buffer is automatically set as the render target of the device.</span></span> <span data-ttu-id="6c103-112">Cuando se restablece el dispositivo, el búfer de profundidad se destruye automáticamente y se vuelve a crear con el nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="6c103-112">When the device is reset, the depth buffer is automatically destroyed and re-created in the new size.</span></span>

<span data-ttu-id="6c103-113">Para crear una superficie de búfer de profundidad nueva, use el método [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="6c103-113">To create a new depth buffer surface, use the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) method.</span></span>

<span data-ttu-id="6c103-114">Para establecer una nueva superficie de búfer de profundidad para el dispositivo, use el método [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="6c103-114">To set a new depth-buffer surface for the device, use the [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) method.</span></span>

<span data-ttu-id="6c103-115">Para usar el búfer de profundidad en la aplicación, debe habilitar el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6c103-115">To use the depth buffer in your application, you need to enable the depth buffer.</span></span> <span data-ttu-id="6c103-116">Para obtener más información, vea [Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)](enabling-depth-buffering.md).</span><span class="sxs-lookup"><span data-stu-id="6c103-116">For details, see [Enabling Depth Buffering (Direct3D 9)](enabling-depth-buffering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c103-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c103-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c103-118">Búferes de profundidad</span><span class="sxs-lookup"><span data-stu-id="6c103-118">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
