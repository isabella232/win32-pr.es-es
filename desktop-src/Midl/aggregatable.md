---
title: aggregatable (atributo)
description: El atributo \ aggregateable \ indica que la clase admite la agregación.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- atributo agregable MIDL
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358876"
---
# <a name="aggregatable-attribute"></a><span data-ttu-id="cbd49-104">aggregatable (atributo)</span><span class="sxs-lookup"><span data-stu-id="cbd49-104">aggregatable attribute</span></span>

<span data-ttu-id="cbd49-105">El atributo **\[ agregable \]** indica que la clase admite la agregación.</span><span class="sxs-lookup"><span data-stu-id="cbd49-105">The **\[aggregatable\]** attribute indicates that the class supports aggregation.</span></span>

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="cbd49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbd49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbd49-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="cbd49-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd49-108">Otros atributos que se aplican a la clase.</span><span class="sxs-lookup"><span data-stu-id="cbd49-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="cbd49-109">*nombre de coclase*</span><span class="sxs-lookup"><span data-stu-id="cbd49-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd49-110">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="cbd49-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="cbd49-111">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="cbd49-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd49-112">Una lista de interfaces para la clase.</span><span class="sxs-lookup"><span data-stu-id="cbd49-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbd49-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbd49-113">Remarks</span></span>

<span data-ttu-id="cbd49-114">Utilice el atributo **\[ agregable \]** en una instrucción de [**coclase**](coclass.md) para permitir que los usuarios sepan que la clase admite agregaciones.</span><span class="sxs-lookup"><span data-stu-id="cbd49-114">Use the **\[aggregatable\]** attribute on a [**coclass**](coclass.md) statement to let users know that the class supports aggregations.</span></span> <span data-ttu-id="cbd49-115">Es decir, la clase permite que una clase contenedora exponga sus interfaces como si fueran las interfaces propias del contenedor.</span><span class="sxs-lookup"><span data-stu-id="cbd49-115">That is, the class allows its interfaces to be exposed by a container class as if these interfaces were the container's own interfaces.</span></span>

<span data-ttu-id="cbd49-116">La representación typeflag para este atributo es TYPEFLAG \_ FAGGREGATABLE.</span><span class="sxs-lookup"><span data-stu-id="cbd49-116">The typeflag representation for this attribute is TYPEFLAG\_FAGGREGATABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="cbd49-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cbd49-117">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="cbd49-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbd49-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd49-119">**coclase**</span><span class="sxs-lookup"><span data-stu-id="cbd49-119">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="cbd49-120">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="cbd49-120">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="cbd49-121">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="cbd49-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="cbd49-122">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="cbd49-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 