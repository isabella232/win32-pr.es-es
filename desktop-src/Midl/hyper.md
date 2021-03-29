---
title: atributo de hipertexto
description: La palabra clave Hyper indica un entero de 64 bits que se puede declarar como con signo o sin signo.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- hiperatributo MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783605"
---
# <a name="hyper-attribute"></a><span data-ttu-id="5fb22-104">atributo de hipertexto</span><span class="sxs-lookup"><span data-stu-id="5fb22-104">hyper attribute</span></span>

<span data-ttu-id="5fb22-105">La palabra clave **Hyper** indica un entero de 64 bits que se puede declarar como con signo o sin signo.</span><span class="sxs-lookup"><span data-stu-id="5fb22-105">The keyword **hyper** indicates a 64-bit integer that can be declared as either signed or unsigned.</span></span>

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="5fb22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fb22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb22-107">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="5fb22-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5fb22-108">Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="5fb22-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="5fb22-109">(Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="5fb22-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="5fb22-110">Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.</span><span class="sxs-lookup"><span data-stu-id="5fb22-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fb22-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fb22-111">Remarks</span></span>

<span data-ttu-id="5fb22-112">El **hipertipo es uno de los tipos** base del lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="5fb22-112">The **hyper** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="5fb22-113">El  hipertipo puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="5fb22-113">The **hyper** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="5fb22-114">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="5fb22-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="5fb22-115">En las plataformas de 16 bits, el compilador MIDL reemplaza los hiperenteros sin signo con **MIDL \_ uhyper**.</span><span class="sxs-lookup"><span data-stu-id="5fb22-115">For 16-bit platforms, the MIDL compiler replaces unsigned hyper integers with **MIDL\_uhyper**.</span></span> <span data-ttu-id="5fb22-116">Esto permite definir interfaces con hiperenteros sin signo en plataformas que no admiten directamente enteros de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5fb22-116">This allows interfaces with unsigned hyper integers to be defined on platforms that do not directly support 64-bit integers.</span></span> <span data-ttu-id="5fb22-117">**MIDL \_ uhyper** se define en los archivos de encabezado de RPC.</span><span class="sxs-lookup"><span data-stu-id="5fb22-117">**MIDL\_uhyper** is defined in the RPC header files.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5fb22-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fb22-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb22-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="5fb22-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="5fb22-120">**const**</span><span class="sxs-lookup"><span data-stu-id="5fb22-120">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="5fb22-121">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="5fb22-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5fb22-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="5fb22-122">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




