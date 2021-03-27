---
title: Método ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Establece los elementos de trabajo en el dispositivo una vez que han finalizado la carga y el procesamiento.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Método ProcessDeviceWorkItems Direct3D 11
- Método ProcessDeviceWorkItems Direct3D 11, interfaz ID3DX11ThreadPump
- Interfaz ID3DX11ThreadPump Direct3D 11, método ProcessDeviceWorkItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986899"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="e1b32-107">ID3DX11ThreadPump::P método rocessDeviceWorkItems</span><span class="sxs-lookup"><span data-stu-id="e1b32-107">ID3DX11ThreadPump::ProcessDeviceWorkItems method</span></span>

> [!Note]  
> <span data-ttu-id="e1b32-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="e1b32-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="e1b32-109">Establece los elementos de trabajo en el dispositivo una vez que han finalizado la carga y el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e1b32-109">Sets work items to the device after they have finished loading and processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b32-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1b32-110">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="e1b32-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1b32-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b32-112">*iWorkItemCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1b32-112">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b32-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1b32-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e1b32-114">Número de elementos de trabajo que se van a establecer en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1b32-114">The number of work items to set to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b32-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1b32-115">Return value</span></span>

<span data-ttu-id="e1b32-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1b32-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1b32-117">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e1b32-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b32-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1b32-118">Remarks</span></span>

<span data-ttu-id="e1b32-119">Cuando el bombeo de subprocesos ha terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en que los elementos procesados se establecerán en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1b32-119">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="e1b32-120">Esto resulta útil para controlar la cantidad de procesamiento que se emplea en los recursos de enlace al dispositivo para cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="e1b32-120">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span>

<span data-ttu-id="e1b32-121">Como ejemplo de cómo se puede usar esta API, supuesto que está llegando al final de un nivel del juego y desea comenzar a cargar previamente las texturas, los sombreadores y otros recursos para el siguiente nivel.</span><span class="sxs-lookup"><span data-stu-id="e1b32-121">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="e1b32-122">El bombeo de subprocesos comenzará a cargar, descomprimir y procesar los recursos y los sombreadores en un subproceso independiente hasta que estén listos para su establecimiento en el dispositivo, momento en el que los dejará en una cola.</span><span class="sxs-lookup"><span data-stu-id="e1b32-122">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="e1b32-123">Es posible que no quiera establecer todos los recursos y sombreadores en el dispositivo de una sola vez, ya que esto puede provocar una disminución temporal apreciable en el rendimiento del juego.</span><span class="sxs-lookup"><span data-stu-id="e1b32-123">One may not want to set all the resources and shaders to the device at once because this may cause a noticeable temporary slow down in the game's performance.</span></span> <span data-ttu-id="e1b32-124">Por lo tanto, se puede llamar a esta API una vez por cada fotograma para que solo se establezca un número pequeño de elementos de trabajo en el dispositivo en cada fotograma, con lo que se propagará la carga de trabajo de los recursos de enlace al dispositivo en varios fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e1b32-124">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b32-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1b32-125">Requirements</span></span>



| <span data-ttu-id="e1b32-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b32-126">Requirement</span></span> | <span data-ttu-id="e1b32-127">Value</span><span class="sxs-lookup"><span data-stu-id="e1b32-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b32-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1b32-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e1b32-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b32-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="e1b32-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1b32-130">Library</span></span><br/> | <dl> <span data-ttu-id="e1b32-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1b32-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1b32-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1b32-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b32-133">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="e1b32-133">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="e1b32-134">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="e1b32-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

