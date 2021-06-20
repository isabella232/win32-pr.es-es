---
title: Registro de contadores de bucles (referencia de HLSL VS)
description: Obtenga información sobre el registro del contador de bucles para sombreadores de vértices. El único registro de este banco es el registro del contador de bucles (aL) actual.
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405778"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="2ec7c-104">Registro de contadores de bucles (referencia de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="2ec7c-104">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="2ec7c-105">El único registro de este banco es el registro del contador de bucles (aL) actual.</span><span class="sxs-lookup"><span data-stu-id="2ec7c-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="2ec7c-106">Se incrementa automáticamente en cada ejecución del [bucle ( frente a](loop---vs.md)... [endloop: vs](endloop---vs.md) block.</span><span class="sxs-lookup"><span data-stu-id="2ec7c-106">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="2ec7c-107">Por lo tanto, se puede usar en el bloque para el direccionamiento relativo si es necesario y no es válido usarlo fuera del bucle.</span><span class="sxs-lookup"><span data-stu-id="2ec7c-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ec7c-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ec7c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ec7c-109">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2ec7c-109">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




