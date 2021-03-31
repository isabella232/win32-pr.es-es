---
title: wchar_t atributo)
description: La \_ palabra clave WCHAR t designa un tipo de caracteres anchos.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t el atributo MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2020
ms.locfileid: "104077408"
---
# <a name="wchar_t-attribute"></a><span data-ttu-id="9ff91-104">WCHAR \_ t (atributo)</span><span class="sxs-lookup"><span data-stu-id="9ff91-104">wchar\_t attribute</span></span>

<span data-ttu-id="9ff91-105">La palabra clave **WCHAR \_ t** designa un tipo de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="9ff91-105">The **wchar\_t** keyword designates a wide-character type.</span></span>

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="9ff91-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ff91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff91-107">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="9ff91-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9ff91-108">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="9ff91-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="9ff91-109">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="9ff91-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ff91-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ff91-110">Remarks</span></span>

<span data-ttu-id="9ff91-111">El tipo **WCHAR \_ t** lo define MIDL como un objeto de datos [**Short**](short.md) (de 16 bits) [**sin signo**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff91-111">The **wchar\_t** type is defined by MIDL as an [**unsigned**](unsigned.md) [**short**](short.md) (16-bit) data object.</span></span>

<span data-ttu-id="9ff91-112">El compilador MIDL permite la redefinición de **WCHAR \_ t**, pero solo si es coherente con la definición anterior.</span><span class="sxs-lookup"><span data-stu-id="9ff91-112">The MIDL compiler allows redefinition of **wchar\_t**, but only if it is consistent with the preceding definition.</span></span>

<span data-ttu-id="9ff91-113">El tipo de carácter ancho es uno de los tipos predefinidos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="9ff91-113">The wide-character type is one of the predefined types of MIDL.</span></span> <span data-ttu-id="9ff91-114">El tipo de caracteres anchos puede aparecer como un especificador de tipo en las declaraciones [**const**](const.md) , en las declaraciones [**typedef**](typedef.md) , en las declaraciones generales y en los declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="9ff91-114">The wide-character type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="9ff91-115">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="9ff91-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="9ff91-116">El atributo de **\[ cadena \]** se puede aplicar a un puntero o una matriz de tipo **WCHAR \_ t**.</span><span class="sxs-lookup"><span data-stu-id="9ff91-116">The **\[string\]** attribute can be applied to a pointer or array of type **wchar\_t**.</span></span>

<span data-ttu-id="9ff91-117">Use el carácter **L** delante de un carácter o una constante de cadena para designar la constante de tipo de carácter ancho.</span><span class="sxs-lookup"><span data-stu-id="9ff91-117">Use the **L** character before a character or a string constant to designate the wide character type constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ff91-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ff91-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff91-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="9ff91-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="9ff91-120">**char**</span><span class="sxs-lookup"><span data-stu-id="9ff91-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="9ff91-121">**const**</span><span class="sxs-lookup"><span data-stu-id="9ff91-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="9ff91-122">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="9ff91-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9ff91-123">**short**</span><span class="sxs-lookup"><span data-stu-id="9ff91-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="9ff91-124">**typedef**</span><span class="sxs-lookup"><span data-stu-id="9ff91-124">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="9ff91-125">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="9ff91-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




