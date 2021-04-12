---
title: handle_t atributo)
description: La \_ palabra clave handler t declara un objeto para que sea del identificador de tipo de identificador primitivo \_ t. Un identificador de enlace primitivo es un objeto de datos que la aplicación puede usar para representar el enlace.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t el atributo MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358869"
---
# <a name="handle_t-attribute"></a><span data-ttu-id="d80d2-105">Handle \_ t (atributo)</span><span class="sxs-lookup"><span data-stu-id="d80d2-105">handle\_t attribute</span></span>

<span data-ttu-id="d80d2-106">La palabra clave **handler \_ t** declara un objeto para que sea del identificador de tipo de identificador primitivo **\_ t**.</span><span class="sxs-lookup"><span data-stu-id="d80d2-106">The **handle\_t** keyword declares an object to be of the primitive handle type **handle\_t**.</span></span> <span data-ttu-id="d80d2-107">Un identificador de enlace primitivo es un objeto de datos que la aplicación puede usar para representar el enlace.</span><span class="sxs-lookup"><span data-stu-id="d80d2-107">A primitive binding handle is a data object that can be used by the application to represent the binding.</span></span>

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a><span data-ttu-id="d80d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d80d2-108">Parameters</span></span>

<span data-ttu-id="d80d2-109">Este atributo no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d80d2-109">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d80d2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d80d2-110">Remarks</span></span>

<span data-ttu-id="d80d2-111">El **tipo \_ t de identificador** es uno de los tipos predefinidos del lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="d80d2-111">The **handle\_t** type is one of the predefined types of the interface definition language (IDL).</span></span> <span data-ttu-id="d80d2-112">Puede aparecer como un especificador de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="d80d2-112">It can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="d80d2-113">Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="d80d2-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="d80d2-114">En Microsoft RPC, los parámetros de **identificador \_** de tipo t solo se pueden producir como **\[** parámetros [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d80d2-114">In Microsoft RPC, parameters of type **handle\_t** can occur only as **\[**[**in**](in.md)**\]** parameters.</span></span> <span data-ttu-id="d80d2-115">Los identificadores primitivos no pueden tener el **\[** atributo [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d80d2-115">Primitive handles cannot have the **\[**[**unique**](unique.md)**\]** or **\[**[**ptr**](ptr.md)**\]** attribute.</span></span>

<span data-ttu-id="d80d2-116">Los parámetros de **identificador \_** de tipo t (parámetros de identificador primitivo) no se transmiten en la red.</span><span class="sxs-lookup"><span data-stu-id="d80d2-116">Parameters of type **handle\_t** (primitive handle parameters) are not transmitted on the network.</span></span>

## <a name="see-also"></a><span data-ttu-id="d80d2-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="d80d2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d80d2-118">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="d80d2-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="d80d2-119">Enlace y controladores</span><span class="sxs-lookup"><span data-stu-id="d80d2-119">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="d80d2-120">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="d80d2-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d80d2-121">**de**</span><span class="sxs-lookup"><span data-stu-id="d80d2-121">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="d80d2-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="d80d2-122">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="d80d2-123">**ptr**</span><span class="sxs-lookup"><span data-stu-id="d80d2-123">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="d80d2-124">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="d80d2-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 