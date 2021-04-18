---
title: noncreatable (atributo)
description: El atributo \ noncreatable \ define un objeto del que no se pueden crear instancias de sí mismo.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL de atributo no creatable
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358865"
---
# <a name="noncreatable-attribute"></a><span data-ttu-id="62496-104">noncreatable (atributo)</span><span class="sxs-lookup"><span data-stu-id="62496-104">noncreatable attribute</span></span>

<span data-ttu-id="62496-105">El atributo **\[ noncreatable \]** define un objeto del que no se pueden crear instancias de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="62496-105">The **\[noncreatable\]** attribute defines an object that cannot be instantiated by itself.</span></span>

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="62496-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62496-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62496-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="62496-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="62496-108">Otros atributos que se aplican a la clase.</span><span class="sxs-lookup"><span data-stu-id="62496-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="62496-109">*nombre de coclase*</span><span class="sxs-lookup"><span data-stu-id="62496-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="62496-110">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="62496-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="62496-111">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="62496-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="62496-112">Una lista de interfaces para la clase.</span><span class="sxs-lookup"><span data-stu-id="62496-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62496-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62496-113">Remarks</span></span>

<span data-ttu-id="62496-114">Use el atributo **\[ noncreatable \]** en una instrucción de [**coclase**](coclass.md) para indicar a los usuarios que no pueden crear un nuevo objeto de esta clase en el nivel superior, es decir, mediante una llamada a **CreateInstance** o **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="62496-114">Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**.</span></span> <span data-ttu-id="62496-115">La creación de instancias de un objeto de esta clase requiere una llamada de método a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="62496-115">Instantiation of an object of this class requires a method call to another object.</span></span> <span data-ttu-id="62496-116">Por ejemplo, en Microsoft Excel, el objeto "Cell" no se puede crear y se debe obtener de un objeto de hoja de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="62496-116">For example, in Microsoft Excel, the "Cell" object is noncreatable and must be obtained from a Microsoft Excel Worksheet object.</span></span>

<span data-ttu-id="62496-117">Los métodos que devuelven instancias de clases que no se pueden crear deben devolver el tipo exacto del objeto, en lugar de los tipos **Variant** o **IDispatch** \* .</span><span class="sxs-lookup"><span data-stu-id="62496-117">Methods that return instances of noncreatable classes should return the exact type of the object, rather than **VARIANT** or **IDispatch**\* types.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="62496-118">Representación de Typeflag:</span><span class="sxs-lookup"><span data-stu-id="62496-118">Typeflag Representation:</span></span>

<span data-ttu-id="62496-119">Ausencia de TYPEFLAG \_ FCANCREATE.</span><span class="sxs-lookup"><span data-stu-id="62496-119">The absence of TYPEFLAG\_FCANCREATE.</span></span>

## <a name="examples"></a><span data-ttu-id="62496-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="62496-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="62496-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="62496-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62496-122">**coclase**</span><span class="sxs-lookup"><span data-stu-id="62496-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="62496-123">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="62496-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="62496-124">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="62496-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="62496-125">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="62496-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 