---
title: ID3D12CommandQueueDownlevel::P método reenviado
description: Copia el contenido de un recurso de Texture2D de Direct3D 12 en una ventana. | ID3D12CommandQueueDownlevel::P método reenviado
keywords:
- Método Present
- Método Present, interfaz ID3D12CommandQueueDownlevel
- Interfaz ID3D12CommandQueueDownlevel, método present
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721488"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a><span data-ttu-id="87fc3-107">ID3D12CommandQueueDownlevel::P método reenviado</span><span class="sxs-lookup"><span data-stu-id="87fc3-107">ID3D12CommandQueueDownlevel::Present method</span></span>

<span data-ttu-id="87fc3-108">Copia el contenido de un recurso de Texture2D de Direct3D 12 en una ventana.</span><span class="sxs-lookup"><span data-stu-id="87fc3-108">Copies contents from a Direct3D 12 Texture2D resource into a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="87fc3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87fc3-109">Syntax</span></span>

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a><span data-ttu-id="87fc3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87fc3-110">Parameters</span></span>

`pOpenCommandList`

<span data-ttu-id="87fc3-111">Tipo: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="87fc3-111">Type: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="87fc3-112">Una lista de comandos abierta, que Direct3D 12 pone en cola un comando presente y, a continuación, se cierra y se envía automáticamente.</span><span class="sxs-lookup"><span data-stu-id="87fc3-112">An open command list, which Direct3D 12 enqueues a Present command onto, and then closes and submits for you.</span></span>

`pSourceTex2D`

<span data-ttu-id="87fc3-113">Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="87fc3-113">Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="87fc3-114">Un recurso que contiene el contenido deseado que se va a mostrar, con la [**dimensión de recursos Dimension D3D12 \_ \_ \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), y un formato que es uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="87fc3-114">A resource containing your desired contents to display, with dimension [**D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), and a format that is one of the following.</span></span>

* <span data-ttu-id="87fc3-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span><span class="sxs-lookup"><span data-stu-id="87fc3-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span></span>
* <span data-ttu-id="87fc3-116">DXGI_FORMAT_R10G10B10A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="87fc3-116">DXGI_FORMAT_R10G10B10A2_UNORM</span></span>
* <span data-ttu-id="87fc3-117">DXGI_FORMAT_R8G8B8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="87fc3-117">DXGI_FORMAT_R8G8B8A8_UNORM</span></span>
* <span data-ttu-id="87fc3-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="87fc3-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span></span>
* <span data-ttu-id="87fc3-119">DXGI_FORMAT_B8G8R8X8_UNORM</span><span class="sxs-lookup"><span data-stu-id="87fc3-119">DXGI_FORMAT_B8G8R8X8_UNORM</span></span>
* <span data-ttu-id="87fc3-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="87fc3-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span></span>
* <span data-ttu-id="87fc3-121">DXGI_FORMAT_B8G8R8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="87fc3-121">DXGI_FORMAT_B8G8R8A8_UNORM</span></span>
* <span data-ttu-id="87fc3-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="87fc3-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span></span>

`hWindow`

<span data-ttu-id="87fc3-123">Tipo: **[hWnd](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="87fc3-123">Type: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="87fc3-124">Identificador de la ventana en la que se debe mostrar el contenido.</span><span class="sxs-lookup"><span data-stu-id="87fc3-124">The handle to the window where the contents should be displayed.</span></span>

`Flags`

<span data-ttu-id="87fc3-125">Tipo: **[D3D12 \_ de \_ presentación \_ de nivel inferior](d3d12_downlevel_present_flags.md)**</span><span class="sxs-lookup"><span data-stu-id="87fc3-125">Type: **[D3D12\_DOWNLEVEL\_PRESENT\_FLAGS](d3d12_downlevel_present_flags.md)**</span></span>

<span data-ttu-id="87fc3-126">Marcas para modificar la operación **actual** .</span><span class="sxs-lookup"><span data-stu-id="87fc3-126">Flags to modify the **Present** operation.</span></span>

## <a name="return-value"></a><span data-ttu-id="87fc3-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87fc3-127">Return value</span></span>

<span data-ttu-id="87fc3-128">Devuelve **S_OK** si se ejecuta correctamente o, de lo contrario, un HRESULT con error.</span><span class="sxs-lookup"><span data-stu-id="87fc3-128">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="87fc3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87fc3-129">Requirements</span></span>

| <span data-ttu-id="87fc3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="87fc3-130">Requirement</span></span> | <span data-ttu-id="87fc3-131">Value</span><span class="sxs-lookup"><span data-stu-id="87fc3-131">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="87fc3-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87fc3-132">Header</span></span> | <span data-ttu-id="87fc3-133">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="87fc3-133">d3d12downlevel.h</span></span> |
| <span data-ttu-id="87fc3-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87fc3-134">DLL</span></span>    | <span data-ttu-id="87fc3-135">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="87fc3-135">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="87fc3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="87fc3-136">See also</span></span>
* [<span data-ttu-id="87fc3-137">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="87fc3-137">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="87fc3-138">Direct3D 12 en interfaces de Windows 7</span><span class="sxs-lookup"><span data-stu-id="87fc3-138">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="87fc3-139">Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="87fc3-139">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="87fc3-140">Direct3D 12 en Windows 7</span><span class="sxs-lookup"><span data-stu-id="87fc3-140">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
