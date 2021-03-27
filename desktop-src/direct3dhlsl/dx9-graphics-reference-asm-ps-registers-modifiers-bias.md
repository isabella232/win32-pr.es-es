---
title: Desviación del registro de origen
description: Reste 0,5 de todos los componentes.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994599"
---
# <a name="source-register-bias"></a><span data-ttu-id="d78f4-103">Desviación del registro de origen</span><span class="sxs-lookup"><span data-stu-id="d78f4-103">Source Register Bias</span></span>

<span data-ttu-id="d78f4-104">Reste 0,5 de todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="d78f4-104">Subtract 0.5 from all components.</span></span>

## <a name="registers"></a><span data-ttu-id="d78f4-105">Registros</span><span class="sxs-lookup"><span data-stu-id="d78f4-105">Registers</span></span>

<span data-ttu-id="d78f4-106">Registro de origen.</span><span class="sxs-lookup"><span data-stu-id="d78f4-106">Source register.</span></span> <span data-ttu-id="d78f4-107">Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="d78f4-107">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d78f4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d78f4-108">Remarks</span></span>

<span data-ttu-id="d78f4-109">No se cambia el contenido del registro.</span><span class="sxs-lookup"><span data-stu-id="d78f4-109">The contents of the register are not changed.</span></span> <span data-ttu-id="d78f4-110">El modificador se aplica solo a los datos leídos del registro.</span><span class="sxs-lookup"><span data-stu-id="d78f4-110">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="d78f4-111">La diferencia se aplica a los cuatro canales de color (RGBA) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d78f4-111">The bias is applied to all four color channels (RGBA) as follows:</span></span>


```
output = (input - 0.5)
```



<span data-ttu-id="d78f4-112">El efecto es modificar los datos que estaban en el intervalo de 0 a 1 para que estén en el intervalo de-0,5 a 0,5.</span><span class="sxs-lookup"><span data-stu-id="d78f4-112">The effect is to modify data that was in the range 0 to 1 to be in the range -0.5 to 0.5.</span></span> <span data-ttu-id="d78f4-113">Aplicar el sesgo a los datos que están fuera de este intervalo puede producir resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="d78f4-113">Applying bias to data outside this range may produce undefined results.</span></span>

> [!Note]  
> <span data-ttu-id="d78f4-114">Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), por lo que no se puede aplicar al mismo registro.</span><span class="sxs-lookup"><span data-stu-id="d78f4-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

 

<span data-ttu-id="d78f4-115">Este modificador es para su uso con las instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="d78f4-115">This modifier is for use with the arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="d78f4-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d78f4-116">Example</span></span>

<span data-ttu-id="d78f4-117">Este ejemplo realiza la misma operación que D3DTOP \_ ADDSIGNED en la sintaxis de varias texturas de DirectX 6,0 y 7,0.</span><span class="sxs-lookup"><span data-stu-id="d78f4-117">This example performs the same operation as D3DTOP\_ADDSIGNED in DirectX 6.0 and 7.0 multiple texture syntax.</span></span>


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a><span data-ttu-id="d78f4-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d78f4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d78f4-119">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d78f4-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




