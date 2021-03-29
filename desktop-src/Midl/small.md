---
title: atributo pequeño
description: La palabra clave Small designa un número entero de 8 bits.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- pequeño atributo MIDL
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419395"
---
# <a name="small-attribute"></a><span data-ttu-id="86131-104">atributo pequeño</span><span class="sxs-lookup"><span data-stu-id="86131-104">small attribute</span></span>

<span data-ttu-id="86131-105">La palabra clave **Small** designa un número entero de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="86131-105">The **small** keyword designates an 8-bit integer number.</span></span>

``` syntax
small identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="86131-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86131-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86131-107">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="86131-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="86131-108">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="86131-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="86131-109">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="86131-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86131-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86131-110">Remarks</span></span>

<span data-ttu-id="86131-111">La palabra clave **Small** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra clave [**sin signo**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="86131-111">The **small** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="86131-112">La palabra clave [**int**](int.md) es opcional y se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="86131-112">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="86131-113">En el compilador de MIDL, un pequeño entero está **firmado** de forma predeterminada y es sinónimo de **int pequeño con signo**.</span><span class="sxs-lookup"><span data-stu-id="86131-113">To the MIDL compiler, a small integer is **signed** by default and is synonymous with **signed small int**.</span></span>

<span data-ttu-id="86131-114">El tipo entero **pequeño** es uno de los tipos base del lenguaje IDL.</span><span class="sxs-lookup"><span data-stu-id="86131-114">The **small** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="86131-115">El tipo entero **pequeño** puede aparecer como especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="86131-115">The **small** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="86131-116">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="86131-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="86131-117">El signo del tipo **pequeño** puede ser modificado por el modificador del compilador de MIDL [**/Char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="86131-117">The sign of the **small** type can be modified by the MIDL compiler switch [**/char**](-char.md).</span></span> <span data-ttu-id="86131-118">Para evitar confusiones, especifique el signo del tipo entero con las palabras clave con [**signo**](signed.md) y sin [**signo**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="86131-118">To avoid confusion, specify the sign of the integer type with the keywords [**signed**](signed.md) and [**unsigned**](unsigned.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="86131-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="86131-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86131-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="86131-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="86131-121">**const**</span><span class="sxs-lookup"><span data-stu-id="86131-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="86131-122">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="86131-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="86131-123">**Inter**</span><span class="sxs-lookup"><span data-stu-id="86131-123">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="86131-124">**tal**</span><span class="sxs-lookup"><span data-stu-id="86131-124">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="86131-125">**short**</span><span class="sxs-lookup"><span data-stu-id="86131-125">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="86131-126">**conectado**</span><span class="sxs-lookup"><span data-stu-id="86131-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="86131-127">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="86131-127">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="86131-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="86131-128">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




