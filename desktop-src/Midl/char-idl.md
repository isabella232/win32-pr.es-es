---
title: Char (atributo)
description: La palabra clave char especifica un elemento de datos de 8 bits.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- Char (atributo) MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904198"
---
# <a name="char-attribute"></a><span data-ttu-id="acf5f-104">Char (atributo)</span><span class="sxs-lookup"><span data-stu-id="acf5f-104">char attribute</span></span>

<span data-ttu-id="acf5f-105">La palabra clave **Char** especifica un elemento de datos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="acf5f-105">The **char** keyword specifies an 8-bit data item.</span></span>

``` syntax
char identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="acf5f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acf5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf5f-107">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="acf5f-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="acf5f-108">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="acf5f-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="acf5f-109">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="acf5f-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acf5f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acf5f-110">Remarks</span></span>

<span data-ttu-id="acf5f-111">La palabra clave **Char** identifica un elemento de datos que tiene 8 bits.</span><span class="sxs-lookup"><span data-stu-id="acf5f-111">The keyword **char** identifies a data item that has 8 bits.</span></span> <span data-ttu-id="acf5f-112">En el compilador de MIDL, un **carácter** no tiene signo de forma predeterminada y es sinónimo de **carácter** [**sin signo**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="acf5f-112">To the MIDL compiler, a **char** is unsigned by default and is synonymous with [**unsigned**](unsigned.md) **char**.</span></span>

<span data-ttu-id="acf5f-113">En esta versión de Microsoft RPC, las tablas de traducción de caracteres que se convierten entre ASCII y EBCDIC están integradas en las bibliotecas en tiempo de ejecución y el usuario no puede cambiarlas.</span><span class="sxs-lookup"><span data-stu-id="acf5f-113">In this version of Microsoft RPC, the character translation tables that convert between ASCII and EBCDIC are built into the run-time libraries and cannot be changed by the user.</span></span>

<span data-ttu-id="acf5f-114">El tipo **Char** es uno de los tipos base del lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="acf5f-114">The **char** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="acf5f-115">El tipo **Char** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="acf5f-115">The **char** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="acf5f-116">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="acf5f-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="acf5f-117">Los compiladores de DCE IDL no aceptan la palabra clave [**signed**](signed.md) aplicada a tipos **Char** .</span><span class="sxs-lookup"><span data-stu-id="acf5f-117">DCE IDL compilers do not accept the keyword [**signed**](signed.md) applied to **char** types.</span></span> <span data-ttu-id="acf5f-118">Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="acf5f-118">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

## <a name="see-also"></a><span data-ttu-id="acf5f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="acf5f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf5f-120">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="acf5f-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="acf5f-121">**bytes**</span><span class="sxs-lookup"><span data-stu-id="acf5f-121">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="acf5f-122">**/Char**</span><span class="sxs-lookup"><span data-stu-id="acf5f-122">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="acf5f-123">**const**</span><span class="sxs-lookup"><span data-stu-id="acf5f-123">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="acf5f-124">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="acf5f-124">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="acf5f-125">**/osf**</span><span class="sxs-lookup"><span data-stu-id="acf5f-125">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="acf5f-126">**conectado**</span><span class="sxs-lookup"><span data-stu-id="acf5f-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="acf5f-127">**string**</span><span class="sxs-lookup"><span data-stu-id="acf5f-127">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="acf5f-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="acf5f-128">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="acf5f-129">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="acf5f-129">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="acf5f-130">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="acf5f-130">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




