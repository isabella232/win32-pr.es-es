---
title: Montones de descriptor visibles del sombreador
description: Los montones de descriptor visibles del sombreador, son montones de descriptor a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104280"
---
# <a name="shader-visible-descriptor-heaps"></a><span data-ttu-id="32639-103">Montones de descriptor visibles del sombreador</span><span class="sxs-lookup"><span data-stu-id="32639-103">Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="32639-104">Los montones de descriptor visibles del sombreador, son montones de descriptor a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.</span><span class="sxs-lookup"><span data-stu-id="32639-104">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span>

-   [<span data-ttu-id="32639-105">Información general</span><span class="sxs-lookup"><span data-stu-id="32639-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="32639-106">Un ejemplo</span><span class="sxs-lookup"><span data-stu-id="32639-106">An example</span></span>](#an-example)
-   [<span data-ttu-id="32639-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32639-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="32639-108">Información general</span><span class="sxs-lookup"><span data-stu-id="32639-108">Overview</span></span>

<span data-ttu-id="32639-109">Los montones de descriptor a los que pueden hacer referencia los sombreadores a través de las tablas de descriptores tienen un par de tipos: un tipo de montón, D3D12 \_ SRV \_ UAV \_ CBV de \_ descriptor \_ , puede contener vistas de recursos del sombreador, vistas de acceso desordenado y vistas de búfer de constantes, todo entremezclado.</span><span class="sxs-lookup"><span data-stu-id="32639-109">Descriptor heaps that can be referenced by shaders through descriptor tables come in a couple of flavors: One heap type, D3D12\_SRV\_UAV\_CBV\_DESCRIPTOR\_HEAP, can hold Shader Resource Views, Unordered Access Views, and Constant Buffer Views, all intermixed.</span></span> <span data-ttu-id="32639-110">Cualquier ubicación determinada en el montón puede ser cualquiera de los tipos de descriptores enumerados.</span><span class="sxs-lookup"><span data-stu-id="32639-110">Any given location in the heap can be any one of the listed types of descriptors.</span></span> <span data-ttu-id="32639-111">Otro tipo de montón, \_ \_ \_ la muestra de tipo de montón del descriptor de D3D12 \_ , solo almacena los muestreadores, que reflejan el hecho de que, para la mayoría del hardware, los muestreadores se administran de forma independiente de SRVs, UAVs, CBVs.</span><span class="sxs-lookup"><span data-stu-id="32639-111">Another heap type, D3D12\_DESCRIPTOR\_HEAP\_TYPE\_SAMPLER, only stores samplers, reflecting the fact that for the majority of hardware, samplers are managed separately from SRVs, UAVs, CBVs.</span></span>

<span data-ttu-id="32639-112">Es posible que se solicite a los montones de descriptores de estos tipos que sean visibles para el sombreador o no cuando se cree el montón (el último, que no es un sombreador visible, puede ser útil para descriptores de ensayo en la CPU).</span><span class="sxs-lookup"><span data-stu-id="32639-112">Descriptor heaps of these types may be requested to be shader visible or not when the heap is created (the latter – non shader visible - can be useful for staging descriptors on the CPU).</span></span> <span data-ttu-id="32639-113">Cuando se solicita que el sombreador sea visible, cada uno de los tipos de montones anteriores puede tener un límite de tamaño de hardware para cualquier asignación de montón de descriptor individual.</span><span class="sxs-lookup"><span data-stu-id="32639-113">When requested to be shader visible, each of the above heap types may have a hardware size limit for any individual descriptor heap allocation.</span></span>

<span data-ttu-id="32639-114">Las aplicaciones pueden crear cualquier número de montones de descriptor y los montones de descriptores no visibles de sombreador no tienen restricciones de tamaño.</span><span class="sxs-lookup"><span data-stu-id="32639-114">Applications can create any number of descriptor heaps , and non shader visible descriptor heaps are not constrained in size.</span></span> <span data-ttu-id="32639-115">Si un montón de descriptor visible del sombreador creado por la aplicación es menor que el límite de tamaño del hardware, el controlador puede optar por subasignar el montón del descriptor de un montón de descriptor subyacente más grande para que varios montones de descriptor de la API se ajusten a un montón de descriptores de hardware.</span><span class="sxs-lookup"><span data-stu-id="32639-115">If a shader visible descriptor heap that is created by the application is smaller than the hardware size limit, the driver may choose to sub-allocate the descriptor heap out of a larger underlying descriptor heap so that multiple API descriptor heaps fit within one hardware descriptor heap.</span></span> <span data-ttu-id="32639-116">La razón por la que esto puede ocurrir es que, para un determinado hardware, el cambio entre los montones de descriptores de hardware durante la ejecución requiere un tiempo de espera de GPU para inactivo (para asegurarse de que las referencias de GPU al montón de descriptor anterior se han completado)</span><span class="sxs-lookup"><span data-stu-id="32639-116">The reason this may happen is that for some hardware, switching between hardware descriptor heaps during execution requires a GPU wait for idle (to ensure that GPU references to the previously descriptor heap are finished).</span></span> <span data-ttu-id="32639-117">Si todos los montones de descriptor que crea una aplicación caben en las capacidades máximas del montón de hardware aplicable, entonces no se producirá ninguna espera al cambiar los montones del descriptor de la API durante la representación.</span><span class="sxs-lookup"><span data-stu-id="32639-117">If all of the descriptor heaps that an application creates fit into the applicable hardware heap's maximum capacities, then no such waits will occur when switching API descriptor heaps during rendering.</span></span> <span data-ttu-id="32639-118">Las aplicaciones deben permitir, sin embargo, que el cambio de la pila de descriptores actual pueda incurrir en una espera de inactividad.</span><span class="sxs-lookup"><span data-stu-id="32639-118">Applications must allow for the possibility, however, that switching the current descriptor heap may incur a wait for idle.</span></span>

<span data-ttu-id="32639-119">Para evitar que esto se vea afectado por esta posible espera de inactividad en el modificador del montón del descriptor, las aplicaciones pueden aprovechar las ventajas de los saltos en la representación que harían que la GPU estuviera inactiva por otras razones como el tiempo para realizar los cambios del montón de descriptor, ya que se produce una espera de inactividad.</span><span class="sxs-lookup"><span data-stu-id="32639-119">To avoid being impacted by this possible wait for idle on the descriptor heap switch, applications can take advantage of breaks in rendering that would cause the GPU to idle for other reasons as the time to do descriptor heap switches, since a wait for idle is happening anyway.</span></span>

<span data-ttu-id="32639-120">El mecanismo y la semántica para identificar montones de descriptores en sombreadores durante la grabación de la lista de comandos o el lote se describen en la referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="32639-120">The mechanism and semantics for identifying descriptor heaps to shaders during command list / bundle recording are described in the API reference.</span></span>

## <a name="an-example"></a><span data-ttu-id="32639-121">Un ejemplo</span><span class="sxs-lookup"><span data-stu-id="32639-121">An example</span></span>

<span data-ttu-id="32639-122">En la imagen siguiente se muestran dos montones de descriptor que hacen referencia a dos texturas 2D independientes que se almacenan en dos ranuras de un montón predeterminado de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="32639-122">The image below shows two descriptor heaps referencing two separate 2D textures being stored in two slots of a large default heap.</span></span> <span data-ttu-id="32639-123">La canalización de gráficos (incluidos los sombreadores) puede tener acceso al montón de descriptor que es visible para el sombreador y, por lo tanto, la textura 2D está disponible para la canalización.</span><span class="sxs-lookup"><span data-stu-id="32639-123">The descriptor heap that is shader visible can be accessed by the graphics pipeline (including the shaders), and hence the 2D texture is available to the pipeline.</span></span>

![montones de descriptores visibles y no visibles](images/descriptor-heaps.png)

> [!Note]  
> <span data-ttu-id="32639-125">A menudo hay un límite en el hardware de GPU de la cantidad de memoria local de GPU que se pueda escribir en la CPU (denominada memoria combinada) para los montones de descriptor.</span><span class="sxs-lookup"><span data-stu-id="32639-125">There is often a limit on GPU hardware of the amount of GPU local memory writeable by the CPU (referred to as write-combined memory) for descriptor heaps.</span></span> <span data-ttu-id="32639-126">Normalmente, este límite está alrededor de 96MB para todos los procesos.</span><span class="sxs-lookup"><span data-stu-id="32639-126">Typically this limit is around 96MB for all processes.</span></span> <span data-ttu-id="32639-127">Un montón de descriptores de miembro 1 millón, con descriptores de 32byte, usaría 32 MB, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="32639-127">A one million member descriptor heap, with 32byte descriptors, would use up 32MB, for example.</span></span> <span data-ttu-id="32639-128">Si es necesario, el controlador revertirá la memoria del sistema, aunque es recomendable no crear un gran número de montones de descriptores grandes.</span><span class="sxs-lookup"><span data-stu-id="32639-128">The driver will fall back on system memory if needed, though it is good practice not to create large numbers of large descriptor heaps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="32639-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32639-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32639-130">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="32639-130">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




