---
title: atributo Long
description: La palabra clave Long designa un entero de 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- Long (atributo) MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994677"
---
# <a name="long-attribute"></a><span data-ttu-id="ed876-104">atributo Long</span><span class="sxs-lookup"><span data-stu-id="ed876-104">long attribute</span></span>

<span data-ttu-id="ed876-105">La palabra clave **Long** designa un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ed876-105">The **long** keyword designates a 32-bit integer.</span></span>

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="ed876-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed876-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed876-107">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="ed876-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ed876-108">Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="ed876-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="ed876-109">(Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="ed876-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="ed876-110">Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.</span><span class="sxs-lookup"><span data-stu-id="ed876-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed876-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed876-111">Remarks</span></span>

<span data-ttu-id="ed876-112">La palabra clave **Long** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra clave [**sin signo**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="ed876-112">The **long** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="ed876-113">La palabra clave [**int**](int.md) es opcional y se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="ed876-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="ed876-114">En el compilador de MIDL, un entero largo está firmado de forma predeterminada y es sinónimo de **signed Long int**. En las plataformas de 32 bits, **Long** es sinónimo de **int**.</span><span class="sxs-lookup"><span data-stu-id="ed876-114">To the MIDL compiler, a long integer is signed by default and is synonymous with **signed long int**. On 32-bit platforms, **long** is synonymous with **int**.</span></span>

<span data-ttu-id="ed876-115">El tipo entero **largo** es uno de los tipos base del lenguaje IDL.</span><span class="sxs-lookup"><span data-stu-id="ed876-115">The **long** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="ed876-116">El tipo de entero **largo** puede aparecer como especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="ed876-116">The **long** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="ed876-117">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="ed876-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed876-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed876-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed876-119">**const**</span><span class="sxs-lookup"><span data-stu-id="ed876-119">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="ed876-120">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="ed876-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ed876-121">**Thread**</span><span class="sxs-lookup"><span data-stu-id="ed876-121">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="ed876-122">**Inter**</span><span class="sxs-lookup"><span data-stu-id="ed876-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="ed876-123">**short**</span><span class="sxs-lookup"><span data-stu-id="ed876-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="ed876-124">**conectado**</span><span class="sxs-lookup"><span data-stu-id="ed876-124">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="ed876-125">**pequeño**</span><span class="sxs-lookup"><span data-stu-id="ed876-125">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="ed876-126">**typedef**</span><span class="sxs-lookup"><span data-stu-id="ed876-126">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="ed876-127">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="ed876-127">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




