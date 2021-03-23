---
title: Subasignación dentro de búferes
description: Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU. En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103841"
---
# <a name="suballocation-within-buffers"></a><span data-ttu-id="92174-104">Subasignación dentro de búferes</span><span class="sxs-lookup"><span data-stu-id="92174-104">Suballocation Within Buffers</span></span>

<span data-ttu-id="92174-105">Los búferes tienen todas las características necesarias en D3D12 para que las aplicaciones transfieran una gran variedad de datos transitorios de la CPU a la GPU.</span><span class="sxs-lookup"><span data-stu-id="92174-105">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="92174-106">En esta sección se tratan cuatro escenarios comunes para el uso y la administración de recursos y búferes.</span><span class="sxs-lookup"><span data-stu-id="92174-106">This section covers four common scenarios for the use and management of resources and buffers.</span></span>

<span data-ttu-id="92174-107">De forma similar a D3D11, las aplicaciones de D3D12 todavía tienen que declarar el uso de memoria cuando se asignan búferes en D3D12 en comparación con recursos dinámicos o de ensayo en D3D11, pero en D3D12, los desarrolladores tienen más flexibilidad y mayor control sobre el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="92174-107">Similar to D3D11, applications in D3D12 still need to declare the usage of memory when allocating buffers in D3D12 compared to Dynamic/Staging Resources in D3D11, but in D3D12, developers have more flexibility and tighter control over memory usage.</span></span> <span data-ttu-id="92174-108">Los búferes, a través de la subasignación, tienen todas las características necesarias para la administración de memoria de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="92174-108">Buffers, through suballocation, have all the features necessary for low-level memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="92174-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="92174-109">In this section</span></span>



| <span data-ttu-id="92174-110">Tema</span><span class="sxs-lookup"><span data-stu-id="92174-110">Topic</span></span>                                                                                        | <span data-ttu-id="92174-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="92174-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92174-112">Cargar diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="92174-112">Uploading Different Types of Resources</span></span>](uploading-resources.md)<br/>                 | <span data-ttu-id="92174-113">Muestra cómo utilizar un búfer para cargar datos de búfer de constantes y datos de búfer de vértices en la GPU, y cómo subasignar y colocar datos correctamente en los búferes.</span><span class="sxs-lookup"><span data-stu-id="92174-113">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="92174-114">El uso de un único búfer aumenta la flexibilidad del uso de memoria y proporciona a las aplicaciones un control más estricto del uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="92174-114">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="92174-115">También se muestran las diferencias entre los modelos D3D11 y D3D12 para cargar diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="92174-115">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span><br/> |
| [<span data-ttu-id="92174-116">Cargar datos de textura a través de búferes</span><span class="sxs-lookup"><span data-stu-id="92174-116">Uploading Texture Data Through Buffers</span></span>](upload-and-readback-of-texture-data.md)<br/> | <span data-ttu-id="92174-117">La carga de datos de textura 2D o 3D es similar a la carga de datos 1D, salvo que las aplicaciones necesitan prestar atención a la alineación de datos relacionada con el paso de las filas.</span><span class="sxs-lookup"><span data-stu-id="92174-117">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="92174-118">Los búferes se pueden usar de forma ortogonal y simultánea desde varias partes de la canalización de gráficos y son muy flexibles.</span><span class="sxs-lookup"><span data-stu-id="92174-118">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span> <br/>                                                                                                                       |
| [<span data-ttu-id="92174-119">Lectura de datos a través de un búfer</span><span class="sxs-lookup"><span data-stu-id="92174-119">Read back data via a buffer</span></span>](readback-data-using-heaps.md)<br/>                    | <span data-ttu-id="92174-120">La lectura de datos de la GPU, como la captura de una captura de pantalla, implica el uso del montón Readback.</span><span class="sxs-lookup"><span data-stu-id="92174-120">Reading back data from the GPU, such as capturing a screen shot, involves the use of the Readback heap.</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="92174-121">Administración de recursos basada en valla</span><span class="sxs-lookup"><span data-stu-id="92174-121">Fence-Based Resource Management</span></span>](fence-based-resource-management.md)<br/>            | <span data-ttu-id="92174-122">Muestra cómo administrar la duración de los datos de recursos mediante el seguimiento del progreso de la GPU a través de vallas.</span><span class="sxs-lookup"><span data-stu-id="92174-122">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="92174-123">La memoria se puede reutilizar eficazmente con barreras administrando cuidadosamente la disponibilidad de espacio libre en memoria, como en una implementación de búfer de anillo para un montón de carga.</span><span class="sxs-lookup"><span data-stu-id="92174-123">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span> <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="92174-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92174-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92174-125">Administración de memoria</span><span class="sxs-lookup"><span data-stu-id="92174-125">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





