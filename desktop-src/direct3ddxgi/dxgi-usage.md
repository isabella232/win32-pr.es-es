---
description: Marcas para las opciones de creación de recursos y superficie.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707841"
---
# <a name="dxgi_usage"></a><span data-ttu-id="a5534-103">uso de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="a5534-103">DXGI\_USAGE</span></span>

<span data-ttu-id="a5534-104">Marcas para las opciones de creación de recursos y superficie.</span><span class="sxs-lookup"><span data-stu-id="a5534-104">Flags for surface and resource creation options.</span></span>



| <span data-ttu-id="a5534-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="a5534-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="a5534-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5534-106">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <span data-ttu-id="a5534-107"><dt>**DXGI \_ <<  \_ de \_ búfer de reserva de uso**</dt> <dt>1L (2 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-107"><dt>**DXGI\_USAGE\_BACK\_BUFFER**</dt> <dt>1L << (2 + 4)</dt></span></span> </dl>                             | <span data-ttu-id="a5534-108">La superficie o el recurso se utiliza como búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="a5534-108">The surface or resource is used as a back buffer.</span></span> <span data-ttu-id="a5534-109">No es necesario pasar el **\_ búfer de \_ retroceso \_ de uso de DXGI** al crear una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="a5534-109">You don’t need to pass **DXGI\_USAGE\_BACK\_BUFFER** when you create a swap chain.</span></span> <span data-ttu-id="a5534-110">Sin embargo, puede determinar si un recurso pertenece a una cadena de intercambio cuando llama a [**IDXGIResource:: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) y obtiene el **búfer de retroceso de uso de DXGI \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="a5534-110">But you can determine whether a resource belongs to a swap chain when you call [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) and get **DXGI\_USAGE\_BACK\_BUFFER**.</span></span><br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <span data-ttu-id="a5534-111"><dt>**DXGI \_ USO \_ descartado \_ en \_**</dt> la <dt>1L actual <<  (5 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-111"><dt>**DXGI\_USAGE\_DISCARD\_ON\_PRESENT**</dt> <dt>1L << (5 + 4)</dt></span></span> </dl>       | <span data-ttu-id="a5534-112">Esta marca solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="a5534-112">This flag is for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <span data-ttu-id="a5534-113"><dt>**DXGI \_ USO \_ de \_ solo lectura**</dt> <dt>1L <<  (4 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-113"><dt>**DXGI\_USAGE\_READ\_ONLY**</dt> <dt>1L << (4 + 4)</dt></span></span> </dl>                                   | <span data-ttu-id="a5534-114">Use la superficie o el recurso solo para lectura.</span><span class="sxs-lookup"><span data-stu-id="a5534-114">Use the surface or resource for reading only.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <span data-ttu-id="a5534-115"><dt>**DXGI \_ 1L \_ de \_ \_ salida de destino de representación de uso**</dt> <dt> <<  (1 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-115"><dt>**DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT**</dt> <dt>1L << (1 + 4)</dt></span></span> </dl> | <span data-ttu-id="a5534-116">Use la superficie o el recurso como destino de representación de salida.</span><span class="sxs-lookup"><span data-stu-id="a5534-116">Use the surface or resource as an output render target.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <span data-ttu-id="a5534-117"><dt>**DXGI \_ <<  de \_ \_ entrada del sombreador de uso**</dt> <dt>1L (0 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-117"><dt>**DXGI\_USAGE\_SHADER\_INPUT**</dt> <dt>1L << (0 + 4)</dt></span></span> </dl>                          | <span data-ttu-id="a5534-118">Use la superficie o el recurso como entrada para un sombreador.</span><span class="sxs-lookup"><span data-stu-id="a5534-118">Use the surface or resource as an input to a shader.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <span data-ttu-id="a5534-119"><dt>**DXGI \_ USO \_ compartido**</dt> de <dt>1L <<  (3 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-119"><dt>**DXGI\_USAGE\_SHARED**</dt> <dt>1L << (3 + 4)</dt></span></span> </dl>                                             | <span data-ttu-id="a5534-120">Comparta la superficie o el recurso.</span><span class="sxs-lookup"><span data-stu-id="a5534-120">Share the surface or resource.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <span data-ttu-id="a5534-121"><dt>**DXGI \_ \_ \_ Acceso desordenado de uso**</dt> <dt>1L <<  (6 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-121"><dt>**DXGI\_USAGE\_UNORDERED\_ACCESS**</dt> <dt>1L << (6 + 4)</dt></span></span> </dl>              | <span data-ttu-id="a5534-122">Use la superficie o el recurso para el acceso desordenado.</span><span class="sxs-lookup"><span data-stu-id="a5534-122">Use the surface or resource for unordered access.</span></span><br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="a5534-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5534-123">Remarks</span></span>

<span data-ttu-id="a5534-124">Cada marca se define como un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="a5534-124">Each flag is defined as an unsigned integer.</span></span>

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

<span data-ttu-id="a5534-125">Estas opciones de marca se usan en una llamada al método [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) para describir las opciones de uso de la superficie y de acceso a la CPU para el búfer de reserva de una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="a5534-125">These flag options are used in a call to the [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method to describe the surface usage and CPU access options for the back buffer of a swap chain.</span></span> <span data-ttu-id="a5534-126">No puede usar los valores de dxgi uso **\_ \_ compartido**, uso **de dxgi \_ \_ descartar \_ en \_ presente** y **uso de dxgi \_ \_ \_ solo lectura** como entrada para crear una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="a5534-126">You can't use the **DXGI\_USAGE\_SHARED**, **DXGI\_USAGE\_DISCARD\_ON\_PRESENT**, and **DXGI\_USAGE\_READ\_ONLY** values as input to create a swap chain.</span></span> <span data-ttu-id="a5534-127">Sin embargo, DXGI puede **establecer \_ \_ descartar el uso \_ de dxgi en \_ presencia** y **uso de dxgi de \_ \_ \_ solo lectura** para algunos de los búferes de reserva de la cadena de intercambio en nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5534-127">However, DXGI can set **DXGI\_USAGE\_DISCARD\_ON\_PRESENT** and **DXGI\_USAGE\_READ\_ONLY** for some of the swap chain's back buffers on the application's behalf.</span></span> <span data-ttu-id="a5534-128">Puede llamar al método [**IDXGIResource:: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) para recuperar el uso de estos búferes de reserva.</span><span class="sxs-lookup"><span data-stu-id="a5534-128">You can call the [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) method to retrieve the usage of these back buffers.</span></span> <span data-ttu-id="a5534-129">La cadena de intercambio solo admite el valor NONE de acceso de CPU de dxgi en la parte del **campo de acceso de CPU de dxgi \_ \_ \_** del **\_ uso de dxgi**. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a5534-129">Swap chain's only support the **DXGI\_CPU\_ACCESS\_NONE** value in the **DXGI\_CPU\_ACCESS\_FIELD** part of **DXGI\_USAGE**.</span></span>

<span data-ttu-id="a5534-130">Estas opciones de marca también se usan en el método [**IDXGIDevice:: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .</span><span class="sxs-lookup"><span data-stu-id="a5534-130">These flag options are also used by the [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5534-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5534-131">Requirements</span></span>



| <span data-ttu-id="a5534-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5534-132">Requirement</span></span> | <span data-ttu-id="a5534-133">Value</span><span class="sxs-lookup"><span data-stu-id="a5534-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a5534-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5534-134">Header</span></span><br/> | <dl> <span data-ttu-id="a5534-135"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5534-135"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5534-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5534-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5534-137">Constantes de DXGI</span><span class="sxs-lookup"><span data-stu-id="a5534-137">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




