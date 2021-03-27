---
title: sincronización (SM5-ASM)
description: Sincronización de grupo de subprocesos o barrera de memoria.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104997000"
---
# <a name="sync-sm5---asm"></a><span data-ttu-id="0a3c7-103">sincronización (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0a3c7-103">sync (sm5 - asm)</span></span>

<span data-ttu-id="0a3c7-104">Sincronización de grupo de subprocesos o barrera de memoria.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-104">Thread group sync or memory barrier.</span></span>



| <span data-ttu-id="0a3c7-105">sincronizar \[ \_ uglobal </span><span class="sxs-lookup"><span data-stu-id="0a3c7-105">sync\[\_uglobal</span></span>\|<span data-ttu-id="0a3c7-106">\_ugroup \] \[ \_ g \] \[ \_ t\]</span><span class="sxs-lookup"><span data-stu-id="0a3c7-106">\_ugroup\]\[\_g\]\[\_t\]</span></span> |
|-------------------------------------------|



 

## <a name="remarks"></a><span data-ttu-id="0a3c7-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a3c7-107">Remarks</span></span>

<span data-ttu-id="0a3c7-108">**Sync** tiene las opciones \_ uglobal, \_ ugroup, \_ g y \_ t.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-108">**Sync** has options \_uglobal, \_ugroup, \_g and \_t.</span></span>

<span data-ttu-id="0a3c7-109">En el sombreador de píxeles, solo se permite la **sincronización de \_ uglobal** .</span><span class="sxs-lookup"><span data-stu-id="0a3c7-109">In the pixel shader, only **sync\_uglobal** is allowed.</span></span>

<span data-ttu-id="0a3c7-110">En el sombreador de cálculo, \_ \_ se deben especificar (uglobal o ugroup \* ) y/o \_ g.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-110">In the compute shader, (\_uglobal or \_ugroup\*) and/or \_g must be specified.</span></span> <span data-ttu-id="0a3c7-111">\_t es opcional además.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-111">\_t is optional in addition.</span></span>

### <a name="_uglobal"></a><span data-ttu-id="0a3c7-112">\_uglobal</span><span class="sxs-lookup"><span data-stu-id="0a3c7-112">\_uglobal</span></span>

<span data-ttu-id="0a3c7-113">Barrera de \# memoria global u (UAV).</span><span class="sxs-lookup"><span data-stu-id="0a3c7-113">Global u\# (UAV) memory fence.</span></span>

<span data-ttu-id="0a3c7-114">Todas las \# lecturas/escrituras de memoria de u anteriores por este subproceso en el orden del programa se hacen visibles a todos los subprocesos de toda la GPU antes de cualquier \# acceso a la memoria u posterior por este subproceso.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-114">All prior u\# memory reads/writes by this thread in program order are made visible to all threads on the entire GPU before any subsequent u\# memory accesses by this thread.</span></span> <span data-ttu-id="0a3c7-115">Toda la parte de la GPU de la definición se sustituye por un ámbito menos que global en un caso, que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-115">The entire GPU part of the definition is replaced by a less-than-global scope in one case, described below.</span></span>

<span data-ttu-id="0a3c7-116">Esto se aplica a toda la memoria UAV enlazada en la fase del sombreador actual.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-116">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="0a3c7-117">\_uglobal está disponible en el sombreador de cálculo o en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-117">\_uglobal is available in the compute shader or pixel shader.</span></span>

<span data-ttu-id="0a3c7-118">En el caso de cualquier UAV enlazado que el sombreador no haya declarado como coherente globalmente, la \_ barrera de memoria de uglobal u \# solo tiene visibilidad dentro del grupo de subprocesos del sombreador de cálculo actual para ese UAV, como si estuviera \_ ugroup en lugar de \_ uglobal.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-118">For any bound UAV that has not been declared by the shader as Globally Coherent, the \_uglobal u\# memory fence only has visibility within the current compute shader thread-group for that UAV, as if it is \_ugroup instead of \_uglobal.</span></span> <span data-ttu-id="0a3c7-119">Este problema solo se aplica al sombreador de cálculo, ya que el sombreador de píxeles debe declarar todos los UAVs como coherentes globalmente.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-119">This issue only applies to the compute shader, since the pixel shader must declare all UAVs as Globally Coherent.</span></span>

