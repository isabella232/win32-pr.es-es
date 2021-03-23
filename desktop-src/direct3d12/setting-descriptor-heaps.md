---
title: Establecer y rellenar montones de descriptores
description: Los tipos de montón descriptor que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptor (como máximo una de cada cada vez).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "104549101"
---
# <a name="setting-and-populating-descriptor-heaps"></a><span data-ttu-id="bcdba-103">Establecer y rellenar montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="bcdba-103">Setting and Populating Descriptor Heaps</span></span>

<span data-ttu-id="bcdba-104">Los tipos de montón descriptor que se pueden establecer en una lista de comandos son aquellos que contienen descriptores para los que se pueden usar tablas de descriptor (como máximo una de cada cada vez).</span><span class="sxs-lookup"><span data-stu-id="bcdba-104">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span>

-   [<span data-ttu-id="bcdba-105">Configuración de montones de descriptor</span><span class="sxs-lookup"><span data-stu-id="bcdba-105">Setting descriptor heaps</span></span>](#setting-and-populating-descriptor-heaps)
-   [<span data-ttu-id="bcdba-106">Rellenar montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="bcdba-106">Populating descriptor heaps</span></span>](#populating-descriptor-heaps)
-   [<span data-ttu-id="bcdba-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bcdba-107">Related topics</span></span>](#related-topics)

## <a name="setting-descriptor-heaps"></a><span data-ttu-id="bcdba-108">Configuración de montones de descriptor</span><span class="sxs-lookup"><span data-stu-id="bcdba-108">Setting descriptor heaps</span></span>

<span data-ttu-id="bcdba-109">Los tipos de montón de descriptor que se pueden establecer en una lista de comandos son:</span><span class="sxs-lookup"><span data-stu-id="bcdba-109">The types of descriptor heap that can be set on a command list are:</span></span>

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

<span data-ttu-id="bcdba-110">Los montones que se establecen en la lista de comandos también se deben haber creado como sombreador visible.</span><span class="sxs-lookup"><span data-stu-id="bcdba-110">The heaps being set on the command list must also have been created as shader visible.</span></span> <span data-ttu-id="bcdba-111">Hay tres tipos de lista de comandos: directo, AGRUPAción y proceso.</span><span class="sxs-lookup"><span data-stu-id="bcdba-111">There are three types of command list: DIRECT, BUNDLE, and COMPUTE.</span></span>

<span data-ttu-id="bcdba-112">Una vez establecido un montón de descriptores en una lista de comandos, las llamadas subsiguientes que definen las tablas de descriptores hacen referencia al montón descriptor actual.</span><span class="sxs-lookup"><span data-stu-id="bcdba-112">After a descriptor heap is set on a command list, subsequent calls that define descriptor tables refer to the current descriptor heap.</span></span> <span data-ttu-id="bcdba-113">El estado de la tabla de descriptores es undefined al principio de una lista de comandos y los montones de descriptores se cambian en una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="bcdba-113">Descriptor table state is undefined at the beginning of a command list and after descriptor heaps are changed on a command list.</span></span> <span data-ttu-id="bcdba-114">Establecer el mismo montón de descriptor redundante no hace que la configuración de la tabla de descriptores sea indefinida.</span><span class="sxs-lookup"><span data-stu-id="bcdba-114">Redundantly setting the same descriptor heap does not cause descriptor table settings to be undefined.</span></span>

<span data-ttu-id="bcdba-115">En una agrupación, por el contrario, los montones de descriptor solo se pueden establecer una vez (las llamadas redundantes que establecen el mismo montón dos veces no producen un error). de lo contrario, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="bcdba-115">In a bundle, by contrast, the descriptor heaps can only be set once (redundant calls setting the same heap twice do not produce an error); otherwise, the behavior is undefined.</span></span> <span data-ttu-id="bcdba-116">Los montones de descriptores que se establecen deben coincidir con el estado cuando cualquier lista de comandos llama a la agrupación; de lo contrario, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="bcdba-116">The descriptor heaps that are set must match the state when any command list calls the bundle; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="bcdba-117">Esto permite a los paquetes heredar y editar la configuración de la tabla de descriptores de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="bcdba-117">This allows bundles to inherit and edit the command list’s descriptor table settings.</span></span> <span data-ttu-id="bcdba-118">Los paquetes que no cambian las tablas de descriptores (solo los heredan) no necesitan establecer un montón de descriptores en absoluto y simplemente heredan de la lista de comandos que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="bcdba-118">Bundles that don’t change descriptor tables (only inherit them) don’t need to set a descriptor heap at all and will just inherit from the calling command list.</span></span>

<span data-ttu-id="bcdba-119">Cuando se establecen montones de descriptor (mediante [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), todos los montones que se usan se establecen en una única llamada (y todos los montones establecidos previamente no están establecidos por la llamada).</span><span class="sxs-lookup"><span data-stu-id="bcdba-119">When descriptor heaps are set (using [**ID3D12GraphicsCommandList::SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), all the heaps being used are set in a single call (and all previously set heaps are unset by the call).</span></span> <span data-ttu-id="bcdba-120">Como máximo, se puede establecer en la llamada un montón de cada tipo enumerado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bcdba-120">At most one heap of each type listed above can be set in the call.</span></span>

## <a name="populating-descriptor-heaps"></a><span data-ttu-id="bcdba-121">Rellenar montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="bcdba-121">Populating descriptor heaps</span></span>

<span data-ttu-id="bcdba-122">Después de que una aplicación haya creado un montón de descriptores, puede usar métodos en el dispositivo para generar los descriptores directamente en el montón o en los descriptores de copia de un lugar a otro.</span><span class="sxs-lookup"><span data-stu-id="bcdba-122">After an application has created a descriptor heap, it can then use methods on the device to either generate descriptors directly into the heap or copy descriptors from one place to another.</span></span>

<span data-ttu-id="bcdba-123">El contenido inicial de la memoria del montón de descriptores es indefinido, por lo que pedir a la GPU o al controlador que haga referencia a la memoria no inicializada para la representación puede producir resultados indefinidos, como un restablecimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bcdba-123">The initial contents of descriptor heap memory is undefined, so asking the GPU or driver to reference uninitialized memory for rendering can cause undefined results such as a device reset.</span></span>

<span data-ttu-id="bcdba-124">Si la aplicación configura un montón de descriptores para que sea visible para la CPU, la CPU puede llamar a métodos para crear descriptores en el montón y copiar desde el lugar (incluidos entre montones) de forma inmediata y gratuita.</span><span class="sxs-lookup"><span data-stu-id="bcdba-124">If the application configures a descriptor heap to be CPU visible, then the CPU can call methods to create descriptors into the heap and copy from place to place (including across heaps) in an immediate, free threaded manner.</span></span> <span data-ttu-id="bcdba-125">Si el montón se ha configurado como SHADER_VISIBLE, no se permite la lectura de la CPU.</span><span class="sxs-lookup"><span data-stu-id="bcdba-125">If the heap has been configured as SHADER_VISIBLE, reading by the CPU is not permitted.</span></span>



## <a name="related-topics"></a><span data-ttu-id="bcdba-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bcdba-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcdba-127">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="bcdba-127">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




