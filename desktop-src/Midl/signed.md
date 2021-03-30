---
title: atributo signed
description: La palabra clave signed indica que el bit más significativo de una variable de entero representa un bit de signo en lugar de un bit de datos.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- atributo con signo MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103903944"
---
# <a name="signed-attribute"></a><span data-ttu-id="a297c-104">atributo signed</span><span class="sxs-lookup"><span data-stu-id="a297c-104">signed attribute</span></span>

<span data-ttu-id="a297c-105">La palabra clave **signed** indica que el bit más significativo de una variable de entero representa un bit de signo en lugar de un bit de datos.</span><span class="sxs-lookup"><span data-stu-id="a297c-105">The **signed** keyword indicates the most significant bit of an integer variable represents a sign bit rather than a data bit.</span></span>

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="a297c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a297c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a297c-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="a297c-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a297c-108">Puede ser cualquiera de [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)y [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="a297c-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="a297c-109">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="a297c-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a297c-110">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="a297c-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="a297c-111">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="a297c-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a297c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a297c-112">Remarks</span></span>

<span data-ttu-id="a297c-113">Esta palabra clave es opcional y se puede usar con cualquiera de los tipos de carácter y entero [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)y [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="a297c-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="a297c-114">Opcionalmente, puede incluir la palabra clave [**int**](int.md) después de los calificadores de tipo **Long**, **Short** y **Small**.</span><span class="sxs-lookup"><span data-stu-id="a297c-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="a297c-115">Al usar el compilador MIDL [**, los tipos de carácter y**](char-idl.md)entero que aparecen en el archivo IDL sin palabras clave explícitas de signo pueden aparecer con las palabras clave **signed** o [**unsigned**](unsigned.md) en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="a297c-115">When you use the MIDL compiler switch [**char**](char-idl.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the **signed** or [**unsigned**](unsigned.md) keywords in the generated header file.</span></span> <span data-ttu-id="a297c-116">Para evitar confusiones, especifique el signo del entero y los tipos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a297c-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="a297c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a297c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a297c-118">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="a297c-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a297c-119">**/Char**</span><span class="sxs-lookup"><span data-stu-id="a297c-119">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="a297c-120">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="a297c-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a297c-121">**Inter**</span><span class="sxs-lookup"><span data-stu-id="a297c-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="a297c-122">**tal**</span><span class="sxs-lookup"><span data-stu-id="a297c-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="a297c-123">**short**</span><span class="sxs-lookup"><span data-stu-id="a297c-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="a297c-124">**pequeño**</span><span class="sxs-lookup"><span data-stu-id="a297c-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="a297c-125">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="a297c-125">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="a297c-126">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="a297c-126">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




