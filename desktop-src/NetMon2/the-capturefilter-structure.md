---
description: En Monitor de red, el filtro de captura se define mediante la estructura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Estructura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001225"
---
# <a name="the-capturefilter-structure"></a><span data-ttu-id="f1625-103">Estructura CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="f1625-103">The CAPTUREFILTER Structure</span></span>

<span data-ttu-id="f1625-104">En Monitor de red, el [filtro de captura](capture-filters.md) se define mediante la estructura [**CAPTUREFILTER**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="f1625-104">In Network Monitor, the [capture filter](capture-filters.md) is defined by the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span> <span data-ttu-id="f1625-105">La ausencia o combinación de marcas, valores y expresiones determina los fotogramas que el controlador Monitor de red pasará o quitará.</span><span class="sxs-lookup"><span data-stu-id="f1625-105">The absence or combination of flags, values, and expressions determines which frames will be passed on or dropped by the Network Monitor driver.</span></span> <span data-ttu-id="f1625-106">En la ilustración siguiente se muestran las tres áreas del análisis del filtro de captura: ETYPE/SAP, dirección y coincidencia de patrones.</span><span class="sxs-lookup"><span data-stu-id="f1625-106">The following illustration shows the three areas of the capture filter analysis: Etype/SAP, address, and pattern match.</span></span>

![tres áreas del análisis del filtro de captura](images/capfilter.png)

<span data-ttu-id="f1625-108">En la tabla siguiente se muestra la función de cada elemento de filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="f1625-108">The following table lists the function of each capture filter element.</span></span>



| <span data-ttu-id="f1625-109">Filter, elemento</span><span class="sxs-lookup"><span data-stu-id="f1625-109">Filter element</span></span>                                       | <span data-ttu-id="f1625-110">Acción</span><span class="sxs-lookup"><span data-stu-id="f1625-110">Action</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1625-111">ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="f1625-111">Etype/SAP</span></span>](writing-etypesap-filter-portion.md)     | <span data-ttu-id="f1625-112">Evalúa la configuración de ETYPE/SAP.</span><span class="sxs-lookup"><span data-stu-id="f1625-112">Evaluates Etype/SAP settings.</span></span> <span data-ttu-id="f1625-113">La combinación de marcas determina qué tipos o valores de configuración se incluyen o excluyen.</span><span class="sxs-lookup"><span data-stu-id="f1625-113">The combination of flags determines which setting types or values are included or excluded.</span></span>                                                                                    |
| [<span data-ttu-id="f1625-114">Dirección</span><span class="sxs-lookup"><span data-stu-id="f1625-114">Address</span></span>](writing-addresstable-filter-portion.md)   | <span data-ttu-id="f1625-115">Evalúa las direcciones de origen y de destino y los pares de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f1625-115">Evaluates source and destination addresses and address pairs.</span></span> <span data-ttu-id="f1625-116">Diferentes combinaciones de marcas determinan qué valores individuales o combinaciones de pares de direcciones se incluyen o excluyen.</span><span class="sxs-lookup"><span data-stu-id="f1625-116">Different combinations of flags determine which individual values or combinations of address pairs are included or excluded.</span></span>                   |
| [<span data-ttu-id="f1625-117">Coincidencia de patrones</span><span class="sxs-lookup"><span data-stu-id="f1625-117">Pattern Match</span></span>](writing-the-patternmatch-filter.md) | <span data-ttu-id="f1625-118">Define coincidencias de patrones complejas dentro de un marco.</span><span class="sxs-lookup"><span data-stu-id="f1625-118">Defines complex pattern matches within a frame.</span></span> <span data-ttu-id="f1625-119">Las marcas se proporcionan para distintos tipos y desplazamientos.</span><span class="sxs-lookup"><span data-stu-id="f1625-119">Flags are provided for different types and offsets.</span></span> <span data-ttu-id="f1625-120">Puede combinar las coincidencias de patrón con las instrucciones de operador AND u OR lógico.</span><span class="sxs-lookup"><span data-stu-id="f1625-120">You can combine pattern matches with logical AND or OR operator statements.</span></span>                              |
| [<span data-ttu-id="f1625-121">Recorte</span><span class="sxs-lookup"><span data-stu-id="f1625-121">Clipping</span></span>](clipping-a-frame.md)                     | <span data-ttu-id="f1625-122">Recorta los fotogramas de forma especificada por varios valores de byte.</span><span class="sxs-lookup"><span data-stu-id="f1625-122">Clips frames in a manner specified by various byte values.</span></span> <span data-ttu-id="f1625-123">Solo puede usar este elemento para recortar todos los marcos o utilizarlos con otros elementos de filtro de captura; por ejemplo, para buscar y después recortar un solo fotograma.</span><span class="sxs-lookup"><span data-stu-id="f1625-123">You can use only this element to clip all frames or use it with other capture filter elements; for example, to find and then clip a single frame.</span></span> |
| [<span data-ttu-id="f1625-124">**Activado**</span><span class="sxs-lookup"><span data-stu-id="f1625-124">**Trigger**</span></span>](trigger.md)                           | <span data-ttu-id="f1625-125">Este elemento de filtro de captura está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f1625-125">This capture filter element is obsolete.</span></span> <span data-ttu-id="f1625-126">Los desencadenadores ya no forman parte de un filtro de captura; ahora están contenidas en sus propias etiquetas BLOB, que se especifican por separado.</span><span class="sxs-lookup"><span data-stu-id="f1625-126">Triggers are no longer part of a capture filter; they are now contained in their own BLOB tags, which are specified separately.</span></span>                                     |



 

<span data-ttu-id="f1625-127">Un marco se evalúa con las tres partes del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="f1625-127">A frame is evaluated against all three portions of the capture filter.</span></span> <span data-ttu-id="f1625-128">Por lo tanto, una trama transmitida correctamente debe pasar cada elemento.</span><span class="sxs-lookup"><span data-stu-id="f1625-128">Therefore, a successfully transmitted frame must pass each element.</span></span> <span data-ttu-id="f1625-129">Tenga en cuenta que el controlador de Monitor de red evalúa la ausencia de cualquiera de los tres elementos como **true**.</span><span class="sxs-lookup"><span data-stu-id="f1625-129">Be aware that the Network Monitor driver evaluates the absence of any of the three elements as **TRUE**.</span></span> <span data-ttu-id="f1625-130">Por ejemplo, el controlador evalúa la ausencia de una sección ETYPE/SAP como "todos los marcos con el valor ETYPE/SAP son válidos".</span><span class="sxs-lookup"><span data-stu-id="f1625-130">For example, the driver evaluates the absence of an Etype/SAP section as "ALL frames with the ANY Etype/SAP value are valid."</span></span>

 

 



