---
description: Estas constantes se utilizan al crear un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: Constantes de D3D10_EFFECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360031"
---
# <a name="d3d10_effect-constants"></a><span data-ttu-id="d8823-103">Constantes de efecto de D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="d8823-103">D3D10\_EFFECT Constants</span></span>

<span data-ttu-id="d8823-104">Estas constantes se utilizan al crear un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d8823-104">These constants used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span>



| <span data-ttu-id="d8823-105">\#define</span><span class="sxs-lookup"><span data-stu-id="d8823-105">\#define</span></span>                                 | <span data-ttu-id="d8823-106">Value</span><span class="sxs-lookup"><span data-stu-id="d8823-106">Value</span></span>        | <span data-ttu-id="d8823-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8823-107">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8823-108">\_Efecto D3D10 \_ compilar \_ \_ efecto secundario</span><span class="sxs-lookup"><span data-stu-id="d8823-108">D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT</span></span>    | <span data-ttu-id="d8823-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="d8823-109">1 << 0</span></span> | <span data-ttu-id="d8823-110">Compile el archivo. FX en un efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="d8823-110">Compile the .fx file to a child effect.</span></span> <span data-ttu-id="d8823-111">Los efectos secundarios no tienen ninguna inicialización para los valores compartidos porque se inicializan en el grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="d8823-111">Child effects have no initializes for any shared values because these are initialized in the effect pool.</span></span>                                                                                                           |
| <span data-ttu-id="d8823-112">D3D10 \_ efecto \_ compilar \_ permitir \_ operaciones lentas \_</span><span class="sxs-lookup"><span data-stu-id="d8823-112">D3D10\_EFFECT\_COMPILE\_ALLOW\_SLOW\_OPS</span></span> | <span data-ttu-id="d8823-113">1 << 1</span><span class="sxs-lookup"><span data-stu-id="d8823-113">1 << 1</span></span> | <span data-ttu-id="d8823-114">De forma predeterminada, el modo de rendimiento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d8823-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="d8823-115">El modo de rendimiento no permite objetos de estado mutable impidiendo que las expresiones no literales aparezcan en las definiciones de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="d8823-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span> <span data-ttu-id="d8823-116">Si se especifica esta marca, se deshabilitará el modo y se permitirán los objetos de estado mutable.</span><span class="sxs-lookup"><span data-stu-id="d8823-116">Specifying this flag will disable the mode and allow for mutable state objects.</span></span> |
| <span data-ttu-id="d8823-117">Efecto de D3D10 con \_ \_ un único \_ subproceso</span><span class="sxs-lookup"><span data-stu-id="d8823-117">D3D10\_EFFECT\_SINGLE\_THREADED</span></span>          | <span data-ttu-id="d8823-118">1 << 3</span><span class="sxs-lookup"><span data-stu-id="d8823-118">1 << 3</span></span> | <span data-ttu-id="d8823-119">No intente sincronizar con otros efectos de carga de subprocesos en el mismo grupo.</span><span class="sxs-lookup"><span data-stu-id="d8823-119">Do not attempt to synchronize with other threads loading effects into the same pool.</span></span>                                                                                                                                                                        |



 

<span data-ttu-id="d8823-120">Estas constantes se definen como macros en d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="d8823-120">These constants are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8823-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8823-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8823-122">Constantes de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d8823-122">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



