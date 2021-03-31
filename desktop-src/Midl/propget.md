---
title: propget (atributo)
description: El atributo \ propget \ especifica una función de descriptor de acceso de propiedad. La propiedad debe tener el mismo nombre que la función.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- propget (atributo) MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077596"
---
# <a name="propget-attribute"></a><span data-ttu-id="6a0a1-105">propget (atributo)</span><span class="sxs-lookup"><span data-stu-id="6a0a1-105">propget attribute</span></span>

<span data-ttu-id="6a0a1-106">El atributo **\[ propget \]** especifica una función de descriptor de acceso de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-106">The **\[propget\]** attribute specifies a property accessor function.</span></span> <span data-ttu-id="6a0a1-107">La propiedad debe tener el mismo nombre que la función.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-107">The property must have the same name as the function.</span></span>

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="6a0a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a0a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a0a1-109">*Optional-Property-Attributes*</span><span class="sxs-lookup"><span data-stu-id="6a0a1-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="6a0a1-110">Cero o más atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="6a0a1-111">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="6a0a1-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="6a0a1-112">Tipo de los datos devueltos por el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="6a0a1-113">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="6a0a1-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6a0a1-114">Nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="6a0a1-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="6a0a1-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="6a0a1-116">Cero o más parámetros para el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a0a1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a0a1-117">Remarks</span></span>

<span data-ttu-id="6a0a1-118">Una función que tiene el atributo propget también debe tener, como su último parámetro, un tipo de puntero con los **\[** atributos [**out**](out-idl.md) **\]** y **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="6a0a1-118">A function that has the propget attribute should also have, as its last parameter, a pointer type with the **\[**[**out**](out-idl.md)**\]** and **\[**[**retval**](retval.md)**\]** attributes.</span></span> <span data-ttu-id="6a0a1-119">Si el último parámetro no tiene los \[ atributos out, retval \] , el valor devuelto de la función se trata como un \[ parámetro out, retval \] .</span><span class="sxs-lookup"><span data-stu-id="6a0a1-119">If the last parameter does not have the \[out, retval\] attributes, the return value of the function is treated as an \[out, retval\] parameter.</span></span> <span data-ttu-id="6a0a1-120">Por ejemplo, una función con el prototipo</span><span class="sxs-lookup"><span data-stu-id="6a0a1-120">For example, a function with the prototype</span></span>

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

<span data-ttu-id="6a0a1-121">se trata como</span><span class="sxs-lookup"><span data-stu-id="6a0a1-121">is treated as</span></span>

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

<span data-ttu-id="6a0a1-122">Como máximo, se puede especificar una de **\[ propget \]**, **\[** [**PROPPUT**](propput.md) **\]** y **\[** [**PROPPUTREF**](propputref.md) **\]** para una función.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-122">At most, one of **\[propget\]**, **\[**[**propput**](propput.md)**\]**, and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="6a0a1-123">Si el **\[** atributo [**LCID**](lcid.md) **\]** se utiliza en la lista de parámetros de una función que contiene un parámetro con el **\[** atributo [**PROPPUT**](propput.md) **\]** , el parámetro **\[ LCID \]** debe ser el segundo en el último.</span><span class="sxs-lookup"><span data-stu-id="6a0a1-123">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[**[**propput**](propput.md)**\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="6a0a1-124">Marcas</span><span class="sxs-lookup"><span data-stu-id="6a0a1-124">Flags</span></span>

<span data-ttu-id="6a0a1-125">INVOCAr \_ PropertyGet (</span><span class="sxs-lookup"><span data-stu-id="6a0a1-125">INVOKE\_PROPERTYGET</span></span>

## <a name="examples"></a><span data-ttu-id="6a0a1-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6a0a1-126">Examples</span></span>

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a><span data-ttu-id="6a0a1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a0a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a0a1-128">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="6a0a1-128">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="6a0a1-129">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="6a0a1-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6a0a1-130">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="6a0a1-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6a0a1-131">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="6a0a1-131">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="6a0a1-132">**retval**</span><span class="sxs-lookup"><span data-stu-id="6a0a1-132">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="6a0a1-133">**PROPPUT**</span><span class="sxs-lookup"><span data-stu-id="6a0a1-133">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="6a0a1-134">**PROPPUTREF**</span><span class="sxs-lookup"><span data-stu-id="6a0a1-134">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="6a0a1-135">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="6a0a1-135">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 