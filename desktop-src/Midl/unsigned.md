---
title: unsigned (atributo)
description: La palabra clave unsigned indica que el bit más significativo de una variable de entero representa un bit de datos en lugar de un bit con signo.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- atributo sin signo MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665759"
---
# <a name="unsigned-attribute"></a><span data-ttu-id="feefd-104">unsigned (atributo)</span><span class="sxs-lookup"><span data-stu-id="feefd-104">unsigned attribute</span></span>

<span data-ttu-id="feefd-105">La palabra clave **unsigned** indica que el bit más significativo de una variable de entero representa un bit de datos en lugar de un bit con signo.</span><span class="sxs-lookup"><span data-stu-id="feefd-105">The **unsigned** keyword indicates that the most significant bit of an integer variable represents a data bit rather than a signed bit.</span></span>

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="feefd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="feefd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feefd-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="feefd-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="feefd-108">Puede ser cualquiera de [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**Short**](short.md)y [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="feefd-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="feefd-109">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="feefd-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="feefd-110">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="feefd-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="feefd-111">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="feefd-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="feefd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="feefd-112">Remarks</span></span>

<span data-ttu-id="feefd-113">Esta palabra clave es opcional y se puede usar con cualquiera de los tipos de carácter y entero [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)y [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="feefd-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="feefd-114">Opcionalmente, puede incluir la palabra clave [**int**](int.md) después de los calificadores de tipo **Long**, **Short** y **Small**.</span><span class="sxs-lookup"><span data-stu-id="feefd-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="feefd-115">Cuando se usa el modificador de compilador MIDL [**/Char**](-char.md), los tipos de carácter y entero que aparecen en el archivo IDL sin palabras clave explícitas de signo pueden aparecer con la palabra clave [**signed**](signed.md) o **unsigned** en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="feefd-115">When you use the MIDL compiler switch [**/char**](-char.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the [**signed**](signed.md) or **unsigned** keyword in the generated header file.</span></span> <span data-ttu-id="feefd-116">Para evitar confusiones, especifique el signo del entero y los tipos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="feefd-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="feefd-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="feefd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feefd-118">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="feefd-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="feefd-119">**char**</span><span class="sxs-lookup"><span data-stu-id="feefd-119">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="feefd-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="feefd-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="feefd-121">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="feefd-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="feefd-122">**Inter**</span><span class="sxs-lookup"><span data-stu-id="feefd-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="feefd-123">**tal**</span><span class="sxs-lookup"><span data-stu-id="feefd-123">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="feefd-124">**short**</span><span class="sxs-lookup"><span data-stu-id="feefd-124">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="feefd-125">**conectado**</span><span class="sxs-lookup"><span data-stu-id="feefd-125">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="feefd-126">**pequeño**</span><span class="sxs-lookup"><span data-stu-id="feefd-126">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="feefd-127">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="feefd-127">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




