---
title: Propiedad VisibilityCause
description: Propiedad VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418738"
---
# <a name="visibilitycause-property"></a><span data-ttu-id="4ff71-103">Propiedad VisibilityCause</span><span class="sxs-lookup"><span data-stu-id="4ff71-103">VisibilityCause Property</span></span>

<span data-ttu-id="4ff71-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ff71-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4ff71-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="4ff71-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4ff71-106">Devuelve un valor entero que especifica la causa del estado visible del carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-106">Returns an integer value that specifies what caused the character's visible state.</span></span>

</dd> <dt>

<span data-ttu-id="4ff71-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="4ff71-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4ff71-108">*agente*. **Caracteres ("***CharacterID***"). VisibilityCause**</span><span class="sxs-lookup"><span data-stu-id="4ff71-108">*agent*.**Characters("***CharacterID***").VisibilityCause**</span></span>



| <span data-ttu-id="4ff71-109">Value</span><span class="sxs-lookup"><span data-stu-id="4ff71-109">Value</span></span> | <span data-ttu-id="4ff71-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ff71-110">Description</span></span>                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff71-111">0</span><span class="sxs-lookup"><span data-stu-id="4ff71-111">0</span></span>     | <span data-ttu-id="4ff71-112">No se ha mostrado el carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-112">The character has not been shown.</span></span>                                                                            |
| <span data-ttu-id="4ff71-113">1</span><span class="sxs-lookup"><span data-stu-id="4ff71-113">1</span></span>     | <span data-ttu-id="4ff71-114">El usuario ocultó el carácter con el comando en el menú emergente del icono de la barra de tareas del carácter o con la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="4ff71-114">User hid the character using the command on the character's taskbar icon pop-up menu or using speech input..</span></span> |
| <span data-ttu-id="4ff71-115">2</span><span class="sxs-lookup"><span data-stu-id="4ff71-115">2</span></span>     | <span data-ttu-id="4ff71-116">El usuario mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-116">The user showed the character.</span></span>                                                                               |
| <span data-ttu-id="4ff71-117">3</span><span class="sxs-lookup"><span data-stu-id="4ff71-117">3</span></span>     | <span data-ttu-id="4ff71-118">La aplicación ocultó el carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-118">Your application hid the character.</span></span>                                                                          |
| <span data-ttu-id="4ff71-119">4</span><span class="sxs-lookup"><span data-stu-id="4ff71-119">4</span></span>     | <span data-ttu-id="4ff71-120">La aplicación mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-120">Your application showed the character.</span></span>                                                                       |
| <span data-ttu-id="4ff71-121">5</span><span class="sxs-lookup"><span data-stu-id="4ff71-121">5</span></span>     | <span data-ttu-id="4ff71-122">Otra aplicación cliente ocultó el carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-122">Another client application hid the character.</span></span>                                                                |
| <span data-ttu-id="4ff71-123">6</span><span class="sxs-lookup"><span data-stu-id="4ff71-123">6</span></span>     | <span data-ttu-id="4ff71-124">Otra aplicación cliente mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-124">Another client application showed the character.</span></span>                                                             |
| <span data-ttu-id="4ff71-125">7</span><span class="sxs-lookup"><span data-stu-id="4ff71-125">7</span></span>     | <span data-ttu-id="4ff71-126">El usuario ocultó el carácter con el comando en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-126">The user hid the character using the command on the character's pop-up menu.</span></span>                                 |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ff71-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ff71-127">Remarks</span></span>

<span data-ttu-id="4ff71-128">Puede usar esta propiedad para determinar qué causó el movimiento del carácter cuando más de una aplicación comparte (ha cargado) el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="4ff71-128">You can use this property to determine what caused the character to move when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="4ff71-129">Estos valores son los mismos que los devueltos por los eventos [**Mostrar**](show-event.md) y [**ocultar**](hide-event.md) .</span><span class="sxs-lookup"><span data-stu-id="4ff71-129">These values are the same as those returned by the [**Show**](show-event.md) and [**Hide**](hide-event.md) events.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ff71-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4ff71-130">See Also</span></span>

<span data-ttu-id="4ff71-131">[**Ocultar evento**](hide-event.md), [**Mostrar evento**](show-event.md), [**ocultar método**](hide-method.md), [**Mostrar método**](show-method.md)</span><span class="sxs-lookup"><span data-stu-id="4ff71-131">[**Hide event**](hide-event.md), [**Show event**](show-event.md), [**Hide method**](hide-method.md), [**Show method**](show-method.md)</span></span>


 

 




