---
description: La interfaz ID3DXRenderToEnvMap se usa para generalizar el proceso de representación de mapas de entorno.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interfaz ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649452"
---
# <a name="id3dxrendertoenvmap-interface"></a><span data-ttu-id="9074d-103">Interfaz ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="9074d-103">ID3DXRenderToEnvMap interface</span></span>

<span data-ttu-id="9074d-104">La interfaz ID3DXRenderToEnvMap se usa para generalizar el proceso de representación de mapas de entorno.</span><span class="sxs-lookup"><span data-stu-id="9074d-104">The ID3DXRenderToEnvMap interface is used to generalize the process of rendering to environment maps.</span></span>

## <a name="members"></a><span data-ttu-id="9074d-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="9074d-105">Members</span></span>

<span data-ttu-id="9074d-106">La interfaz **ID3DXRenderToEnvMap** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9074d-106">The **ID3DXRenderToEnvMap** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9074d-107">**ID3DXRenderToEnvMap** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9074d-107">**ID3DXRenderToEnvMap** also has these types of members:</span></span>

-   [<span data-ttu-id="9074d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="9074d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9074d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9074d-109">Methods</span></span>

<span data-ttu-id="9074d-110">La interfaz **ID3DXRenderToEnvMap** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9074d-110">The **ID3DXRenderToEnvMap** interface has these methods.</span></span>



| <span data-ttu-id="9074d-111">Método</span><span class="sxs-lookup"><span data-stu-id="9074d-111">Method</span></span>                                                          | <span data-ttu-id="9074d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9074d-112">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9074d-113">**BeginCube**</span><span class="sxs-lookup"><span data-stu-id="9074d-113">**BeginCube**</span></span>](id3dxrendertoenvmap--begincube.md)             | <span data-ttu-id="9074d-114">Inicie la representación de un mapa de entorno cúbico.</span><span class="sxs-lookup"><span data-stu-id="9074d-114">Initiate the rendering of a cubic environment map.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="9074d-115">**BeginHemisphere**</span><span class="sxs-lookup"><span data-stu-id="9074d-115">**BeginHemisphere**</span></span>](id3dxrendertoenvmap--beginhemisphere.md) | <span data-ttu-id="9074d-116">Inicie la representación de un mapa de entorno de Hemispheric.</span><span class="sxs-lookup"><span data-stu-id="9074d-116">Initiate the rendering of a hemispheric environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="9074d-117">**BeginParabolic**</span><span class="sxs-lookup"><span data-stu-id="9074d-117">**BeginParabolic**</span></span>](id3dxrendertoenvmap--beginparabolic.md)   | <span data-ttu-id="9074d-118">Inicie la representación de un mapa de entorno de parabólica.</span><span class="sxs-lookup"><span data-stu-id="9074d-118">Initiate the rendering of a parabolic environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="9074d-119">**BeginSphere**</span><span class="sxs-lookup"><span data-stu-id="9074d-119">**BeginSphere**</span></span>](id3dxrendertoenvmap--beginsphere.md)         | <span data-ttu-id="9074d-120">Inicie la representación de un mapa de entorno esférico.</span><span class="sxs-lookup"><span data-stu-id="9074d-120">Initiate the rendering of a spherical environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="9074d-121">**Fin**</span><span class="sxs-lookup"><span data-stu-id="9074d-121">**End**</span></span>](id3dxrendertoenvmap--end.md)                         | <span data-ttu-id="9074d-122">Restaure todos los destinos de representación y, si es necesario, componga todas las caras representadas en la superficie del mapa del entorno.</span><span class="sxs-lookup"><span data-stu-id="9074d-122">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span><br/>                                                                           |
| [<span data-ttu-id="9074d-123">**Face**</span><span class="sxs-lookup"><span data-stu-id="9074d-123">**Face**</span></span>](id3dxrendertoenvmap--face.md)                       | <span data-ttu-id="9074d-124">Inicia el dibujo de cada una de las caras de un mapa de entorno.</span><span class="sxs-lookup"><span data-stu-id="9074d-124">Initiate the drawing of each face of an environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="9074d-125">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9074d-125">**GetDesc**</span></span>](id3dxrendertoenvmap--getdesc.md)                 | <span data-ttu-id="9074d-126">Recupera la descripción de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="9074d-126">Retrieves the description of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="9074d-127">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="9074d-127">**GetDevice**</span></span>](id3dxrendertoenvmap--getdevice.md)             | <span data-ttu-id="9074d-128">Recupera el dispositivo Direct3D asociado a la asignación de entorno.</span><span class="sxs-lookup"><span data-stu-id="9074d-128">Retrieves the Direct3D device associated with the environment map.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="9074d-129">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="9074d-129">**OnLostDevice**</span></span>](id3dxrendertoenvmap--onlostdevice.md)       | <span data-ttu-id="9074d-130">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="9074d-130">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="9074d-131">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9074d-131">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="9074d-132">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="9074d-132">**OnResetDevice**</span></span>](id3dxrendertoenvmap--onresetdevice.md)     | <span data-ttu-id="9074d-133">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="9074d-133">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="9074d-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9074d-134">Remarks</span></span>

<span data-ttu-id="9074d-135">Un mapa de entorno se usa para la geometría de la escena de mapa de textura con el fin de proporcionar una escena más sofisticada sin usar geometría compleja.</span><span class="sxs-lookup"><span data-stu-id="9074d-135">An environment map is used to texture-map scene geometry to provide a more sophisticated scene without using complex geometry.</span></span> <span data-ttu-id="9074d-136">Esta interfaz permite crear superficies para los siguientes tipos de geometría: Cube, Half Sphere o Hemispheric, parabólica o Sphere.</span><span class="sxs-lookup"><span data-stu-id="9074d-136">This interface supports creating surfaces for the following kinds of geometry: cube, half sphere or hemispheric, parabolic, or sphere.</span></span>

<span data-ttu-id="9074d-137">La interfaz **ID3DXRenderToEnvMap** se obtiene mediante una llamada a la función [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="9074d-137">The **ID3DXRenderToEnvMap** interface is obtained by calling the [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) function.</span></span>

<span data-ttu-id="9074d-138">El tipo LPD3DXRenderToEnvMap se define como un puntero a la interfaz **ID3DXRenderToEnvMap** .</span><span class="sxs-lookup"><span data-stu-id="9074d-138">The LPD3DXRenderToEnvMap type is defined as a pointer to the **ID3DXRenderToEnvMap** interface.</span></span>


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a><span data-ttu-id="9074d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9074d-139">Requirements</span></span>



| <span data-ttu-id="9074d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9074d-140">Requirement</span></span> | <span data-ttu-id="9074d-141">Value</span><span class="sxs-lookup"><span data-stu-id="9074d-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9074d-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9074d-142">Header</span></span><br/>  | <dl> <span data-ttu-id="9074d-143"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9074d-143"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9074d-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9074d-144">Library</span></span><br/> | <dl> <span data-ttu-id="9074d-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9074d-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9074d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="9074d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9074d-147">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="9074d-147">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
