---
title: int (atributo)
description: La palabra clave int especifica un entero con signo de 32 bits en plataformas de 32 bits. En las plataformas de 16 bits, la palabra clave INT es una palabra clave opcional que puede acompañar a las palabras clave Small, Short y Long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- atributo int de tipo MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783599"
---
# <a name="int-attribute"></a><span data-ttu-id="4ff8d-105">int (atributo)</span><span class="sxs-lookup"><span data-stu-id="4ff8d-105">int attribute</span></span>

<span data-ttu-id="4ff8d-106">La palabra clave **int** especifica un entero con signo de 32 bits en plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-106">The keyword **int** specifies a 32-bit signed integer on 32-bit platforms.</span></span> <span data-ttu-id="4ff8d-107">En las plataformas de 16 bits, la palabra clave **int** es una palabra clave opcional que puede acompañar a las palabras clave [**Small**](small.md), [**Short**](short.md)y [**Long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="4ff8d-107">On 16-bit platforms, the keyword **int** is an optional keyword that can accompany the keywords [**small**](small.md), [**short**](short.md), and [**long**](long.md).</span></span>

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="4ff8d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ff8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff8d-109">*Integer-modificador*</span><span class="sxs-lookup"><span data-stu-id="4ff8d-109">*integer-modifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff8d-110">Especifica la palabra clave [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)o [**\_ \_ Int64**](--int64.md), que selecciona el tamaño de los datos enteros.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-110">Specifies the keyword [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_\_int3264**](--int3264.md), or [**\_\_int64**](--int64.md),which selects the size of the integer data.</span></span> <span data-ttu-id="4ff8d-111">En las plataformas de 16 bits, el calificador de tamaño debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-111">On 16-bit platforms, the size qualifier must be present.</span></span>

</dd> <dt>

<span data-ttu-id="4ff8d-112">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="4ff8d-112">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff8d-113">Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-113">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="4ff8d-114">(Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-114">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="4ff8d-115">Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-115">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ff8d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ff8d-116">Remarks</span></span>

<span data-ttu-id="4ff8d-117">Los tipos enteros se encuentran entre los tipos base del lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="4ff8d-117">Integer types are among the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="4ff8d-118">Pueden aparecer como especificadores de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="4ff8d-118">They can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="4ff8d-119">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="4ff8d-119">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="4ff8d-120">Si no se proporciona ninguna especificación de signo de entero, el tipo entero tiene como valor predeterminado [**signed**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="4ff8d-120">If no integer sign specification is provided, the integer type defaults to [**signed**](signed.md).</span></span>

<span data-ttu-id="4ff8d-121">Los compiladores de DCE IDL no permiten que la palabra clave [**signed**](signed.md) especifique el signo de los tipos enteros.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-121">DCE IDL compilers do not allow the keyword [**signed**](signed.md) to specify the sign of integer types.</span></span> <span data-ttu-id="4ff8d-122">Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-122">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="4ff8d-123">Microsoft no recomienda el uso de \_ \_ int3264 para la comunicación remota si se puede evitar.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-123">Microsoft does not recommend the use of \_\_int3264 for remoting if it can be avoided.</span></span> <span data-ttu-id="4ff8d-124">Consulte el tema sobre [**\_ \_ int3264**](--int3264.md) para obtener más información sobre su uso y limitaciones.</span><span class="sxs-lookup"><span data-stu-id="4ff8d-124">Please see the topic on [**\_\_int3264**](--int3264.md) for more information regarding it's use and limitations.</span></span>

## <a name="examples"></a><span data-ttu-id="4ff8d-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4ff8d-125">Examples</span></span>

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a><span data-ttu-id="4ff8d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ff8d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff8d-127">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="4ff8d-127">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-128">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-128">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-129">**Thread**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-129">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-130">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="4ff8d-130">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-131">**tal**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-131">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-133">**short**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-133">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-134">**conectado**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-134">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-135">**pequeño**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-135">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-136">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-136">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-137">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="4ff8d-138">**Unión**</span><span class="sxs-lookup"><span data-stu-id="4ff8d-138">**union**</span></span>](union.md)
</dt> </dl>

 

 




