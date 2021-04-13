---
title: Interfaz ID3DX11Effect (D3dx11effect. h)
description: Una interfaz ID3DX11Effect administra un conjunto de objetos de estado, recursos y sombreadores para implementar un efecto de representación.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Interfaz ID3DX11Effect Direct3D 11
- Interfaz ID3DX11Effect Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395946ea4276bc57595abdeb18e7d1755ca0ff1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998598"
---
# <a name="id3dx11effect-interface"></a><span data-ttu-id="e54cc-105">Interfaz ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="e54cc-105">ID3DX11Effect interface</span></span>

<span data-ttu-id="e54cc-106">Una interfaz **ID3DX11Effect** administra un conjunto de objetos de estado, recursos y sombreadores para implementar un efecto de representación.</span><span class="sxs-lookup"><span data-stu-id="e54cc-106">An **ID3DX11Effect** interface manages a set of state objects, resources, and shaders for implementing a rendering effect.</span></span>

## <a name="members"></a><span data-ttu-id="e54cc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e54cc-107">Members</span></span>

<span data-ttu-id="e54cc-108">La interfaz **ID3DX11Effect** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e54cc-108">The **ID3DX11Effect** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e54cc-109">**ID3DX11Effect** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e54cc-109">**ID3DX11Effect** also has these types of members:</span></span>

