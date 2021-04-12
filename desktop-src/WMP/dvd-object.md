---
title: Objeto de DVD
description: El objeto DVD proporciona propiedades y métodos para trabajar con DVDs.
ms.assetid: 953f6ba5-637b-4f70-aeea-dfe9f52d8675
keywords:
- Media Player de objetos de DVD de Windows
topic_type:
- apiref
api_name:
- DVD Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 656b08f90f3b6878cfde2a526ddf682a82dd8498
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104419769"
---
# <a name="dvd-object"></a><span data-ttu-id="9f8f8-104">Objeto de DVD</span><span class="sxs-lookup"><span data-stu-id="9f8f8-104">DVD Object</span></span>

<span data-ttu-id="9f8f8-105">El objeto **DVD** proporciona propiedades y métodos para trabajar con DVDs.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-105">The **DVD** object provides properties and methods for working with DVDs.</span></span>

<span data-ttu-id="9f8f8-106">El objeto **DVD** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-106">The **DVD** object supports the following properties.</span></span>



| <span data-ttu-id="9f8f8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f8f8-107">Property</span></span>                           | <span data-ttu-id="9f8f8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f8f8-108">Description</span></span>                                                                                        |
|------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f8f8-109">dominio</span><span class="sxs-lookup"><span data-stu-id="9f8f8-109">domain</span></span>](dvd-domain.md)           | <span data-ttu-id="9f8f8-110">Recupera el dominio actual del DVD.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-110">Retrieves the current domain of the DVD.</span></span>                                                           |
| [<span data-ttu-id="9f8f8-111">isAvailable</span><span class="sxs-lookup"><span data-stu-id="9f8f8-111">isAvailable</span></span>](dvd-isavailable.md) | <span data-ttu-id="9f8f8-112">Recupera si un tipo de información especificado está disponible o se puede realizar una acción determinada.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-112">Retrieves whether a specified type of information is available or a given action can be performed.</span></span> |



 

<span data-ttu-id="9f8f8-113">El objeto **DVD** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-113">The **DVD** object supports the following methods.</span></span>



| <span data-ttu-id="9f8f8-114">Método</span><span class="sxs-lookup"><span data-stu-id="9f8f8-114">Method</span></span>                         | <span data-ttu-id="9f8f8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f8f8-115">Description</span></span>                                                                                          |
|--------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f8f8-116">Atrás</span><span class="sxs-lookup"><span data-stu-id="9f8f8-116">back</span></span>](dvd-back.md)           | <span data-ttu-id="9f8f8-117">Cambia la presentación de un submenú a su menú primario.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-117">Changes the display from a submenu to its parent menu.</span></span>                                               |
| [<span data-ttu-id="9f8f8-118">Recuper</span><span class="sxs-lookup"><span data-stu-id="9f8f8-118">resume</span></span>](dvd-resume.md)       | <span data-ttu-id="9f8f8-119">Cambia el modo de reproducción del modo de menú, reanudando en la misma posición que cuando se invocó el menú.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-119">Changes to playback mode from menu mode, resuming at the same position as when the menu was invoked.</span></span> |
| [<span data-ttu-id="9f8f8-120">titleMenu</span><span class="sxs-lookup"><span data-stu-id="9f8f8-120">titleMenu</span></span>](dvd-titlemenu.md) | <span data-ttu-id="9f8f8-121">Detiene la reproducción y muestra el menú de título.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-121">Stops playback and displays the title menu.</span></span>                                                          |
| [<span data-ttu-id="9f8f8-122">Menú de menús</span><span class="sxs-lookup"><span data-stu-id="9f8f8-122">topMenu</span></span>](dvd-topmenu.md)     | <span data-ttu-id="9f8f8-123">Detiene la reproducción y muestra el menú raíz.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-123">Stops playback and displays the root menu.</span></span>                                                           |



 

<span data-ttu-id="9f8f8-124">Se tiene acceso al objeto de **DVD** a través de la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-124">The **DVD** object is accessed through the following property.</span></span>



| <span data-ttu-id="9f8f8-125">Object</span><span class="sxs-lookup"><span data-stu-id="9f8f8-125">Object</span></span>                      | <span data-ttu-id="9f8f8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f8f8-126">Property</span></span>              |
|-----------------------------|-----------------------|
| [<span data-ttu-id="9f8f8-127">Reproductor</span><span class="sxs-lookup"><span data-stu-id="9f8f8-127">Player</span></span>](player-object.md) | [<span data-ttu-id="9f8f8-128">discos</span><span class="sxs-lookup"><span data-stu-id="9f8f8-128">dvd</span></span>](player-dvd.md) |



 

## <a name="see-also"></a><span data-ttu-id="9f8f8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f8f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f8f8-130">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="9f8f8-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




