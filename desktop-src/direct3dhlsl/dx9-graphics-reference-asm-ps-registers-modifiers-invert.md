---
title: Inversión del registro de origen
description: Realiza un cálculo de (1 valor) para cada canal del registro especificado.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983743"
---
# <a name="source-register-invert"></a><span data-ttu-id="38566-103">Inversión del registro de origen</span><span class="sxs-lookup"><span data-stu-id="38566-103">Source Register Invert</span></span>

<span data-ttu-id="38566-104">Realiza un cálculo de (1 valor) para cada canal del registro especificado.</span><span class="sxs-lookup"><span data-stu-id="38566-104">Performs a (1 - value) calculation for each channel of the specified register.</span></span>

## <a name="syntax"></a><span data-ttu-id="38566-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38566-105">Syntax</span></span>


```
1 - register
```



## <a name="registers"></a><span data-ttu-id="38566-106">Registros</span><span class="sxs-lookup"><span data-stu-id="38566-106">Registers</span></span>

<span data-ttu-id="38566-107">Registro de origen.</span><span class="sxs-lookup"><span data-stu-id="38566-107">Source Register.</span></span> <span data-ttu-id="38566-108">Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="38566-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="38566-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38566-109">Remarks</span></span>

<span data-ttu-id="38566-110">No se cambia el contenido del registro.</span><span class="sxs-lookup"><span data-stu-id="38566-110">The contents of the register are not changed.</span></span> <span data-ttu-id="38566-111">El modificador se aplica solo a los datos leídos del registro.</span><span class="sxs-lookup"><span data-stu-id="38566-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="38566-112">La operación de inversión se aplica a los cuatro canales de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="38566-112">The invert operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="38566-113">Este modificador solo se puede usar con instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="38566-113">This modifier can be used only with arithmetic instructions.</span></span> <span data-ttu-id="38566-114">Además, este modificador no se puede combinar con la otra [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="38566-114">In addition, this modifier cannot be combined with the other [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="example"></a><span data-ttu-id="38566-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38566-115">Example</span></span>

<span data-ttu-id="38566-116">En este ejemplo se usa inversion para generar el complemento del registro R1.</span><span class="sxs-lookup"><span data-stu-id="38566-116">This example uses inversion to generate the complement of register r1.</span></span>


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a><span data-ttu-id="38566-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38566-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38566-118">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="38566-118">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




