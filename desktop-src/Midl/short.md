---
title: Short (atributo)
description: La palabra clave Short designa un entero de 16 bits.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- atributo abreviado MIDL
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358174"
---
# <a name="short-attribute"></a><span data-ttu-id="f1c0c-104">Short (atributo)</span><span class="sxs-lookup"><span data-stu-id="f1c0c-104">short attribute</span></span>

<span data-ttu-id="f1c0c-105">La palabra clave **Short** designa un entero de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-105">The **short** keyword designates a 16-bit integer.</span></span>

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="f1c0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1c0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1c0c-107">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="f1c0c-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c0c-108">Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="f1c0c-109">(Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="f1c0c-110">Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1c0c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1c0c-111">Remarks</span></span>

<span data-ttu-id="f1c0c-112">La palabra clave **Short** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra clave [**sin signo**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="f1c0c-112">The **short** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="f1c0c-113">La palabra clave [**int**](int.md) es opcional y se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="f1c0c-114">En el compilador MIDL, un entero corto está firmado de forma predeterminada y es sinónimo de **signed Short int**.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-114">To the MIDL compiler, a short integer is signed by default and is synonymous with **signed short int**.</span></span>

<span data-ttu-id="f1c0c-115">El tipo de entero **corto** es uno de los tipos base del lenguaje IDL.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-115">The **short** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="f1c0c-116">El tipo de entero **Short** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="f1c0c-116">The **short** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="f1c0c-117">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="f1c0c-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f1c0c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1c0c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c0c-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="f1c0c-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="f1c0c-120">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="f1c0c-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f1c0c-121">**Inter**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="f1c0c-122">**tal**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="f1c0c-123">**conectado**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-123">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="f1c0c-124">**pequeño**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="f1c0c-125">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="f1c0c-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




