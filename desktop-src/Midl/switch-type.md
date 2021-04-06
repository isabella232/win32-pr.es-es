---
title: switch_type (atributo)
description: El atributo \ switch \_ Type \ identifica el tipo de la variable que se usa como discriminante de Unión. El tipo de modificador puede ser un entero, un carácter, un valor booleano o un tipo de enumeración.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type el atributo MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904129"
---
# <a name="switch_type-attribute"></a><span data-ttu-id="87e63-105">atributo de tipo de conmutador \_</span><span class="sxs-lookup"><span data-stu-id="87e63-105">switch\_type attribute</span></span>

<span data-ttu-id="87e63-106">El atributo de **\[ \_ tipo \] de conmutador** identifica el tipo de la variable que se usa como discriminante de Unión.</span><span class="sxs-lookup"><span data-stu-id="87e63-106">The **\[switch\_type\]** attribute identifies the type of the variable used as the union discriminant.</span></span> <span data-ttu-id="87e63-107">El tipo de modificador puede ser un entero, un carácter, un valor booleano o un tipo de enumeración.</span><span class="sxs-lookup"><span data-stu-id="87e63-107">The switch type can be an integer, character, Boolean, or enumeration type.</span></span>

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a><span data-ttu-id="87e63-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87e63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e63-109">*Switch-Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="87e63-109">*switch-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="87e63-110">Especifica un tipo [**int**](int.md), [**Char**](char-idl.md), [**Boolean**](boolean.md)o [**enum**](enum.md) , o un identificador de este tipo.</span><span class="sxs-lookup"><span data-stu-id="87e63-110">Specifies an [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md), or [**enum**](enum.md) type, or an identifier of such a type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87e63-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87e63-111">Remarks</span></span>

<span data-ttu-id="87e63-112">Mientras que el atributo de **\[ \_ tipo \] de conmutador** identifica el tipo de variable, el **\[** atributo [**Switch \_ es**](switch-is.md) **\]** especifica el nombre del parámetro que es la Unión discriminante.</span><span class="sxs-lookup"><span data-stu-id="87e63-112">While the **\[switch\_type\]** attribute identifies the variable type, the **\[**[**switch\_is**](switch-is.md)**\]** attribute specifies the name of the parameter that is the union discriminant.</span></span> <span data-ttu-id="87e63-113">El atributo de **\[ \_ tipo \] de conmutador** se aplica a los parámetros o miembros de estructuras o uniones.</span><span class="sxs-lookup"><span data-stu-id="87e63-113">The **\[switch\_type\]** attribute applies to parameters or members of structures or unions.</span></span>

<span data-ttu-id="87e63-114">La Unión y su discriminante deben especificarse en el mismo nivel lógico.</span><span class="sxs-lookup"><span data-stu-id="87e63-114">The union and its discriminant must be specified at the same logical level.</span></span> <span data-ttu-id="87e63-115">Cuando la Unión es un parámetro, el discriminante de Unión debe ser otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="87e63-115">When the union is a parameter, the union discriminant must be another parameter.</span></span> <span data-ttu-id="87e63-116">Cuando la Unión es un campo de una estructura, el discriminante debe ser otro campo de la estructura en el mismo nivel que el campo de Unión.</span><span class="sxs-lookup"><span data-stu-id="87e63-116">When the union is a field of a structure, the discriminant must be another field of the structure at the same level as the union field.</span></span>

## <a name="examples"></a><span data-ttu-id="87e63-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="87e63-117">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="87e63-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="87e63-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e63-119">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="87e63-119">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="87e63-120">**char**</span><span class="sxs-lookup"><span data-stu-id="87e63-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="87e63-121">Uniones encapsuladas</span><span class="sxs-lookup"><span data-stu-id="87e63-121">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="87e63-122">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="87e63-122">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="87e63-123">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="87e63-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="87e63-124">**Inter**</span><span class="sxs-lookup"><span data-stu-id="87e63-124">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="87e63-125">Uniones no encapsuladas</span><span class="sxs-lookup"><span data-stu-id="87e63-125">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="87e63-126">**el modificador \_ es**</span><span class="sxs-lookup"><span data-stu-id="87e63-126">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="87e63-127">**Unión**</span><span class="sxs-lookup"><span data-stu-id="87e63-127">**union**</span></span>](union.md)
</dt> </dl>

 

 