### <a name="_ugroup"></a><span data-ttu-id="0a3c7-120">\_ugroup</span><span class="sxs-lookup"><span data-stu-id="0a3c7-120">\_ugroup</span></span>

<span data-ttu-id="0a3c7-121">Límite de memoria del ámbito del grupo de subprocesos u \# (UAV).</span><span class="sxs-lookup"><span data-stu-id="0a3c7-121">Thread group scope u\# (UAV) memory fence.</span></span>

<span data-ttu-id="0a3c7-122">Todas las \# lecturas o escrituras de memoria de u anteriores por este subproceso en el orden del programa se hacen visibles a todos los subprocesos del grupo de subprocesos antes de cualquier \# acceso a la memoria u posterior por parte de este subproceso.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-122">All prior u\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent u\# memory accesses by this thread.</span></span>

<span data-ttu-id="0a3c7-123">Esto se aplica a toda la memoria UAV enlazada en la fase del sombreador actual.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-123">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="0a3c7-124">\_ugroup solo está disponible en el sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-124">\_ugroup is available in the compute shader only.</span></span>

<span data-ttu-id="0a3c7-125">Si \_ se expone ugroup, para algunas implementaciones.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-125">If \_ugroup is exposed, for some implementations.</span></span> <span data-ttu-id="0a3c7-126">La ventaja de especificar \_ ugroup en lugar de \_ uglobal es que la operación de **sincronización** se puede completar con mayor rapidez.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-126">The advantage of specifying \_ugroup instead of \_uglobal is that the **sync** operation can complete more quickly.</span></span>

<span data-ttu-id="0a3c7-127">Otras implementaciones no distinguen \_ ugroup de \_ uglobal, por lo que ambas operaciones son equivalentes y se comportan como \_ uglobal.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-127">Other implementations do not distinguish \_ugroup from \_uglobal, so both operations are equivalent and behave like \_uglobal.</span></span> <span data-ttu-id="0a3c7-128">Las aplicaciones pueden especificar su intención solicitando el ámbito más restringido necesario para la **sincronización** .</span><span class="sxs-lookup"><span data-stu-id="0a3c7-128">Applications can specify their intent by requesting the narrowest scope of **sync** necessary.</span></span>

<span data-ttu-id="0a3c7-129">Aunque un UAV determinado se declare como coherente globalmente, una \_ operación de **sincronización** de ugroup funcionará de manera más eficaz en ese UAV si no se requiere una barrera global.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-129">Even if a particular UAV is declared as Globally Coherent, a \_ugroup **sync** operation will function more efficiently on that UAV if a global barrier is not required.</span></span>

### <a name="_g"></a><span data-ttu-id="0a3c7-130">\_i</span><span class="sxs-lookup"><span data-stu-id="0a3c7-130">\_g</span></span>

<span data-ttu-id="0a3c7-131">\#barrera g (memoria compartida del grupo de subprocesos).</span><span class="sxs-lookup"><span data-stu-id="0a3c7-131">g\# (thread group shared memory) fence.</span></span>

<span data-ttu-id="0a3c7-132">Todas las \# lecturas o escrituras anteriores de la memoria de g realizadas por este subproceso en el orden del programa se hacen visibles a todos los subprocesos del grupo de subprocesos antes de cualquier \# acceso posterior a la memoria de g por este subproceso.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-132">All prior g\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent g\# memory accesses by this thread.</span></span>

