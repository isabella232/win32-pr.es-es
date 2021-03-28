---
title: Interfaz ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Una interfaz de búfer de constantes accede a búferes de constantes o a búferes de textura.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362650"
---
# <a name="id3dx11effectconstantbuffer-interface"></a><span data-ttu-id="99489-105">Interfaz ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="99489-105">ID3DX11EffectConstantBuffer interface</span></span>

<span data-ttu-id="99489-106">Una interfaz de búfer de constantes accede a búferes de constantes o a búferes de textura.</span><span class="sxs-lookup"><span data-stu-id="99489-106">A constant-buffer interface accesses constant buffers or texture buffers.</span></span>

## <a name="members"></a><span data-ttu-id="99489-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="99489-107">Members</span></span>

<span data-ttu-id="99489-108">La interfaz **ID3DX11EffectConstantBuffer** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="99489-108">The **ID3DX11EffectConstantBuffer** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="99489-109">**ID3DX11EffectConstantBuffer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="99489-109">**ID3DX11EffectConstantBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="99489-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="99489-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="99489-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="99489-111">Methods</span></span>

<span data-ttu-id="99489-112">La interfaz **ID3DX11EffectConstantBuffer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="99489-112">The **ID3DX11EffectConstantBuffer** interface has these methods.</span></span>



| <span data-ttu-id="99489-113">Método</span><span class="sxs-lookup"><span data-stu-id="99489-113">Method</span></span>                                                                             | <span data-ttu-id="99489-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="99489-114">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="99489-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="99489-115">**GetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-getconstantbuffer.md)         | <span data-ttu-id="99489-116">Obtiene un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="99489-116">Get a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="99489-117">**GetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="99489-117">**GetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-gettexturebuffer.md)           | <span data-ttu-id="99489-118">Obtiene un búfer de textura.</span><span class="sxs-lookup"><span data-stu-id="99489-118">Get a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="99489-119">**SetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="99489-119">**SetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-setconstantbuffer.md)         | <span data-ttu-id="99489-120">Establezca un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="99489-120">Set a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="99489-121">**SetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="99489-121">**SetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-settexturebuffer.md)           | <span data-ttu-id="99489-122">Establezca un búfer de textura.</span><span class="sxs-lookup"><span data-stu-id="99489-122">Set a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="99489-123">**UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="99489-123">**UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | <span data-ttu-id="99489-124">Revierte un búfer de constantes previamente establecido.</span><span class="sxs-lookup"><span data-stu-id="99489-124">Reverts a previously set constant buffer.</span></span><br/> |
| [<span data-ttu-id="99489-125">**UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="99489-125">**UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | <span data-ttu-id="99489-126">Revierte un búfer de textura previamente establecido.</span><span class="sxs-lookup"><span data-stu-id="99489-126">Reverts a previously set texture buffer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="99489-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99489-127">Remarks</span></span>

<span data-ttu-id="99489-128">Usar búferes de constantes para almacenar muchas constantes de efecto; agrupación de constantes en búferes según su frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="99489-128">Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update.</span></span> <span data-ttu-id="99489-129">Esto le permite minimizar el número de cambios de estado, así como realizar las llamadas de API menos para cambiar el estado.</span><span class="sxs-lookup"><span data-stu-id="99489-129">This allows you to minimize the number of state changes as well as make the fewest API calls to change state.</span></span> <span data-ttu-id="99489-130">Ambos factores conducen a un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="99489-130">Both of these factors lead to better performance.</span></span>

> [!Note]  
> <span data-ttu-id="99489-131">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="99489-131">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="99489-132">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="99489-132">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="99489-133">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="99489-133">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99489-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99489-134">Requirements</span></span>



| <span data-ttu-id="99489-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="99489-135">Requirement</span></span> | <span data-ttu-id="99489-136">Value</span><span class="sxs-lookup"><span data-stu-id="99489-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99489-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99489-137">Header</span></span><br/>  | <dl> <span data-ttu-id="99489-138"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="99489-138"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="99489-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99489-139">Library</span></span><br/> | <dl> <span data-ttu-id="99489-140"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="99489-140"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99489-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="99489-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99489-142">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="99489-142">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="99489-143">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="99489-143">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="99489-144">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="99489-144">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





