---
title: enum (atributo)
description: La palabra clave enum identifica un tipo enumerado.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- atributo de enumeración MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358000"
---
# <a name="enum-attribute"></a><span data-ttu-id="18e81-104">enum (atributo)</span><span class="sxs-lookup"><span data-stu-id="18e81-104">enum attribute</span></span>

<span data-ttu-id="18e81-105">La palabra clave **enum** identifica un tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="18e81-105">The keyword **enum** identifies an enumerated type.</span></span>

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a><span data-ttu-id="18e81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18e81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e81-107">*etiqueta*</span><span class="sxs-lookup"><span data-stu-id="18e81-107">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="18e81-108">Especifica una etiqueta opcional para el tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="18e81-108">Specifies an optional tag for the enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="18e81-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="18e81-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="18e81-110">Especifica la enumeración concreta.</span><span class="sxs-lookup"><span data-stu-id="18e81-110">Specifies the particular enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="18e81-111">*valor entero:*</span><span class="sxs-lookup"><span data-stu-id="18e81-111">*integer-value*</span></span> 
</dt> <dd>

<span data-ttu-id="18e81-112">Especifica un valor entero constante.</span><span class="sxs-lookup"><span data-stu-id="18e81-112">Specifies a constant integer value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18e81-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18e81-113">Remarks</span></span>

<span data-ttu-id="18e81-114">los tipos de **enumeración** pueden aparecer como especificadores de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como function-return-type o como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="18e81-114">**enum** types can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (either as the function-return-type or as a parameter-type specifier).</span></span> <span data-ttu-id="18e81-115">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="18e81-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="18e81-116">En el modo predeterminado del compilador MIDL, puede asignar valores enteros a los enumeradores.</span><span class="sxs-lookup"><span data-stu-id="18e81-116">In the MIDL compiler's default mode, you can assign integer values to enumerators.</span></span> <span data-ttu-id="18e81-117">(Esta característica no está disponible cuando se compila con el modificador [**/OSF**](-osf.md) ). Al igual que con los enumeradores de lenguaje C, los nombres de enumerador deben ser únicos, pero los valores del enumerador no deben ser.</span><span class="sxs-lookup"><span data-stu-id="18e81-117">(This feature is not available when you compile with the [**/osf**](-osf.md) switch.) As with C-language enumerators, enumerator names must be unique, but the enumerator values need not be.</span></span>

<span data-ttu-id="18e81-118">Cuando no se proporcionan operadores de asignación, los identificadores se asignan a enteros consecutivos de izquierda a derecha, empezando por cero.</span><span class="sxs-lookup"><span data-stu-id="18e81-118">When assignment operators are not provided, identifiers are mapped to consecutive integers from left to right, starting with zero.</span></span> <span data-ttu-id="18e81-119">Cuando se proporcionan operadores de asignación, los valores asignados empiezan por el valor asignado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="18e81-119">When assignment operators are provided, assigned values start from the most recently assigned value.</span></span>

<span data-ttu-id="18e81-120">El número máximo de identificadores es 65.535.</span><span class="sxs-lookup"><span data-stu-id="18e81-120">The maximum number of identifiers is 65,535.</span></span>

<span data-ttu-id="18e81-121">Los objetos de tipo **enum** son tipos [**int**](int.md) y su tamaño depende del sistema.</span><span class="sxs-lookup"><span data-stu-id="18e81-121">Objects of type **enum** are [**int**](int.md) types, and their size is system-dependent.</span></span> <span data-ttu-id="18e81-122">De forma predeterminada, los objetos de tipos de **enumeración** se tratan como objetos de 16 bits de tipo [**Short**](short.md) [**sin signo**](unsigned.md) cuando se transmiten a través de una red.</span><span class="sxs-lookup"><span data-stu-id="18e81-122">By default, objects of **enum** types are treated as 16-bit objects of type [**unsigned**](unsigned.md) [**short**](short.md) when transmitted over a network.</span></span> <span data-ttu-id="18e81-123">Los valores que están fuera del intervalo de 0 a 32.767 provocan que el valor de enumeración de RPC X de la excepción en tiempo de ejecución esté \_ \_ \_ \_ fuera \_ del \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="18e81-123">Values outside the range 0 - 32,767 cause the run-time exception RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="18e81-124">Para transmitir objetos como entidades de 32 bits, aplique el **\[** atributo de [**\_ enumeración v1**](v1-enum.md) **\]** al typedef **enum** .</span><span class="sxs-lookup"><span data-stu-id="18e81-124">To transmit objects as 32-bit entities, apply the **\[**[**v1\_enum**](v1-enum.md)**\]** attribute to the **enum** typedef.</span></span>

## <a name="examples"></a><span data-ttu-id="18e81-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="18e81-125">Examples</span></span>

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a><span data-ttu-id="18e81-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="18e81-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e81-127">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="18e81-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="18e81-128">**Inter**</span><span class="sxs-lookup"><span data-stu-id="18e81-128">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="18e81-129">**short**</span><span class="sxs-lookup"><span data-stu-id="18e81-129">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="18e81-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="18e81-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="18e81-131">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="18e81-131">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="18e81-132">**\_enumeración v1**</span><span class="sxs-lookup"><span data-stu-id="18e81-132">**v1\_enum**</span></span>](v1-enum.md)
</dt> </dl>

 

 