<span data-ttu-id="0a3c7-133">Esto se aplica a toda la memoria compartida de g del grupo de subprocesos actual \# .</span><span class="sxs-lookup"><span data-stu-id="0a3c7-133">This applies to all of the current thread group's g\# shared memory.</span></span>

<span data-ttu-id="0a3c7-134">\_g solo está disponible en el sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-134">\_g is available in the compute shader only.</span></span>

### <a name="_t"></a><span data-ttu-id="0a3c7-135">\_t</span><span class="sxs-lookup"><span data-stu-id="0a3c7-135">\_t</span></span>

<span data-ttu-id="0a3c7-136">Sincronización de grupo de subprocesos. Todos los subprocesos dentro de un único grupo de subprocesos (aquellos que pueden compartir el acceso a un conjunto común de espacio de registro compartido) se ejecutarán hasta el punto en el que lleguen a esta instrucción antes de que cualquier subproceso pueda continuar.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-136">Thread group sync. All threads within a single thread group (those that can share access to a common set of shared register space) will be executed up to the point where they reach this instruction before any thread can continue.</span></span>

<span data-ttu-id="0a3c7-137">\_no se puede colocar en el control de flujo dinámico (ramas que podrían variar dentro de un grupo de subprocesos), pero pueden estar presentes en el control de flujo uniforme, donde todos los subprocesos del grupo seleccionan la misma ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-137">\_t cannot be placed in dynamic flow control, (branches which could vary within a thread group), but can be present in uniform flow control, where all threads in the group pick the same path.</span></span>

<span data-ttu-id="0a3c7-138">\_t solo está disponible en el sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-138">\_t is available in the compute shader only.</span></span>

<span data-ttu-id="0a3c7-139">A continuación se muestra una lista de variantes del sombreador de cálculo ' Sync '.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-139">The following is a listing of compute shader ‘sync’ variants.</span></span>

-   <span data-ttu-id="0a3c7-140">sincronizar \_ g</span><span class="sxs-lookup"><span data-stu-id="0a3c7-140">sync\_g</span></span>
-   <span data-ttu-id="0a3c7-141">sincronizar \_ ugroup\*</span><span class="sxs-lookup"><span data-stu-id="0a3c7-141">sync\_ugroup\*</span></span>
-   <span data-ttu-id="0a3c7-142">sincronizar \_ uglobal</span><span class="sxs-lookup"><span data-stu-id="0a3c7-142">sync\_uglobal</span></span>
-   <span data-ttu-id="0a3c7-143">sincronizar \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="0a3c7-143">sync\_g\_t</span></span>
-   <span data-ttu-id="0a3c7-144">sincronizar \_ ugroup \_ t\*</span><span class="sxs-lookup"><span data-stu-id="0a3c7-144">sync\_ugroup\_t\*</span></span>
-   <span data-ttu-id="0a3c7-145">sincronizar \_ uglobal \_ t</span><span class="sxs-lookup"><span data-stu-id="0a3c7-145">sync\_uglobal\_t</span></span>
-   <span data-ttu-id="0a3c7-146">sincronizar \_ ugroup \_ g\*</span><span class="sxs-lookup"><span data-stu-id="0a3c7-146">sync\_ugroup\_g\*</span></span>
-   <span data-ttu-id="0a3c7-147">sincronizar \_ uglobal \_ g</span><span class="sxs-lookup"><span data-stu-id="0a3c7-147">sync\_uglobal\_g</span></span>
-   <span data-ttu-id="0a3c7-148">sincronizar \_ ugroup \_ g \_ t\*</span><span class="sxs-lookup"><span data-stu-id="0a3c7-148">sync\_ugroup\_g\_t\*</span></span>
-   <span data-ttu-id="0a3c7-149">sincronizar \_ uglobal \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="0a3c7-149">sync\_uglobal\_g\_t</span></span>

<span data-ttu-id="0a3c7-150">\*\_Es posible que las variantes con ugroup no sean el destino del compilador de HLSL, según la explicación anterior en la \_ sección ugroup anterior.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-150">\*Variants with \_ugroup may not be targeted by the HLSL compiler, per the earlier discussion in the \_ugroup section above.</span></span>

