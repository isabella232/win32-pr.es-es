---
title: Registro de origen negativo
description: Realiza una negación (y-x) en todos los componentes del registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075612"
---
# <a name="source-register-negate"></a><span data-ttu-id="ef8bd-103">Registro de origen negativo</span><span class="sxs-lookup"><span data-stu-id="ef8bd-103">Source Register Negate</span></span>

<span data-ttu-id="ef8bd-104">Realiza una negación (y =-x) en todos los componentes del registro.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-104">Performs a negate (y = -x), on all register components.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef8bd-105">Syntax</span></span>


```
- register
```



## <a name="registers"></a><span data-ttu-id="ef8bd-106">Registros</span><span class="sxs-lookup"><span data-stu-id="ef8bd-106">Registers</span></span>

<span data-ttu-id="ef8bd-107">Registro de origen.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-107">Source Register.</span></span> <span data-ttu-id="ef8bd-108">Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="ef8bd-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef8bd-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef8bd-109">Remarks</span></span>

<span data-ttu-id="ef8bd-110">No se cambia el contenido del registro.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-110">The contents of the register are not changed.</span></span> <span data-ttu-id="ef8bd-111">El modificador se aplica solo a los datos leídos del registro.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="ef8bd-112">La operación de negación se aplica a los cuatro canales de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="ef8bd-112">The negate operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="ef8bd-113">Esta operación se realiza después de cualquier otro modificador presente en el mismo argumento.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-113">This operation is performed after any other modifiers present on the same argument.</span></span>

<span data-ttu-id="ef8bd-114">Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , por lo que no se puede aplicar al mismo registro.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="ef8bd-115">Este modificador solo se usa con instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-115">This modifier is for use only with arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="ef8bd-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef8bd-116">Example</span></span>

<span data-ttu-id="ef8bd-117">En el ejemplo siguiente se muestra cómo utilizar este modificador.</span><span class="sxs-lookup"><span data-stu-id="ef8bd-117">The following example shows how to use this modifier.</span></span>


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a><span data-ttu-id="ef8bd-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef8bd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef8bd-119">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ef8bd-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




