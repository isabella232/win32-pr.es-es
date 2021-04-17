---
description: Estas constantes se aplican a las variables de efecto.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: Constantes de D3D10_EFFECT_VARIABLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705282"
---
# <a name="d3d10_effect_variable-constants"></a><span data-ttu-id="4675b-103">Constantes de variable de \_ efecto de D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="4675b-103">D3D10\_EFFECT\_VARIABLE Constants</span></span>

<span data-ttu-id="4675b-104">Estas constantes se aplican a las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="4675b-104">These constants apply to effect variables.</span></span>



| <span data-ttu-id="4675b-105">\#define</span><span class="sxs-lookup"><span data-stu-id="4675b-105">\#define</span></span>                                       | <span data-ttu-id="4675b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4675b-106">Description</span></span>  | <span data-ttu-id="4675b-107">Value</span><span class="sxs-lookup"><span data-stu-id="4675b-107">Value</span></span>                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4675b-108">D3D10 \_ \_ anotación de variable de efecto \_</span><span class="sxs-lookup"><span data-stu-id="4675b-108">D3D10\_EFFECT\_VARIABLE\_ANNOTATION</span></span>            | <span data-ttu-id="4675b-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="4675b-109">1 << 0</span></span> | <span data-ttu-id="4675b-110">Indica que se trata de una anotación o una variable global.</span><span class="sxs-lookup"><span data-stu-id="4675b-110">Indicates that this is an annotation or a global variable.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="4675b-111">\_Variable de efecto D3D10 \_ \_ agrupada</span><span class="sxs-lookup"><span data-stu-id="4675b-111">D3D10\_EFFECT\_VARIABLE\_POOLED</span></span>                | <span data-ttu-id="4675b-112">1 << 1</span><span class="sxs-lookup"><span data-stu-id="4675b-112">1 << 1</span></span> | <span data-ttu-id="4675b-113">Indica que esta variable o búfer de constantes reside en un grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="4675b-113">Indicates that this variable or constant buffer resides in an effect pool.</span></span> <span data-ttu-id="4675b-114">Si no se establece esta marca, la variable se encuentra en un efecto independiente o en un efecto secundario (los efectos independientes devuelven false desde [**ID3D10Effect:: IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool)).</span><span class="sxs-lookup"><span data-stu-id="4675b-114">If this flag is not set, then the variable resides in a standalone effect or a child effect (standalone effects return false from [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span></span> |
| <span data-ttu-id="4675b-115">\_Punto de \_ \_ enlace explícito \_ de variable de efecto de \_ D3D10</span><span class="sxs-lookup"><span data-stu-id="4675b-115">D3D10\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT</span></span> | <span data-ttu-id="4675b-116">1 << 2</span><span class="sxs-lookup"><span data-stu-id="4675b-116">1 << 2</span></span> | <span data-ttu-id="4675b-117">Indica que la variable se ha enlazado explícitamente mediante la palabra clave Register.</span><span class="sxs-lookup"><span data-stu-id="4675b-117">Indicates that the variable has been explicitly bound using the register keyword.</span></span>                                                                                                                                                                                 |



 

<span data-ttu-id="4675b-118">Estas marcas se definen como macros en d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="4675b-118">These flags are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4675b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4675b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4675b-120">Constantes de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4675b-120">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



