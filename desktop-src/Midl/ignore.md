---
title: omitir atributo
description: El atributo \ ignore \ designa que no se transmite un puntero contenido en una estructura o Unión y el objeto indicado por el puntero. El atributo \ ignore \ está restringido a los miembros de puntero de estructuras o uniones.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- omitir el atributo MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904539"
---
# <a name="ignore-attribute"></a><span data-ttu-id="f7853-105">omitir atributo</span><span class="sxs-lookup"><span data-stu-id="f7853-105">ignore attribute</span></span>

<span data-ttu-id="f7853-106">El atributo **\[ Ignore \]** designa que no se transmite un puntero contenido en una estructura o Unión y el objeto indicado por el puntero.</span><span class="sxs-lookup"><span data-stu-id="f7853-106">The **\[ignore\]** attribute designates that a pointer contained in a structure or union and the object indicated by the pointer is not transmitted.</span></span> <span data-ttu-id="f7853-107">El atributo **\[ Ignore \]** está restringido a los miembros de puntero de estructuras o uniones.</span><span class="sxs-lookup"><span data-stu-id="f7853-107">The **\[ignore\]** attribute is restricted to pointer members of structures or unions.</span></span>

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a><span data-ttu-id="f7853-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7853-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7853-109">*tipo de miembro de puntero*</span><span class="sxs-lookup"><span data-stu-id="f7853-109">*pointer-member-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f7853-110">Especifica el tipo del miembro de puntero de la estructura o Unión.</span><span class="sxs-lookup"><span data-stu-id="f7853-110">Specifies the type of the pointer member of the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="f7853-111">*puntero: nombre*</span><span class="sxs-lookup"><span data-stu-id="f7853-111">*pointer-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f7853-112">Especifica el nombre del miembro de puntero que se va a omitir durante el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="f7853-112">Specifies the name of the pointer member that is to be ignored during marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7853-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7853-113">Remarks</span></span>

<span data-ttu-id="f7853-114">El valor de un miembro de estructura con el atributo **\[ Ignore \]** no está definido en el destino.</span><span class="sxs-lookup"><span data-stu-id="f7853-114">The value of a structure member with the **\[ignore\]** attribute is undefined at the destination.</span></span> <span data-ttu-id="f7853-115">Un **\[** parámetro [**in**](in.md) **\]** no está definido en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="f7853-115">An **\[**[**in**](in.md)**\]** parameter is not defined at the remote computer.</span></span> <span data-ttu-id="f7853-116">Un **\[** parámetro [**out**](out-idl.md) **\]** no está definido en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="f7853-116">An **\[**[**out**](out-idl.md)**\]** parameter is not defined at the local computer.</span></span>

<span data-ttu-id="f7853-117">El atributo **\[ Ignore \]** permite evitar la transmisión de datos.</span><span class="sxs-lookup"><span data-stu-id="f7853-117">The **\[ignore\]** attribute allows you to prevent transmission of data.</span></span> <span data-ttu-id="f7853-118">Esto resulta útil en situaciones como una lista de vínculos dobles.</span><span class="sxs-lookup"><span data-stu-id="f7853-118">This is useful in situations such as a double-linked list.</span></span> <span data-ttu-id="f7853-119">En el ejemplo siguiente se incluye una lista de vínculos dobles que presenta los alias de datos:</span><span class="sxs-lookup"><span data-stu-id="f7853-119">The following example includes a double-linked list that introduces data aliasing:</span></span>

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

<span data-ttu-id="f7853-120">El alias se produce en el ejemplo anterior porque el mismo área de memoria está disponible en dos punteros diferentes en la función **p** y **p->siguiente->anterior**.</span><span class="sxs-lookup"><span data-stu-id="f7853-120">Aliasing occurs in the preceding example because the same memory area is available from two different pointers in the function **p** and **p->next->previous**.</span></span>

<span data-ttu-id="f7853-121">Tenga en cuenta que no se puede usar **\[ Ignore \]** como atributo de tipo.</span><span class="sxs-lookup"><span data-stu-id="f7853-121">Note that **\[ignore\]** cannot be used as a type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="f7853-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f7853-122">Examples</span></span>

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="f7853-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7853-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7853-124">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="f7853-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="f7853-125">**matrices**</span><span class="sxs-lookup"><span data-stu-id="f7853-125">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="f7853-126">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="f7853-126">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="f7853-127">**de**</span><span class="sxs-lookup"><span data-stu-id="f7853-127">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="f7853-128">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="f7853-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f7853-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="f7853-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="f7853-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="f7853-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="f7853-131">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="f7853-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 