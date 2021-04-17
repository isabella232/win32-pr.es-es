---
title: DISPID estándar
description: Se ha definido un número de DISPID estándar para la especificación de los controles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704609"
---
# <a name="standard-dispids"></a><span data-ttu-id="bfb7c-103">DISPID estándar</span><span class="sxs-lookup"><span data-stu-id="bfb7c-103">Standard DISPIDS</span></span>

<span data-ttu-id="bfb7c-104">Se ha definido un número de DISPID estándar para la especificación de los controles.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-104">A number of standard dispids have been defined for the controls specification.</span></span>

## <a name="dispid_mousepointer"></a><span data-ttu-id="bfb7c-105">desspid- \_ MOUSEPOINTER</span><span class="sxs-lookup"><span data-stu-id="bfb7c-105">DISPID\_MOUSEPOINTER</span></span>

<span data-ttu-id="bfb7c-106">Propiedad de tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-106">Property of type integer.</span></span>

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

<span data-ttu-id="bfb7c-107">La propiedad MousePointer identifica los iconos del mouse estándar.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-107">The Mousepointer property identifies standard mouse icons.</span></span>



| <span data-ttu-id="bfb7c-108">Value</span><span class="sxs-lookup"><span data-stu-id="bfb7c-108">Value</span></span>         | <span data-ttu-id="bfb7c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfb7c-109">Description</span></span>                                                                |
|---------------|----------------------------------------------------------------------------|
| <span data-ttu-id="bfb7c-110">0</span><span class="sxs-lookup"><span data-stu-id="bfb7c-110">0</span></span><br/>  | <span data-ttu-id="bfb7c-111">Predeterminada Forma determinada por el objeto.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-111">(Default) Shape determined by the object.</span></span><br/>                       |
| <span data-ttu-id="bfb7c-112">1</span><span class="sxs-lookup"><span data-stu-id="bfb7c-112">1</span></span><br/>  | <span data-ttu-id="bfb7c-113">Flecha</span><span class="sxs-lookup"><span data-stu-id="bfb7c-113">Arrow</span></span><br/>                                                           |
| <span data-ttu-id="bfb7c-114">2</span><span class="sxs-lookup"><span data-stu-id="bfb7c-114">2</span></span><br/>  | <span data-ttu-id="bfb7c-115">Cross (puntero de Cruz)</span><span class="sxs-lookup"><span data-stu-id="bfb7c-115">Cross (cross-hair pointer)</span></span><br/>                                      |
| <span data-ttu-id="bfb7c-116">3</span><span class="sxs-lookup"><span data-stu-id="bfb7c-116">3</span></span><br/>  | <span data-ttu-id="bfb7c-117">I</span><span class="sxs-lookup"><span data-stu-id="bfb7c-117">I Beam</span></span><br/>                                                          |
| <span data-ttu-id="bfb7c-118">4</span><span class="sxs-lookup"><span data-stu-id="bfb7c-118">4</span></span><br/>  | <span data-ttu-id="bfb7c-119">Icono (cuadrado pequeño dentro de un cuadrado)</span><span class="sxs-lookup"><span data-stu-id="bfb7c-119">Icon (small square within a square)</span></span><br/>                             |
| <span data-ttu-id="bfb7c-120">5</span><span class="sxs-lookup"><span data-stu-id="bfb7c-120">5</span></span><br/>  | <span data-ttu-id="bfb7c-121">Tamaño (flecha de cuatro puntas que apunta al norte, sur, este y oeste)</span><span class="sxs-lookup"><span data-stu-id="bfb7c-121">Size (four-pointed arrow pointing north, south, east, and west)</span></span><br/> |
| <span data-ttu-id="bfb7c-122">6</span><span class="sxs-lookup"><span data-stu-id="bfb7c-122">6</span></span><br/>  | <span data-ttu-id="bfb7c-123">Tamaño NE SW (doble flecha que apunta al noreste y suroeste)</span><span class="sxs-lookup"><span data-stu-id="bfb7c-123">Size NE SW (double arrow pointing northeast and southwest)</span></span><br/>      |
| <span data-ttu-id="bfb7c-124">7</span><span class="sxs-lookup"><span data-stu-id="bfb7c-124">7</span></span><br/>  | <span data-ttu-id="bfb7c-125">Tamaño N S (flecha doble que apunta al norte y al sur)</span><span class="sxs-lookup"><span data-stu-id="bfb7c-125">Size N S (double arrow pointing north and south)</span></span><br/>                |
| <span data-ttu-id="bfb7c-126">8</span><span class="sxs-lookup"><span data-stu-id="bfb7c-126">8</span></span><br/>  | <span data-ttu-id="bfb7c-127">Tamaño NW, SE</span><span class="sxs-lookup"><span data-stu-id="bfb7c-127">Size NW, SE</span></span><br/>                                                     |
| <span data-ttu-id="bfb7c-128">9</span><span class="sxs-lookup"><span data-stu-id="bfb7c-128">9</span></span><br/>  | <span data-ttu-id="bfb7c-129">Tamaño E W (flecha doble que señala al este y oeste)</span><span class="sxs-lookup"><span data-stu-id="bfb7c-129">Size E W (double arrow pointing east and west)</span></span><br/>                  |
| <span data-ttu-id="bfb7c-130">10</span><span class="sxs-lookup"><span data-stu-id="bfb7c-130">10</span></span><br/> | <span data-ttu-id="bfb7c-131">Flecha arriba</span><span class="sxs-lookup"><span data-stu-id="bfb7c-131">Up Arrow</span></span><br/>                                                        |
| <span data-ttu-id="bfb7c-132">11</span><span class="sxs-lookup"><span data-stu-id="bfb7c-132">11</span></span><br/> | <span data-ttu-id="bfb7c-133">Reloj de arena (esperar)</span><span class="sxs-lookup"><span data-stu-id="bfb7c-133">Hourglass (wait)</span></span><br/>                                                |
| <span data-ttu-id="bfb7c-134">12</span><span class="sxs-lookup"><span data-stu-id="bfb7c-134">12</span></span><br/> | <span data-ttu-id="bfb7c-135">No eliminar</span><span class="sxs-lookup"><span data-stu-id="bfb7c-135">No Drop</span></span><br/>                                                         |
| <span data-ttu-id="bfb7c-136">13</span><span class="sxs-lookup"><span data-stu-id="bfb7c-136">13</span></span><br/> | <span data-ttu-id="bfb7c-137">Flecha y reloj de arena</span><span class="sxs-lookup"><span data-stu-id="bfb7c-137">Arrow and hourglass</span></span><br/>                                             |
| <span data-ttu-id="bfb7c-138">14</span><span class="sxs-lookup"><span data-stu-id="bfb7c-138">14</span></span><br/> | <span data-ttu-id="bfb7c-139">Flecha y signo de interrogación</span><span class="sxs-lookup"><span data-stu-id="bfb7c-139">Arrow and question mark</span></span><br/>                                         |
| <span data-ttu-id="bfb7c-140">15</span><span class="sxs-lookup"><span data-stu-id="bfb7c-140">15</span></span><br/> | <span data-ttu-id="bfb7c-141">Ajustar todo</span><span class="sxs-lookup"><span data-stu-id="bfb7c-141">Size all</span></span><br/>                                                        |
| <span data-ttu-id="bfb7c-142">99</span><span class="sxs-lookup"><span data-stu-id="bfb7c-142">99</span></span><br/> | <span data-ttu-id="bfb7c-143">Icono personalizado especificado por la propiedad MouseIcon</span><span class="sxs-lookup"><span data-stu-id="bfb7c-143">Custom icon specified by the MouseIcon property</span></span><br/>                 |



 

