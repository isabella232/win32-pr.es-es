---
description: La interfaz IAMTimeline proporciona métodos para manipular la escala de tiempo, el objeto central en los servicios de edición de Microsoft DirectShow (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interfaz IAMTimeline (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680978"
---
# <a name="iamtimeline-interface"></a><span data-ttu-id="4b130-103">Interfaz IAMTimeline</span><span class="sxs-lookup"><span data-stu-id="4b130-103">IAMTimeline interface</span></span>

> [!Note]  
> <span data-ttu-id="4b130-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4b130-104">\[Deprecated.</span></span> <span data-ttu-id="4b130-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b130-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4b130-106">La `IAMTimeline` interfaz proporciona métodos para manipular la escala de tiempo, el objeto central en los [servicios de edición](directshow-editing-services.md) de Microsoft DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="4b130-106">The `IAMTimeline` interface provides methods for manipulating the timeline, the central object in Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="4b130-107">Una escala de tiempo es una colección de elementos ordenados por tiempo, como clips de vídeo, clips de audio, efectos y transiciones entre clips.</span><span class="sxs-lookup"><span data-stu-id="4b130-107">A timeline is a collection of time-ordered elements, such as video clips, audio clips, effects, and transitions between clips.</span></span> <span data-ttu-id="4b130-108">El motor de representación utiliza la escala de tiempo para crear un gráfico de filtro, desde el que la aplicación puede generar la salida representada.</span><span class="sxs-lookup"><span data-stu-id="4b130-108">The render engine uses the timeline to create a filter graph, from which the application can generate the rendered output.</span></span>

<span data-ttu-id="4b130-109">`IAMTimeline` realiza tres servicios básicos.</span><span class="sxs-lookup"><span data-stu-id="4b130-109">`IAMTimeline` performs three basic services.</span></span> <span data-ttu-id="4b130-110">It</span><span class="sxs-lookup"><span data-stu-id="4b130-110">It</span></span>

-   <span data-ttu-id="4b130-111">Crea los objetos en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-111">Creates the objects in the timeline.</span></span>
-   <span data-ttu-id="4b130-112">Actúa como contenedor de esos objetos.</span><span class="sxs-lookup"><span data-stu-id="4b130-112">Acts as a container for those objects.</span></span>
-   <span data-ttu-id="4b130-113">Establece y recupera los parámetros generales de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-113">Sets and retrieves general parameters of the timeline.</span></span>

<span data-ttu-id="4b130-114">Para crear el objeto Timeline, llame a **CoCreateInstance** con el identificador de clase CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="4b130-114">To create the timeline object, call **CoCreateInstance** with the class identifier CLSID\_AMTimeline.</span></span>

## <a name="members"></a><span data-ttu-id="4b130-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b130-115">Members</span></span>

<span data-ttu-id="4b130-116">La interfaz **IAMTimeline** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4b130-116">The **IAMTimeline** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4b130-117">**IAMTimeline** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4b130-117">**IAMTimeline** also has these types of members:</span></span>

-   [<span data-ttu-id="4b130-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b130-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b130-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b130-119">Methods</span></span>

<span data-ttu-id="4b130-120">La interfaz **IAMTimeline** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4b130-120">The **IAMTimeline** interface has these methods.</span></span>



| <span data-ttu-id="4b130-121">Método</span><span class="sxs-lookup"><span data-stu-id="4b130-121">Method</span></span>                                                             | <span data-ttu-id="4b130-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b130-122">Description</span></span>                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b130-123">**AddGroup**</span><span class="sxs-lookup"><span data-stu-id="4b130-123">**AddGroup**</span></span>](iamtimeline-addgroup.md)                           | <span data-ttu-id="4b130-124">Agrega un grupo a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-124">Adds a group to the timeline.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4b130-125">**ClearAllGroups**</span><span class="sxs-lookup"><span data-stu-id="4b130-125">**ClearAllGroups**</span></span>](iamtimeline-clearallgroups.md)               | <span data-ttu-id="4b130-126">Quita todos los grupos de la escala de tiempo, junto con todos los objetos contenidos en esos grupos.</span><span class="sxs-lookup"><span data-stu-id="4b130-126">Removes all groups from the timeline, along with all objects contained in those groups.</span></span><br/>                                |
| [<span data-ttu-id="4b130-127">**CreateEmptyNode**</span><span class="sxs-lookup"><span data-stu-id="4b130-127">**CreateEmptyNode**</span></span>](iamtimeline-createemptynode.md)             | <span data-ttu-id="4b130-128">Crea un nuevo objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="4b130-128">Creates a new timeline object.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4b130-129">**EffectsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4b130-129">**EffectsEnabled**</span></span>](iamtimeline-effectsenabled.md)               | <span data-ttu-id="4b130-130">Determina si los efectos están habilitados.</span><span class="sxs-lookup"><span data-stu-id="4b130-130">Determines whether effects are enabled.</span></span><br/>                                                                                |
| [<span data-ttu-id="4b130-131">**EnableEffects**</span><span class="sxs-lookup"><span data-stu-id="4b130-131">**EnableEffects**</span></span>](iamtimeline-enableeffects.md)                 | <span data-ttu-id="4b130-132">Habilita o deshabilita todos los efectos de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-132">Enables or disables all effects in the timeline.</span></span><br/>                                                                       |
| [<span data-ttu-id="4b130-133">**EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="4b130-133">**EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)         | <span data-ttu-id="4b130-134">Habilita o deshabilita todas las transiciones de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-134">Enables or disables all transitions in the timeline.</span></span><br/>                                                                   |
| [<span data-ttu-id="4b130-135">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="4b130-135">**GetCountOfType**</span></span>](iamtimeline-getcountoftype.md)               | <span data-ttu-id="4b130-136">Recupera el número de objetos del tipo especificado contenidos en un grupo especificado y todos sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="4b130-136">Retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span><br/> |
| [<span data-ttu-id="4b130-137">**GetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="4b130-137">**GetDefaultEffect**</span></span>](iamtimeline-getdefaulteffect.md)           | <span data-ttu-id="4b130-138">Recupera el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4b130-138">Retrieves the default effect.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4b130-139">**GetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="4b130-139">**GetDefaultEffectB**</span></span>](iamtimeline-getdefaulteffectb.md)         | <span data-ttu-id="4b130-140">Recupera el efecto predeterminado como un valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4b130-140">Retrieves the default effect as a **BSTR** value.</span></span><br/>                                                                      |
| [<span data-ttu-id="4b130-141">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="4b130-141">**GetDefaultFPS**</span></span>](iamtimeline-getdefaultfps.md)                 | <span data-ttu-id="4b130-142">Recupera la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4b130-142">Retrieves the default output frame rate, in frames per second.</span></span><br/>                                                         |
| [<span data-ttu-id="4b130-143">**GetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="4b130-143">**GetDefaultTransition**</span></span>](iamtimeline-getdefaulttransition.md)   | <span data-ttu-id="4b130-144">Recupera la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b130-144">Retrieves the default transition.</span></span><br/>                                                                                      |
| [<span data-ttu-id="4b130-145">**GetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="4b130-145">**GetDefaultTransitionB**</span></span>](iamtimeline-getdefaulttransitionb.md) | <span data-ttu-id="4b130-146">Recupera la transición predeterminada como un valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4b130-146">Retrieves the default transition as a **BSTR** value.</span></span><br/>                                                                  |
| [<span data-ttu-id="4b130-147">**GetDirtyRange**</span><span class="sxs-lookup"><span data-stu-id="4b130-147">**GetDirtyRange**</span></span>](iamtimeline-getdirtyrange.md)                 | <span data-ttu-id="4b130-148">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4b130-148">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4b130-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="4b130-149">**GetDuration**</span></span>](iamtimeline-getduration.md)                     | <span data-ttu-id="4b130-150">Recupera la duración de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-150">Retrieves the timeline duration.</span></span><br/>                                                                                       |
| [<span data-ttu-id="4b130-151">**GetDuration2**</span><span class="sxs-lookup"><span data-stu-id="4b130-151">**GetDuration2**</span></span>](iamtimeline-getduration2.md)                   | <span data-ttu-id="4b130-152">Recupera la duración de la escala de tiempo como un **valor Double**.</span><span class="sxs-lookup"><span data-stu-id="4b130-152">Retrieves the timeline duration as a **double**.</span></span><br/>                                                                       |
| [<span data-ttu-id="4b130-153">**GetGroup**</span><span class="sxs-lookup"><span data-stu-id="4b130-153">**GetGroup**</span></span>](iamtimeline-getgroup.md)                           | <span data-ttu-id="4b130-154">Recupera un grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="4b130-154">Retrieves a specified group.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4b130-155">**GetGroupCount**</span><span class="sxs-lookup"><span data-stu-id="4b130-155">**GetGroupCount**</span></span>](iamtimeline-getgroupcount.md)                 | <span data-ttu-id="4b130-156">Recupera el número de grupos contenidos en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-156">Retrieves the number of groups that are contained in the timeline.</span></span><br/>                                                     |
| [<span data-ttu-id="4b130-157">**GetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="4b130-157">**GetInsertMode**</span></span>](iamtimeline-getinsertmode.md)                 | <span data-ttu-id="4b130-158">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4b130-158">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4b130-159">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="4b130-159">**IsDirty**</span></span>](iamtimeline-isdirty.md)                             | <span data-ttu-id="4b130-160">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4b130-160">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4b130-161">**RemGroupFromList**</span><span class="sxs-lookup"><span data-stu-id="4b130-161">**RemGroupFromList**</span></span>](iamtimeline-remgroupfromlist.md)           | <span data-ttu-id="4b130-162">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4b130-162">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4b130-163">**SetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="4b130-163">**SetDefaultEffect**</span></span>](iamtimeline-setdefaulteffect.md)           | <span data-ttu-id="4b130-164">Establece el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4b130-164">Sets the default effect.</span></span><br/>                                                                                               |
| [<span data-ttu-id="4b130-165">**SetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="4b130-165">**SetDefaultEffectB**</span></span>](iamtimeline-setdefaulteffectb.md)         | <span data-ttu-id="4b130-166">Establece el efecto predeterminado como un valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4b130-166">Sets the default effect as a **BSTR** value.</span></span><br/>                                                                           |
| [<span data-ttu-id="4b130-167">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="4b130-167">**SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)                 | <span data-ttu-id="4b130-168">Establece la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4b130-168">Sets the default output frame rate, in frames per second.</span></span><br/>                                                              |
| [<span data-ttu-id="4b130-169">**SetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="4b130-169">**SetDefaultTransition**</span></span>](iamtimeline-setdefaulttransition.md)   | <span data-ttu-id="4b130-170">Establece la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b130-170">Sets the default transition.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4b130-171">**SetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="4b130-171">**SetDefaultTransitionB**</span></span>](iamtimeline-setdefaulttransitionb.md) | <span data-ttu-id="4b130-172">Establece la transición predeterminada como un valor BSTR.</span><span class="sxs-lookup"><span data-stu-id="4b130-172">Sets the default transition as a BSTR value.</span></span><br/>                                                                           |
| [<span data-ttu-id="4b130-173">**SetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="4b130-173">**SetInsertMode**</span></span>](iamtimeline-setinsertmode.md)                 | <span data-ttu-id="4b130-174">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="4b130-174">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4b130-175">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="4b130-175">**SetInterestRange**</span></span>](iamtimeline-setinterestrange.md)           | <span data-ttu-id="4b130-176">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="4b130-176">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4b130-177">**TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4b130-177">**TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)       | <span data-ttu-id="4b130-178">Determina si las transiciones están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="4b130-178">Determines whether transitions are enabled.</span></span><br/>                                                                            |
| [<span data-ttu-id="4b130-179">**ValidateSourceNames**</span><span class="sxs-lookup"><span data-stu-id="4b130-179">**ValidateSourceNames**</span></span>](iamtimeline-validatesourcenames.md)     | <span data-ttu-id="4b130-180">Valida los nombres de origen en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b130-180">Validates source names in the timeline.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="4b130-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b130-181">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4b130-182">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4b130-182">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b130-183">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4b130-183">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4b130-184">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4b130-184">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b130-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b130-185">Requirements</span></span>



| <span data-ttu-id="4b130-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b130-186">Requirement</span></span> | <span data-ttu-id="4b130-187">Value</span><span class="sxs-lookup"><span data-stu-id="4b130-187">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b130-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b130-188">Header</span></span><br/>  | <dl> <span data-ttu-id="4b130-189"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b130-189"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4b130-190">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b130-190">Library</span></span><br/> | <dl> <span data-ttu-id="4b130-191"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b130-191"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