-   [<span data-ttu-id="e54cc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e54cc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e54cc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e54cc-111">Methods</span></span>

<span data-ttu-id="e54cc-112">La interfaz **ID3DX11Effect** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e54cc-112">The **ID3DX11Effect** interface has these methods.</span></span>



| <span data-ttu-id="e54cc-113">Método</span><span class="sxs-lookup"><span data-stu-id="e54cc-113">Method</span></span>                                                                     | <span data-ttu-id="e54cc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e54cc-114">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e54cc-115">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="e54cc-115">**CloneEffect**</span></span>](id3dx11effect-cloneeffect.md)                           | <span data-ttu-id="e54cc-116">Crea una copia de una interfaz de efecto.</span><span class="sxs-lookup"><span data-stu-id="e54cc-116">Creates a copy of an effect interface.</span></span><br/>                                         |
| [<span data-ttu-id="e54cc-117">**GetClassLinkage**</span><span class="sxs-lookup"><span data-stu-id="e54cc-117">**GetClassLinkage**</span></span>](id3dx11effect-getclasslinkage.md)                   | <span data-ttu-id="e54cc-118">Obtiene una interfaz de vinculación de clases.</span><span class="sxs-lookup"><span data-stu-id="e54cc-118">Gets a class linkage interface.</span></span><br/>                                                |
| [<span data-ttu-id="e54cc-119">**GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="e54cc-119">**GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md) | <span data-ttu-id="e54cc-120">Obtiene un búfer de constantes por índice.</span><span class="sxs-lookup"><span data-stu-id="e54cc-120">Get a constant buffer by index.</span></span><br/>                                                |
| [<span data-ttu-id="e54cc-121">**GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="e54cc-121">**GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)   | <span data-ttu-id="e54cc-122">Obtiene un búfer de constantes por nombre.</span><span class="sxs-lookup"><span data-stu-id="e54cc-122">Get a constant buffer by name.</span></span><br/>                                                 |
| [<span data-ttu-id="e54cc-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="e54cc-123">**GetDesc**</span></span>](id3dx11effect-getdesc.md)                                   | <span data-ttu-id="e54cc-124">Obtiene una descripción de efecto.</span><span class="sxs-lookup"><span data-stu-id="e54cc-124">Get an effect description.</span></span><br/>                                                     |
| [<span data-ttu-id="e54cc-125">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="e54cc-125">**GetDevice**</span></span>](id3dx11effect-getdevice.md)                               | <span data-ttu-id="e54cc-126">Obtiene el dispositivo que creó el efecto.</span><span class="sxs-lookup"><span data-stu-id="e54cc-126">Get the device that created the effect.</span></span><br/>                                        |
| [<span data-ttu-id="e54cc-127">**GetGroupByIndex**</span><span class="sxs-lookup"><span data-stu-id="e54cc-127">**GetGroupByIndex**</span></span>](id3dx11effect-getgroupbyindex.md)                   | <span data-ttu-id="e54cc-128">Obtiene un grupo de efectos por índice.</span><span class="sxs-lookup"><span data-stu-id="e54cc-128">Gets an effect group by index.</span></span><br/>                                                 |
| [<span data-ttu-id="e54cc-129">**GetGroupByName**</span><span class="sxs-lookup"><span data-stu-id="e54cc-129">**GetGroupByName**</span></span>](id3dx11effect-getgroupbyname.md)                     | <span data-ttu-id="e54cc-130">Obtiene un grupo de efectos por nombre.</span><span class="sxs-lookup"><span data-stu-id="e54cc-130">Gets an effect group by name.</span></span><br/>                                                  |
| [<span data-ttu-id="e54cc-131">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="e54cc-131">**GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)           | <span data-ttu-id="e54cc-132">Obtiene una técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="e54cc-132">Get a technique by index.</span></span><br/>                                                      |
| [<span data-ttu-id="e54cc-133">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="e54cc-133">**GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)             | <span data-ttu-id="e54cc-134">Obtener una técnica por nombre.</span><span class="sxs-lookup"><span data-stu-id="e54cc-134">Get a technique by name.</span></span><br/>                                                       |
| [<span data-ttu-id="e54cc-135">**GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="e54cc-135">**GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)             | <span data-ttu-id="e54cc-136">Obtiene una variable por índice.</span><span class="sxs-lookup"><span data-stu-id="e54cc-136">Get a variable by index.</span></span><br/>                                                       |
| [<span data-ttu-id="e54cc-137">**GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="e54cc-137">**GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)               | <span data-ttu-id="e54cc-138">Obtiene una variable por nombre.</span><span class="sxs-lookup"><span data-stu-id="e54cc-138">Get a variable by name.</span></span><br/>                                                        |
| [<span data-ttu-id="e54cc-139">**GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="e54cc-139">**GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)       | <span data-ttu-id="e54cc-140">Obtiene una variable por semántica.</span><span class="sxs-lookup"><span data-stu-id="e54cc-140">Get a variable by semantic.</span></span><br/>                                                    |
| [<span data-ttu-id="e54cc-141">**IsOptimized**</span><span class="sxs-lookup"><span data-stu-id="e54cc-141">**IsOptimized**</span></span>](id3dx11effect-isoptimized.md)                           | <span data-ttu-id="e54cc-142">Pruebe un efecto para ver si los metadatos de reflexión se han quitado de la memoria.</span><span class="sxs-lookup"><span data-stu-id="e54cc-142">Test an effect to see if the reflection metadata has been removed from memory.</span></span><br/> |
| [<span data-ttu-id="e54cc-143">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="e54cc-143">**IsValid**</span></span>](id3dx11effect-isvalid.md)                                   | <span data-ttu-id="e54cc-144">Pruebe un efecto para ver si contiene una sintaxis válida.</span><span class="sxs-lookup"><span data-stu-id="e54cc-144">Test an effect to see if it contains valid syntax.</span></span><br/>                             |
| [<span data-ttu-id="e54cc-145">**Optimización**</span><span class="sxs-lookup"><span data-stu-id="e54cc-145">**Optimize**</span></span>](id3dx11effect-optimize.md)                                 | <span data-ttu-id="e54cc-146">Minimizar la cantidad de memoria necesaria para un efecto.</span><span class="sxs-lookup"><span data-stu-id="e54cc-146">Minimize the amount of memory required for an effect.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="e54cc-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e54cc-147">Remarks</span></span>

<span data-ttu-id="e54cc-148">Un efecto se crea llamando a [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="e54cc-148">An effect is created by calling [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

<span data-ttu-id="e54cc-149">El sistema de efectos agrupa la información necesaria para la representación en un efecto que contiene: objetos de estado para asignar cambios de estado en grupos, recursos para proporcionar datos de entrada y almacenamiento de datos de salida, y programas que controlan cómo se realiza la representación denominado sombreadores.</span><span class="sxs-lookup"><span data-stu-id="e54cc-149">The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders.</span></span>

> [!Note]  
> <span data-ttu-id="e54cc-150">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="e54cc-150">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e54cc-151">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e54cc-151">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e54cc-152">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e54cc-152">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

> [!Note]
>
> <span data-ttu-id="e54cc-153">Si llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un objeto **ID3DX11Effect** para recuperar la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , **QueryInterface** devuelve E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="e54cc-153">If you call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an **ID3DX11Effect** object to retrieve the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, **QueryInterface** returns E\_NOINTERFACE.</span></span> <span data-ttu-id="e54cc-154">Para solucionar este problema, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e54cc-154">To work around this issue, use the following code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="requirements"></a><span data-ttu-id="e54cc-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e54cc-155">Requirements</span></span>
>
> 
>
<span data-ttu-id="e54cc-156">| Requisito | Valor |</span><span class="sxs-lookup"><span data-stu-id="e54cc-156">| Requirement | Value |</span></span>
> <span data-ttu-id="e54cc-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Encabezado</span><span class="sxs-lookup"><span data-stu-id="e54cc-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Header</span></span><br/>  | <dl> <span data-ttu-id="e54cc-158"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e54cc-158"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    <span data-ttu-id="e54cc-159">| | Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e54cc-159">| | Library</span></span><br/> | <dl> <span data-ttu-id="e54cc-160"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="e54cc-160"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |
>
> 
>
> ## <a name="see-also"></a><span data-ttu-id="e54cc-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="e54cc-161">See also</span></span>
>
> <dl> <dt>

[<span data-ttu-id="e54cc-162">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="e54cc-162">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e54cc-163">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="e54cc-163">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>
>
>  
>
>  
>