## <a name="dispid_mouseicon"></a><span data-ttu-id="bfb7c-144">MOUSEICON de DISPID \_</span><span class="sxs-lookup"><span data-stu-id="bfb7c-144">DISPID\_MOUSEICON</span></span>

<span data-ttu-id="bfb7c-145">Propiedad de tipo imagen.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-145">Property of type picture.</span></span>

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a><span data-ttu-id="bfb7c-146">imagen de DISPID \_</span><span class="sxs-lookup"><span data-stu-id="bfb7c-146">DISPID\_PICTURE</span></span>

<span data-ttu-id="bfb7c-147">Propiedad de tipo imagen.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-147">Property of type picture.</span></span>

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a><span data-ttu-id="bfb7c-148">DISPID \_ válido</span><span class="sxs-lookup"><span data-stu-id="bfb7c-148">DISPID\_VALID</span></span>

<span data-ttu-id="bfb7c-149">Se utiliza para determinar si el control tiene datos válidos o no.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-149">Used to determine if the control has valid data or not.</span></span>

<span data-ttu-id="bfb7c-150">Propiedad de tipo BOOL.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-150">Property of type BOOL.</span></span>

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a><span data-ttu-id="bfb7c-151">paleta ambiente de DISPID \_ \_</span><span class="sxs-lookup"><span data-stu-id="bfb7c-151">DISPID\_ AMBIENT\_PALETTE</span></span>

<span data-ttu-id="bfb7c-152">Se utiliza para permitir que el control obtenga el HPAL del contenedor.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-152">Used to allow the control to get the container's HPAL.</span></span> <span data-ttu-id="bfb7c-153">Si el contenedor proporciona una paleta ambiente, es la única paleta que se puede realizar en primer plano.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-153">If the container supplies an ambient palette then that is the only palette that may be realized into the foreground.</span></span> <span data-ttu-id="bfb7c-154">Los controles que deseen obtener sus propias paletas deben hacerlo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-154">Controls that want to realize their own palettes must do so in the background.</span></span> <span data-ttu-id="bfb7c-155">Si no hay ninguna paleta ambiente proporcionada por el contenedor, el control activo puede obtener su paleta en primer plano.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-155">If there is no ambient palette provided by the container, then the active control can realize its palette in the foreground.</span></span> <span data-ttu-id="bfb7c-156">El control de paleta se describe con más detalle en el comportamiento de la paleta para los controles OLE que se encuentra en el SDK de ActiveX.</span><span class="sxs-lookup"><span data-stu-id="bfb7c-156">Palette handling is further discussed in Palette Behavior for OLE Controls which is in the ActiveX SDK.</span></span>

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





