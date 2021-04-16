---
title: Float (atributo)
description: La palabra clave Float designa un número de punto flotante de 32 bits.
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- atributo Float de MIDL
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82d298506c5117c0643df8ecea841832d5f923
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685628"
---
# <a name="float-attribute"></a><span data-ttu-id="65511-104">Float (atributo)</span><span class="sxs-lookup"><span data-stu-id="65511-104">float attribute</span></span>

<span data-ttu-id="65511-105">La palabra clave **float** designa un número de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="65511-105">The **float** keyword designates a 32-bit floating-point number.</span></span>

``` syntax
float identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="65511-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65511-107">*identificador: nombre*</span><span class="sxs-lookup"><span data-stu-id="65511-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65511-108">Especifica un identificador de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="65511-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="65511-109">Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="65511-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65511-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65511-110">Remarks</span></span>

<span data-ttu-id="65511-111">El tipo **float** es uno de los tipos base del lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="65511-111">The **float** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="65511-112">El tipo **float** puede aparecer como un especificador de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="65511-112">The **float** type can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="65511-113">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="65511-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="65511-114">El tipo **float** no puede aparecer en las declaraciones [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="65511-114">The **float** type cannot appear in [**const**](const.md) declarations.</span></span>

## <a name="see-also"></a><span data-ttu-id="65511-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="65511-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65511-116">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="65511-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="65511-117">**double**</span><span class="sxs-lookup"><span data-stu-id="65511-117">**double**</span></span>](double.md)
</dt> <dt>

[<span data-ttu-id="65511-118">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="65511-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="65511-119">**typedef**</span><span class="sxs-lookup"><span data-stu-id="65511-119">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




