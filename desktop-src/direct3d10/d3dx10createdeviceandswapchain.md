---
description: Cree el mejor dispositivo Direct3D y una cadena de intercambio.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Función D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362709"
---
# <a name="d3dx10createdeviceandswapchain-function"></a><span data-ttu-id="46235-103">D3DX10CreateDeviceAndSwapChain función)</span><span class="sxs-lookup"><span data-stu-id="46235-103">D3DX10CreateDeviceAndSwapChain function</span></span>

<span data-ttu-id="46235-104">Cree el mejor dispositivo Direct3D y una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="46235-104">Create the best Direct3D device and a swap chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="46235-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46235-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="46235-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46235-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46235-107">*pAdapter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46235-107">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46235-108">Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="46235-108">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="46235-109">Puntero a un [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span><span class="sxs-lookup"><span data-stu-id="46235-109">Pointer to a [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span></span>

</dd> <dt>

<span data-ttu-id="46235-110">*DriverType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46235-110">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46235-111">Tipo: **[ **\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="46235-111">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="46235-112">El tipo de controlador para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46235-112">The type of driver for the device.</span></span> <span data-ttu-id="46235-113">Consulte [**\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span><span class="sxs-lookup"><span data-stu-id="46235-113">See [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span></span>

</dd> <dt>

<span data-ttu-id="46235-114">*Software* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="46235-114">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46235-115">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46235-115">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46235-116">Identificador del archivo DLL que implementa un rasterizador de software.</span><span class="sxs-lookup"><span data-stu-id="46235-116">A handle to the DLL that implements a software rasterizer.</span></span> <span data-ttu-id="46235-117">Debe ser **null** si DriverType es no software.</span><span class="sxs-lookup"><span data-stu-id="46235-117">Must be **NULL** if DriverType is non-software.</span></span> <span data-ttu-id="46235-118">Los HMODULE de un archivo DLL se pueden obtener con [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)o [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="46235-118">The HMODULE of a DLL can be obtained with [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa), or [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="46235-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="46235-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46235-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46235-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46235-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="46235-121">Optional.</span></span> <span data-ttu-id="46235-122">Marcas de creación de dispositivos (consulte [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) que habilitan las [capas de API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="46235-122">Device creation flags (see [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="46235-123">Estas marcas pueden ser OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="46235-123">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="46235-124">*pSwapChainDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46235-124">*pSwapChainDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46235-125">Tipo: **[ **\_ \_ \_ Descripción** de la cadena de intercambio de DXGI](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span><span class="sxs-lookup"><span data-stu-id="46235-125">Type: **[**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span></span>

<span data-ttu-id="46235-126">Descripción de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="46235-126">Description of the swap chain.</span></span> <span data-ttu-id="46235-127">Consulte [**la \_ \_ \_ Descripción**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)de la cadena de intercambio de DXGI.</span><span class="sxs-lookup"><span data-stu-id="46235-127">See [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span></span>

</dd> <dt>

<span data-ttu-id="46235-128">*ppSwapChain* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46235-128">*ppSwapChain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46235-129">Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span><span class="sxs-lookup"><span data-stu-id="46235-129">Type: **[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span></span>

<span data-ttu-id="46235-130">Dirección de un puntero a un [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="46235-130">Address of a pointer to an [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

</dd> <dt>

<span data-ttu-id="46235-131">*ppDevice* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46235-131">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46235-132">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="46235-132">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="46235-133">Dirección de un puntero a una [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) que recibirá el dispositivo recién creado.</span><span class="sxs-lookup"><span data-stu-id="46235-133">Address of a pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) that will receive the newly created device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46235-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46235-134">Return value</span></span>

<span data-ttu-id="46235-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46235-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46235-136">Este método devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="46235-136">This method returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46235-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46235-137">Remarks</span></span>

<span data-ttu-id="46235-138">Para crear el mejor dispositivo, este método implementa más de una opción de creación de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="46235-138">To create the best device, this method implements more than one device creation option.</span></span> <span data-ttu-id="46235-139">En primer lugar, el método intenta crear un dispositivo 10,1 (y una cadena de intercambio).</span><span class="sxs-lookup"><span data-stu-id="46235-139">First, the method attempts to create a 10.1 device (and swap chain).</span></span> <span data-ttu-id="46235-140">Si se produce un error, el método intenta crear un dispositivo 10,0.</span><span class="sxs-lookup"><span data-stu-id="46235-140">If that fails, the method attempts to create a 10.0 device.</span></span> <span data-ttu-id="46235-141">Si se produce un error, se producirá un error en el método.</span><span class="sxs-lookup"><span data-stu-id="46235-141">If that fails, the method will fail.</span></span> <span data-ttu-id="46235-142">Si su aplicación solo necesita crear un dispositivo 10,1 o un dispositivo 10,0, use estas API en su lugar:</span><span class="sxs-lookup"><span data-stu-id="46235-142">If your application needs to create only a 10.1 device, or a 10.0 device only, use these APIs instead:</span></span>

-   <span data-ttu-id="46235-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) para crear un dispositivo Direct3D 10,0 (solo) y una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="46235-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) to create a Direct3D 10.0 (only) device and swap chain.</span></span>
-   <span data-ttu-id="46235-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) para crear un dispositivo Direct3D 10,1 (solo) y una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="46235-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) to create a Direct3D 10.1 (only) device and swap chain.</span></span>

<span data-ttu-id="46235-145">Este método requiere Windows Vista Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46235-145">This method requires Windows Vista Service Pack 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="46235-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46235-146">Requirements</span></span>



| <span data-ttu-id="46235-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="46235-147">Requirement</span></span> | <span data-ttu-id="46235-148">Value</span><span class="sxs-lookup"><span data-stu-id="46235-148">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46235-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46235-149">Header</span></span><br/> | <dl> <span data-ttu-id="46235-150"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="46235-150"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46235-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="46235-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46235-152">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="46235-152">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
