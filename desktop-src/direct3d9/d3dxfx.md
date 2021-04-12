---
description: Opciones para guardar y crear efectos.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151958"
---
# <a name="d3dxfx"></a><span data-ttu-id="d3dbe-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="d3dbe-103">D3DXFX</span></span>

<span data-ttu-id="d3dbe-104">Opciones para guardar y crear efectos.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="d3dbe-105">Las constantes de la tabla siguiente se definen en d3dx9effect. h.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3dbe-106">Estado del efecto guardar y restaurar marcas</span><span class="sxs-lookup"><span data-stu-id="d3dbe-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="d3dbe-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3dbe-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3dbe-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="d3dbe-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="d3dbe-109">No se guarda ningún Estado cuando se llama a <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> o restore cuando se llama a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3dbe-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="d3dbe-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="d3dbe-111">Un stateblock guarda el estado al llamar a <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> y restaura el estado al llamar a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3dbe-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="d3dbe-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="d3dbe-113">Un stateblock guarda el estado (excepto los sombreadores y las constantes del sombreador) al llamar a <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> y restaura el estado cuando se llama a <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3dbe-114">Marcas de creación de efectos</span><span class="sxs-lookup"><span data-stu-id="d3dbe-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="d3dbe-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3dbe-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3dbe-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="d3dbe-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="d3dbe-117">El efecto será no clonable y no contendrá ningún dato binario de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="d3dbe-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> no devolverá punteros de función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="d3dbe-119">La configuración de esta marca reduce el uso de memoria de efecto en aproximadamente el 50% porque elimina la necesidad de que el sistema de efectos mantenga una copia de los sombreadores en la memoria.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="d3dbe-120">Esta marca se usa en <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>y <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3dbe-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="d3dbe-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="d3dbe-122">Habilita la asignación de un recurso de efecto en el espacio de direcciones de uppder de un equipo.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="d3dbe-123">Una limitación importante es que no se pueden usar cadenas y administrar indistintamente.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="d3dbe-124">Por ejemplo, lo siguiente dejará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3dbe-125">En su lugar, se debe usar un método como [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) para almacenar el identificador del parámetro, que se usa para pasar variables al efecto.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d3dbe-126">Las constantes de la tabla siguiente no se definen de forma predeterminada y las debe definir el desarrollador.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3dbe-127">Definición del preprocesador \# de efectos</span><span class="sxs-lookup"><span data-stu-id="d3dbe-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="d3dbe-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3dbe-128">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="d3dbe-129">D3DXFX \_ identificador de LARGEADDRESS \_</span><span class="sxs-lookup"><span data-stu-id="d3dbe-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="d3dbe-130">Defina este valor antes de incluir d3dx9. h para que la aplicación no pueda compilarse al intentar pasar cadenas a los parámetros de D3DXHANDLE.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="d3dbe-131">Esto le ayudará a asegurarse de que se pasa información válida al tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="d3dbe-132">Efectos del enlazador de efectos</span><span class="sxs-lookup"><span data-stu-id="d3dbe-132">Effect Linker Flags</span></span>            | <span data-ttu-id="d3dbe-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3dbe-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="d3dbe-134">\_reconocimiento de direcciones grandes \_</span><span class="sxs-lookup"><span data-stu-id="d3dbe-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="d3dbe-135">Si se establece la marca del enlazador \_ , la dirección grande \_ consciente = 1 permitirá a la aplicación asignar recursos más allá del límite de 2 GB de direcciones cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="d3dbe-136">El sistema de efectos usa bloques de estado para guardar y restaurar el estado automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="d3dbe-137">Para obtener más información sobre los bloques de estado, vea estado de guardado y restauración del estado de los [bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="d3dbe-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3dbe-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3dbe-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3dbe-139">Constantes de efecto</span><span class="sxs-lookup"><span data-stu-id="d3dbe-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



