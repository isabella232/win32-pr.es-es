---
title: Escala del registro de origen x 2
description: Multiplique el valor por dos antes de usarlo en la instrucción.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983742"
---
# <a name="source-register-scale-x-2"></a><span data-ttu-id="9bea9-103">Escala del registro de origen x 2</span><span class="sxs-lookup"><span data-stu-id="9bea9-103">Source Register Scale x 2</span></span>

<span data-ttu-id="9bea9-104">Multiplique el valor por dos antes de usarlo en la instrucción.</span><span class="sxs-lookup"><span data-stu-id="9bea9-104">Multiply the value by two before using it in the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bea9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bea9-105">Syntax</span></span>


```
register_x2
```



## <a name="register"></a><span data-ttu-id="9bea9-106">Registrarse</span><span class="sxs-lookup"><span data-stu-id="9bea9-106">Register</span></span>

<span data-ttu-id="9bea9-107">Registro de origen.</span><span class="sxs-lookup"><span data-stu-id="9bea9-107">Source register.</span></span> <span data-ttu-id="9bea9-108">Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="9bea9-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9bea9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bea9-109">Remarks</span></span>

<span data-ttu-id="9bea9-110">No se cambia el contenido del registro.</span><span class="sxs-lookup"><span data-stu-id="9bea9-110">The contents of the register are not changed.</span></span> <span data-ttu-id="9bea9-111">El modificador se aplica solo a los datos leídos del registro.</span><span class="sxs-lookup"><span data-stu-id="9bea9-111">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="9bea9-112">Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), por lo que no se puede aplicar al mismo registro.</span><span class="sxs-lookup"><span data-stu-id="9bea9-112">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

<span data-ttu-id="9bea9-113">Este modificador solo está disponible para las instrucciones aritméticas de la versión \_ 4.</span><span class="sxs-lookup"><span data-stu-id="9bea9-113">This modifier is only available to arithmetic instructions in version 1\_4.</span></span>

## <a name="example"></a><span data-ttu-id="9bea9-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9bea9-114">Example</span></span>

<span data-ttu-id="9bea9-115">En este ejemplo se muestrea una textura, se convierten los datos en el intervalo de-1 a + 1 y se calcula un producto de punto.</span><span class="sxs-lookup"><span data-stu-id="9bea9-115">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a><span data-ttu-id="9bea9-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bea9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bea9-117">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9bea9-117">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