<span data-ttu-id="0a3c7-151">La lista de variantes de sincronización del sombreador de píxeles incluye \_ solo uglobal de sincronización.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-151">Listing of pixel shader sync variants include sync\_uglobal only.</span></span>

<span data-ttu-id="0a3c7-152">Las barreras de memoria impiden que las instrucciones afectadas se reordenen mediante compiladores o hardware a través de la barrera.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-152">Memory fences prevent affected instructions from being reordered by compilers or hardware across the fence.</span></span>

<span data-ttu-id="0a3c7-153">Varias lecturas de la misma dirección mediante una invocación del sombreador que no están separadas por barreras de memoria o las escrituras en la dirección se pueden contraer juntas.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-153">Multiple reads from the same address by a shader invocation that are not separated by memory barriers or writes to the address can be collapsed together.</span></span> <span data-ttu-id="0a3c7-154">Lo mismo se aplica a las escrituras.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-154">The same applies to writes.</span></span> <span data-ttu-id="0a3c7-155">Los accesos separados por una barrera no se pueden combinar ni pasar por la barrera.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-155">Accesses separated by a barrier cannot be merged or moved across the barrier.</span></span>

<span data-ttu-id="0a3c7-156">Las barreras de memoria no son necesarias para que los distintos subprocesos funcionen correctamente las operaciones atómicas en una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-156">Memory fences are not necessary for atomic operations to a given address by different threads to function correctly.</span></span> <span data-ttu-id="0a3c7-157">Las barreras son necesarias cuando es necesario sincronizar las operaciones atómicas o de carga y almacenamiento con respecto a las demás, tal como aparecen en subprocesos individuales desde el punto de vista de otros subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-157">Fences are needed when atomics and/or load/store operations need to be synchronized with respect to each other as they appear in individual threads from the point of view of other threads.</span></span>

<span data-ttu-id="0a3c7-158">En el sombreador de píxeles, las instrucciones [descartadas](discard--sm4---asm-.md) implican una \_ barrera uglobal de sincronización, en las instrucciones no se pueden reordenar en la **descartar**.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-158">In the pixel shader, [discard](discard--sm4---asm-.md) instructions imply a sync\_uglobal fence, in that instructions cannot be reordered across the **discard**.</span></span> <span data-ttu-id="0a3c7-159">\_la sincronización de uglobal en píxeles auxiliares (que solo se ejecutan para admitir derivados) o los píxeles descartados puede o no tener ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-159">sync\_uglobal in helper pixels (which run only to support derivatives) or discarded pixels may or may not have any affect.</span></span> <span data-ttu-id="0a3c7-160">No se permite que los píxeles auxiliares o descartados escriban en UAVs si, en el caso de discard, las escrituras se emiten después de la descarte.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-160">It is not allowed for helper or discarded pixels to write to UAVs if, in the case of discard, the writes are issued after the discard.</span></span> <span data-ttu-id="0a3c7-161">Los valores devueltos de UAVs no pueden contribuir a cálculos derivados.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-161">Returned values from UAVs are not allowed to contribute to derivative calculations.</span></span> <span data-ttu-id="0a3c7-162">Por lo tanto, tanto si se cumple la sincronización u como si no \_ para los píxeles del ayudante o cuando se emite después de un descarte, se Moot.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-162">Therefore whether or not sync\_u is honored for helper pixels or when issued after a discard is moot.</span></span>

