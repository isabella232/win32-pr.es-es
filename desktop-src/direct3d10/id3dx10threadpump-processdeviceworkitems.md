---
description: Establezca los elementos de trabajo en el dispositivo una vez que hayan finalizado la carga y el procesamiento.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: ID3DX10ThreadPump::P método rocessDeviceWorkItems (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157261"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="137ca-103">ID3DX10ThreadPump::P método rocessDeviceWorkItems</span><span class="sxs-lookup"><span data-stu-id="137ca-103">ID3DX10ThreadPump::ProcessDeviceWorkItems method</span></span>

<span data-ttu-id="137ca-104">Establezca los elementos de trabajo en el dispositivo una vez que hayan finalizado la carga y el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="137ca-104">Set work items to the device after they have finished loading and processing.</span></span> <span data-ttu-id="137ca-105">Cuando el bombeo de subprocesos ha terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en que los elementos procesados se establecerán en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="137ca-105">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="137ca-106">Esto resulta útil para controlar la cantidad de procesamiento que se emplea en los recursos de enlace al dispositivo para cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="137ca-106">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span> <span data-ttu-id="137ca-107">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="137ca-107">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="137ca-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="137ca-108">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="137ca-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="137ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="137ca-110">*iWorkItemCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="137ca-110">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="137ca-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="137ca-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="137ca-112">Número de elementos de trabajo que se van a establecer en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="137ca-112">The number of work items to set to the device.</span></span> <span data-ttu-id="137ca-113">ProcessDeviceObjectCreation creará como máximo objetos iWorkItemCount.</span><span class="sxs-lookup"><span data-stu-id="137ca-113">ProcessDeviceObjectCreation will create at most iWorkItemCount objects.</span></span> <span data-ttu-id="137ca-114">Si no hay suficientes elementos de trabajo en la cola para procesar los objetos iWorkItemCount, ProcessDeviceObjectCreation creará tantos objetos de dispositivo como elementos haya en la cola.</span><span class="sxs-lookup"><span data-stu-id="137ca-114">If there are not enough work items in the queue to process iWorkItemCount objects, ProcessDeviceObjectCreation will create as many device objects as there are items in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="137ca-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="137ca-115">Return value</span></span>

<span data-ttu-id="137ca-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="137ca-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="137ca-117">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="137ca-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="137ca-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="137ca-118">Remarks</span></span>

<span data-ttu-id="137ca-119">Como ejemplo de cómo se puede usar esta API, supuesto que está llegando al final de un nivel del juego y desea comenzar a cargar previamente las texturas, los sombreadores y otros recursos para el siguiente nivel.</span><span class="sxs-lookup"><span data-stu-id="137ca-119">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="137ca-120">El bombeo de subprocesos comenzará a cargar, descomprimir y procesar los recursos y los sombreadores en un subproceso independiente hasta que estén listos para su establecimiento en el dispositivo, momento en el que los dejará en una cola.</span><span class="sxs-lookup"><span data-stu-id="137ca-120">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="137ca-121">Es posible que no quiera establecer todos los recursos y sombreadores en el dispositivo de una sola vez, ya que esto puede provocar que una temporal advertible se ralentice en el rendimiento del juego.</span><span class="sxs-lookup"><span data-stu-id="137ca-121">One may not want to set all the resources and shaders to the device at once because this may cause a noticable temporary slow down in the game's performance.</span></span> <span data-ttu-id="137ca-122">Por lo tanto, se puede llamar a esta API una vez por fotograma para que solo se establezca un número pequeño de elementos de trabajo en el dispositivo en cada fotograma, con lo que se propagará la carga de trabajo de los recursos de enlace al dispositivo a través de varios fotogramas y se minimizará la posibilidad de que una observable se ralentice en el rendimiento del juego.</span><span class="sxs-lookup"><span data-stu-id="137ca-122">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames and minimizing the possibility of a noticable slow down in the game's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="137ca-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="137ca-123">Requirements</span></span>



| <span data-ttu-id="137ca-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="137ca-124">Requirement</span></span> | <span data-ttu-id="137ca-125">Value</span><span class="sxs-lookup"><span data-stu-id="137ca-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="137ca-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="137ca-126">Header</span></span><br/>  | <dl> <span data-ttu-id="137ca-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="137ca-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="137ca-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="137ca-128">Library</span></span><br/> | <dl> <span data-ttu-id="137ca-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="137ca-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="137ca-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="137ca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137ca-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="137ca-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="137ca-132">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="137ca-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
