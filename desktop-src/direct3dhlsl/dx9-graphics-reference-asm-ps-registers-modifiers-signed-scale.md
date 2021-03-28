---
title: Escala de registro de origen firmada
description: Resta 0,5 de cada canal y escala el resultado en 2,0. El nombre BX2 proviene de Bias y Scale-Times-Two, que es la operación que realiza.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269464"
---
# <a name="source-register-signed-scaling"></a><span data-ttu-id="c480f-104">Escala de registro de origen firmada</span><span class="sxs-lookup"><span data-stu-id="c480f-104">Source Register Signed Scaling</span></span>

<span data-ttu-id="c480f-105">Resta 0,5 de cada canal y escala el resultado en 2,0.</span><span class="sxs-lookup"><span data-stu-id="c480f-105">Subtracts 0.5 from each channel and scales the result by 2.0.</span></span> <span data-ttu-id="c480f-106">El nombre BX2 proviene de Bias y Scale-Times-Two, que es la operación que realiza.</span><span class="sxs-lookup"><span data-stu-id="c480f-106">The name bx2 comes from bias and scale-times-two, which is the operation it performs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c480f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c480f-107">Syntax</span></span>


```
source register_bx2
```



## <a name="register"></a><span data-ttu-id="c480f-108">Registrarse</span><span class="sxs-lookup"><span data-stu-id="c480f-108">Register</span></span>

<span data-ttu-id="c480f-109">Registro de origen.</span><span class="sxs-lookup"><span data-stu-id="c480f-109">Source Register.</span></span> <span data-ttu-id="c480f-110">Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="c480f-110">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c480f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c480f-111">Remarks</span></span>

<span data-ttu-id="c480f-112">Esta operación se utiliza normalmente para expandir los datos de \[ 0,0 a 1,0 a \] \[ -1,0 a 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="c480f-112">This operation is commonly used to expand data from \[0.0 to 1.0\] to \[-1.0 to 1.0\].</span></span> <span data-ttu-id="c480f-113">Este modificador está diseñado para su uso con las instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="c480f-113">This modifier is designed for use with the arithmetic instructions.</span></span> <span data-ttu-id="c480f-114">Este modificador se usa normalmente en las entradas de la instrucción de producto DOT ([DP3-PS](dp3---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="c480f-114">This modifier is commonly used on inputs to the dot product instruction ([dp3 - ps](dp3---ps.md)).</span></span> <span data-ttu-id="c480f-115">\_El uso de BX2 en los datos que están fuera del intervalo de 0 a 1 puede producir resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="c480f-115">Using \_bx2 on data outside the range 0 to 1 may produce undefined results.</span></span>

<span data-ttu-id="c480f-116">La operación de escalado firmada se aplica a los datos leídos del registro antes de que se ejecute la siguiente instrucción.</span><span class="sxs-lookup"><span data-stu-id="c480f-116">The signed scaling operation is applied to the data read from the register before the next instruction is run.</span></span> <span data-ttu-id="c480f-117">La operación se aplica a los cuatro canales de color (RGBA) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c480f-117">The operation is applied to all four color channels (RGBA) as follows:</span></span>


```
y = 2(x - 0.5)
```



<span data-ttu-id="c480f-118">No se cambia el contenido del registro.</span><span class="sxs-lookup"><span data-stu-id="c480f-118">The contents of the register are not changed.</span></span> <span data-ttu-id="c480f-119">El modificador se aplica solo a los datos leídos del registro.</span><span class="sxs-lookup"><span data-stu-id="c480f-119">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="c480f-120">Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , por lo que no se puede aplicar al mismo registro.</span><span class="sxs-lookup"><span data-stu-id="c480f-120">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="c480f-121">Información de versión:</span><span class="sxs-lookup"><span data-stu-id="c480f-121">Version information:</span></span>

-   <span data-ttu-id="c480f-122">Para PS \_ 1 \_ 0 y PS \_ 1 \_ 1, puede usar \_ BX2 en cualquier registro de origen para obtener instrucciones de textura con la forma texm3x2 \* y texm3x3 \* .</span><span class="sxs-lookup"><span data-stu-id="c480f-122">For ps\_1\_0 and ps\_1\_1, you can use \_bx2 on any source register for texture instructions of the form texm3x2\* and texm3x3\*.</span></span> <span data-ttu-id="c480f-123">\_BX2 no se puede usar en ninguna de las otras instrucciones de textura como [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c480f-123">\_bx2 cannot be used on any of the other texture instructions such as [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md).</span></span>
-   <span data-ttu-id="c480f-124">Para PS \_ 1 \_ 2 y PS \_ 1 \_ 3, puede usar \_ BX2 en cualquier registro de origen para cualquier instrucción Tex, \* excepto: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) o [texbeml-PS](texbeml---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c480f-124">For ps\_1\_2 and ps\_1\_3, you can use \_bx2 on any source register for any tex\* instruction except: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) or [texbeml - ps](texbeml---ps.md).</span></span>

## <a name="example"></a><span data-ttu-id="c480f-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c480f-125">Example</span></span>

<span data-ttu-id="c480f-126">En este ejemplo se muestrea una textura, se convierten los datos en el intervalo de-1 a + 1 y se calcula un producto de punto.</span><span class="sxs-lookup"><span data-stu-id="c480f-126">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a><span data-ttu-id="c480f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c480f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c480f-128">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c480f-128">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




