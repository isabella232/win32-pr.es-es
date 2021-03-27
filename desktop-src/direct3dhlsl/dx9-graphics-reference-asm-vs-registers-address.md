---
title: Registro de direcciones
description: El registro a0 es un registro de direcciones.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903693"
---
# <a name="address-register"></a><span data-ttu-id="8efa6-103">Registro de direcciones</span><span class="sxs-lookup"><span data-stu-id="8efa6-103">Address Register</span></span>

<span data-ttu-id="8efa6-104">El registro a0 es un registro de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8efa6-104">The a0 register is an address register.</span></span> <span data-ttu-id="8efa6-105">Un único registro está disponible en la versión vs \_ 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="8efa6-105">A single register is available in version vs\_1\_1.</span></span> <span data-ttu-id="8efa6-106">El registro de dirección, designado como a0. x en vs \_ 1 \_ 1, se puede usar como desplazamiento de entero con signo para el direccionamiento relativo en el archivo de registro de constantes.</span><span class="sxs-lookup"><span data-stu-id="8efa6-106">The address register, designated as a0.x in vs\_1\_1, can be used as a signed integer offset for relative addressing into the constant register file.</span></span> <span data-ttu-id="8efa6-107">En el caso de las versiones de vs \_ 2 \_ 0 y posteriores, los cuatro componentes (. x,. y,. z,. w) están disponibles para el direccionamiento relativo.</span><span class="sxs-lookup"><span data-stu-id="8efa6-107">For versions vs\_2\_0 and above, all four components (.x, .y, .z, .w) are available for relative addressing.</span></span>


```
c[a0.x + n]
```



<span data-ttu-id="8efa6-108">Un sombreador de vértices no puede leer el registro de direcciones, solo se puede usar para el direccionamiento relativo de un registro de constantes.</span><span class="sxs-lookup"><span data-stu-id="8efa6-108">The address register cannot be read by a vertex shader, it can only be used for relative addressing of a constant register.</span></span> <span data-ttu-id="8efa6-109">La lectura de valores fuera del intervalo legal devolverá (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="8efa6-109">Reading values outside of the legal range will return (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="8efa6-110">El registro de dirección solo puede ser un destino para la instrucción [MOV-vs](mov---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="8efa6-110">The address register can only be a destination for the [mov - vs](mov---vs.md) instruction.</span></span> <span data-ttu-id="8efa6-111">Si un número de punto flotante se mueve a un registro entero, se produce una conversión de ida a vuelta más cercana.</span><span class="sxs-lookup"><span data-stu-id="8efa6-111">If a floating-point number is moved into an integer register, a round-to-nearest conversion happens.</span></span>

<span data-ttu-id="8efa6-112">Todos los sombreadores deben inicializar el registro de direcciones antes de usarlo.</span><span class="sxs-lookup"><span data-stu-id="8efa6-112">All shaders must initialize the address register before using it.</span></span> <span data-ttu-id="8efa6-113">En el caso de la versión de vs \_ 2 \_ 0 y versiones posteriores, la instrucción [mova-vs](mova---vs.md) puede trasladar un valor de punto flotante a un registro de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8efa6-113">For version vs\_2\_0 and above, the [mova - vs](mova---vs.md) instruction can move a floating-point value to an address register.</span></span>



| <span data-ttu-id="8efa6-114">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8efa6-114">Vertex shader versions</span></span> | <span data-ttu-id="8efa6-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="8efa6-115">1\_1</span></span> | <span data-ttu-id="8efa6-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8efa6-116">2\_0</span></span> | <span data-ttu-id="8efa6-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8efa6-117">2\_sw</span></span> | <span data-ttu-id="8efa6-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8efa6-118">2\_x</span></span> | <span data-ttu-id="8efa6-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8efa6-119">3\_0</span></span> | <span data-ttu-id="8efa6-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8efa6-120">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="8efa6-121">Registro de direcciones</span><span class="sxs-lookup"><span data-stu-id="8efa6-121">Address Register</span></span>       | <span data-ttu-id="8efa6-122">x</span><span class="sxs-lookup"><span data-stu-id="8efa6-122">x</span></span>    | <span data-ttu-id="8efa6-123">x</span><span class="sxs-lookup"><span data-stu-id="8efa6-123">x</span></span>    | <span data-ttu-id="8efa6-124">x</span><span class="sxs-lookup"><span data-stu-id="8efa6-124">x</span></span>     | <span data-ttu-id="8efa6-125">x</span><span class="sxs-lookup"><span data-stu-id="8efa6-125">x</span></span>    | <span data-ttu-id="8efa6-126">x</span><span class="sxs-lookup"><span data-stu-id="8efa6-126">x</span></span>    | <span data-ttu-id="8efa6-127">x</span><span class="sxs-lookup"><span data-stu-id="8efa6-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="8efa6-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8efa6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8efa6-129">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8efa6-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




