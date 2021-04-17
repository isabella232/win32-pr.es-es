---
title: byte (atributo)
description: La palabra clave byte especifica un elemento de datos de 8 bits.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- atributo de byte MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651339"
---
# <a name="byte-attribute"></a><span data-ttu-id="fadfc-104">byte (atributo)</span><span class="sxs-lookup"><span data-stu-id="fadfc-104">byte attribute</span></span>

<span data-ttu-id="fadfc-105">La palabra clave **byte** especifica un elemento de datos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="fadfc-105">The **byte** keyword specifies an 8-bit data item.</span></span>

``` syntax
byte identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="fadfc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fadfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fadfc-107">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="fadfc-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fadfc-108">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="fadfc-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="fadfc-109">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="fadfc-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fadfc-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fadfc-110">Remarks</span></span>

<span data-ttu-id="fadfc-111">Un elemento de datos de **bytes** no se somete a ninguna conversión de transmisión en la red como un tipo [**Char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="fadfc-111">A **byte** data item does not undergo any conversion for transmission on the network as a [**char**](char-idl.md) type might.</span></span>

<span data-ttu-id="fadfc-112">El tipo de **byte** es uno de los tipos base del lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="fadfc-112">The **byte** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="fadfc-113">El tipo **byte** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="fadfc-113">The **byte** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="fadfc-114">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="fadfc-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fadfc-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="fadfc-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fadfc-116">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="fadfc-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="fadfc-117">**char**</span><span class="sxs-lookup"><span data-stu-id="fadfc-117">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="fadfc-118">**const**</span><span class="sxs-lookup"><span data-stu-id="fadfc-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="fadfc-119">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="fadfc-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fadfc-120">**typedef**</span><span class="sxs-lookup"><span data-stu-id="fadfc-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




