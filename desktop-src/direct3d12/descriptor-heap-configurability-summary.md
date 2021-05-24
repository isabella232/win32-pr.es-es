---
title: Resumen de la capacidad de configuración del montón de descriptores
description: En la tabla siguiente se resume información sobre la compatibilidad del montón visible de sombreador y no sombreador.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335578"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="23ecc-103">Resumen de la capacidad de configuración del montón de descriptores</span><span class="sxs-lookup"><span data-stu-id="23ecc-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="23ecc-104">En la tabla siguiente se resume información sobre la compatibilidad del montón visible de sombreador y no sombreador.</span><span class="sxs-lookup"><span data-stu-id="23ecc-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="23ecc-105">Montón de descriptores visibles del sombreador</span><span class="sxs-lookup"><span data-stu-id="23ecc-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="23ecc-106">Montón de descriptores visibles que no son de sombreador</span><span class="sxs-lookup"><span data-stu-id="23ecc-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23ecc-107">**Tipos de montón admitidos**</span><span class="sxs-lookup"><span data-stu-id="23ecc-107">**Heap Types Supported**</span></span>          | <span data-ttu-id="23ecc-108">CBV \_ SRV \_ UAV, Sampler</span><span class="sxs-lookup"><span data-stu-id="23ecc-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="23ecc-109">Todo</span><span class="sxs-lookup"><span data-stu-id="23ecc-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="23ecc-110">**Propiedades de página de CPU admitidas**</span><span class="sxs-lookup"><span data-stu-id="23ecc-110">**CPU Page Properties Supported**</span></span> | <span data-ttu-id="23ecc-111">NO \_ DISPONIBLE, COMBINACIÓN DE \_ ESCRITURA</span><span class="sxs-lookup"><span data-stu-id="23ecc-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="23ecc-112">\_REESCRIBA</span><span class="sxs-lookup"><span data-stu-id="23ecc-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="23ecc-113">**Administración de residencias por aplicación**</span><span class="sxs-lookup"><span data-stu-id="23ecc-113">**Residency Management By App**</span></span>   | <span data-ttu-id="23ecc-114">Sí, aplicación responsable</span><span class="sxs-lookup"><span data-stu-id="23ecc-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="23ecc-115">No aplicable (no visible para GPU).</span><span class="sxs-lookup"><span data-stu-id="23ecc-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="23ecc-116">**Compatibilidad con la edición de descriptores**</span><span class="sxs-lookup"><span data-stu-id="23ecc-116">**Descriptor Edit Support**</span></span>       | <span data-ttu-id="23ecc-117">Copiar solo el destino, a través de la actualización de la lista de comandos o la copia de CPU si la CPU está visible.</span><span class="sxs-lookup"><span data-stu-id="23ecc-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="23ecc-118">Solo lectura y escritura de CPU.</span><span class="sxs-lookup"><span data-stu-id="23ecc-118">CPU read and write only.</span></span> <span data-ttu-id="23ecc-119">Sin acceso directo a GPU.</span><span class="sxs-lookup"><span data-stu-id="23ecc-119">No direct GPU access.</span></span> <span data-ttu-id="23ecc-120">Se puede usar para la copia inmediata de CPU (como origen y destino).</span><span class="sxs-lookup"><span data-stu-id="23ecc-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="23ecc-121">Se puede usar como origen de actualización en una lista de comandos: copiará los descriptores en el almacenamiento de la lista de comandos durante el registro de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="23ecc-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="23ecc-122">En la ejecución, la copia almacenada se copiará en el destino, que debe ser un montón visible del sombreador.</span><span class="sxs-lookup"><span data-stu-id="23ecc-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="23ecc-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23ecc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ecc-124">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="23ecc-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




