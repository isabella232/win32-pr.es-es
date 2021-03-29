---
title: propputref (atributo)
description: El atributo \ PROPPUTREF \ especifica una función de configuración de propiedades que usa una referencia en lugar de un valor.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- atributo PROPPUTREF MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995131"
---
# <a name="propputref-attribute"></a><span data-ttu-id="55e5d-104">propputref (atributo)</span><span class="sxs-lookup"><span data-stu-id="55e5d-104">propputref attribute</span></span>

<span data-ttu-id="55e5d-105">El atributo **\[ PROPPUTREF \]** especifica una función de configuración de propiedades que usa una referencia en lugar de un valor.</span><span class="sxs-lookup"><span data-stu-id="55e5d-105">The **\[propputref\]** attribute specifies a property-setting function that uses a reference instead of a value.</span></span>

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="55e5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55e5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55e5d-107">*Optional-Property-Attributes*</span><span class="sxs-lookup"><span data-stu-id="55e5d-107">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="55e5d-108">Cero o más atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="55e5d-108">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="55e5d-109">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="55e5d-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="55e5d-110">Tipo de los datos devueltos por el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="55e5d-110">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="55e5d-111">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="55e5d-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="55e5d-112">Nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="55e5d-112">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="55e5d-113">*parameters*</span><span class="sxs-lookup"><span data-stu-id="55e5d-113">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="55e5d-114">Cero o más parámetros para el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="55e5d-114">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55e5d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55e5d-115">Remarks</span></span>

<span data-ttu-id="55e5d-116">Una función que tenga el atributo **\[ PROPPUTREF \]** también debe tener, como el último parámetro, un puntero con el atributo **\[** [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="55e5d-116">A function that has the **\[propputref\]** attribute must also have, as its last parameter, a pointer that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="55e5d-117">La propiedad debe tener el mismo nombre que la función.</span><span class="sxs-lookup"><span data-stu-id="55e5d-117">The property must have the same name as the function.</span></span> <span data-ttu-id="55e5d-118">Como máximo, **\[** [](propget.md) **\]** **\[** [](propput.md) **\]** se puede especificar uno de los atributos propget, PROPPUT y **\[ PROPPUTREF \]** para una función.</span><span class="sxs-lookup"><span data-stu-id="55e5d-118">At most, one of **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]** and **\[propputref\]** attributes can be specified for a function.</span></span>

### <a name="flags"></a><span data-ttu-id="55e5d-119">Marcas</span><span class="sxs-lookup"><span data-stu-id="55e5d-119">Flags</span></span>

<span data-ttu-id="55e5d-120">INVOCAr \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="55e5d-120">INVOKE\_PROPERTYPUTREF</span></span>

## <a name="examples"></a><span data-ttu-id="55e5d-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="55e5d-121">Examples</span></span>

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a><span data-ttu-id="55e5d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="55e5d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e5d-123">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="55e5d-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="55e5d-124">**de**</span><span class="sxs-lookup"><span data-stu-id="55e5d-124">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="55e5d-125">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="55e5d-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="55e5d-126">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="55e5d-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="55e5d-127">**propget**</span><span class="sxs-lookup"><span data-stu-id="55e5d-127">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="55e5d-128">**PROPPUT**</span><span class="sxs-lookup"><span data-stu-id="55e5d-128">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="55e5d-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="55e5d-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 