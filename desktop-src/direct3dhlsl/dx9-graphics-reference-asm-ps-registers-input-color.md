---
title: Registro del color de entrada
description: Registro de entrada del sombreador de píxeles que contiene el color del vértice.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419186"
---
# <a name="input-color-register"></a><span data-ttu-id="7fbfd-103">Registro del color de entrada</span><span class="sxs-lookup"><span data-stu-id="7fbfd-103">Input Color Register</span></span>

<span data-ttu-id="7fbfd-104">Registro de entrada del sombreador de píxeles que contiene el color del vértice.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-104">Pixel shader input register containing vertex color.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbfd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fbfd-105">Syntax</span></span>


```
dcl v#.writeMask
```



<span data-ttu-id="7fbfd-106">donde:</span><span class="sxs-lookup"><span data-stu-id="7fbfd-106">where:</span></span>

-   <span data-ttu-id="7fbfd-107">[DCL: (SM2, SM3-PS ASM)](dcl---ps.md) es una instrucción de declaración de registro.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-107">[dcl - (sm2, sm3 - ps asm)](dcl---ps.md) is a register declaration instruction.</span></span>
-   <span data-ttu-id="7fbfd-108">v es un registro de entrada y \# es el número de registro.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-108">v is an input register and \# is the register number.</span></span> <span data-ttu-id="7fbfd-109">El número de registros permitidos viene determinado por la versión del sombreador.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-109">The number of registers allowed is determined by the shader version.</span></span>
-   <span data-ttu-id="7fbfd-110">writeMask determina qué componentes (hasta cuatro) están escritos.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-110">writeMask determines which components (up to four) are written.</span></span> <span data-ttu-id="7fbfd-111">Los componentes válidos son: (x, y, z, w) o (r, g, b, a).</span><span class="sxs-lookup"><span data-stu-id="7fbfd-111">Valid components are: (x,y,z,w) or (r,g,b,a).</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbfd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fbfd-112">Remarks</span></span>

<span data-ttu-id="7fbfd-113">Los registros de color son registros de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-113">Color registers are read-only registers.</span></span> <span data-ttu-id="7fbfd-114">Cada registro contiene valores RGBA de cuatro componentes que se iteran desde los vértices de entrada.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-114">Each register contains four-component RGBA values iterated from input vertices.</span></span> <span data-ttu-id="7fbfd-115">Tienen una precisión menor que la mayoría de los registros, se garantiza que tienen 8 bits de datos sin signo en el intervalo (0, + 1).</span><span class="sxs-lookup"><span data-stu-id="7fbfd-115">They have lower precision than most registers, guaranteed to have 8 bits of unsigned data in the range (0, +1).</span></span> <span data-ttu-id="7fbfd-116">No se puede usar más de una en una sola instrucción.</span><span class="sxs-lookup"><span data-stu-id="7fbfd-116">You cannot use more than one in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fbfd-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fbfd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fbfd-118">Registra</span><span class="sxs-lookup"><span data-stu-id="7fbfd-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="7fbfd-119">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros</span><span class="sxs-lookup"><span data-stu-id="7fbfd-119">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="7fbfd-120">Registros de PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7fbfd-120">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="7fbfd-121">Registros de PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7fbfd-121">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="7fbfd-122">Registros de PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7fbfd-122">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