<span data-ttu-id="0a3c7-163">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-163">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="0a3c7-164">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="0a3c7-164">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0a3c7-165">Vértice</span><span class="sxs-lookup"><span data-stu-id="0a3c7-165">Vertex</span></span> | <span data-ttu-id="0a3c7-166">Casco</span><span class="sxs-lookup"><span data-stu-id="0a3c7-166">Hull</span></span> | <span data-ttu-id="0a3c7-167">Dominio</span><span class="sxs-lookup"><span data-stu-id="0a3c7-167">Domain</span></span> | <span data-ttu-id="0a3c7-168">Geometría</span><span class="sxs-lookup"><span data-stu-id="0a3c7-168">Geometry</span></span> | <span data-ttu-id="0a3c7-169">Píxel</span><span class="sxs-lookup"><span data-stu-id="0a3c7-169">Pixel</span></span> | <span data-ttu-id="0a3c7-170">Compute</span><span class="sxs-lookup"><span data-stu-id="0a3c7-170">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0a3c7-171">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-171">X</span></span>     | <span data-ttu-id="0a3c7-172">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-172">X</span></span>       |



 

<span data-ttu-id="0a3c7-173">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, la variante **Sync \_ uglobal** de esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a3c7-173">Because UAVs are available at all shader stages for Direct3D 11.1, the **sync\_uglobal** variant of this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="0a3c7-174">Vértice</span><span class="sxs-lookup"><span data-stu-id="0a3c7-174">Vertex</span></span> | <span data-ttu-id="0a3c7-175">Casco</span><span class="sxs-lookup"><span data-stu-id="0a3c7-175">Hull</span></span> | <span data-ttu-id="0a3c7-176">Dominio</span><span class="sxs-lookup"><span data-stu-id="0a3c7-176">Domain</span></span> | <span data-ttu-id="0a3c7-177">Geometría</span><span class="sxs-lookup"><span data-stu-id="0a3c7-177">Geometry</span></span> | <span data-ttu-id="0a3c7-178">Píxel</span><span class="sxs-lookup"><span data-stu-id="0a3c7-178">Pixel</span></span> | <span data-ttu-id="0a3c7-179">Compute</span><span class="sxs-lookup"><span data-stu-id="0a3c7-179">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0a3c7-180">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-180">X</span></span>      | <span data-ttu-id="0a3c7-181">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-181">X</span></span>    | <span data-ttu-id="0a3c7-182">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-182">X</span></span>      | <span data-ttu-id="0a3c7-183">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-183">X</span></span>        | <span data-ttu-id="0a3c7-184">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-184">X</span></span>     | <span data-ttu-id="0a3c7-185">X</span><span class="sxs-lookup"><span data-stu-id="0a3c7-185">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0a3c7-186">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0a3c7-186">Minimum Shader Model</span></span>

<span data-ttu-id="0a3c7-187">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0a3c7-187">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0a3c7-188">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0a3c7-188">Shader Model</span></span>                                              | <span data-ttu-id="0a3c7-189">Compatible</span><span class="sxs-lookup"><span data-stu-id="0a3c7-189">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0a3c7-190">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0a3c7-190">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0a3c7-191">sí</span><span class="sxs-lookup"><span data-stu-id="0a3c7-191">yes</span></span>       |
| [<span data-ttu-id="0a3c7-192">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0a3c7-192">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0a3c7-193">no</span><span class="sxs-lookup"><span data-stu-id="0a3c7-193">no</span></span>        |
| [<span data-ttu-id="0a3c7-194">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0a3c7-194">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0a3c7-195">no</span><span class="sxs-lookup"><span data-stu-id="0a3c7-195">no</span></span>        |
| [<span data-ttu-id="0a3c7-196">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a3c7-196">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0a3c7-197">no</span><span class="sxs-lookup"><span data-stu-id="0a3c7-197">no</span></span>        |
| [<span data-ttu-id="0a3c7-198">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a3c7-198">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0a3c7-199">no</span><span class="sxs-lookup"><span data-stu-id="0a3c7-199">no</span></span>        |
| [<span data-ttu-id="0a3c7-200">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a3c7-200">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0a3c7-201">no</span><span class="sxs-lookup"><span data-stu-id="0a3c7-201">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0a3c7-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a3c7-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a3c7-203">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a3c7-203">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




