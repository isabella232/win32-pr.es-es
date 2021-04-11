---
title: propput (atributo)
description: El atributo \ PROPPUT \ especifica una función de configuración de propiedades. La propiedad debe tener el mismo nombre que la función.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- atributo de PROPPUT (MIDL)
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149204"
---
# <a name="propput-attribute"></a><span data-ttu-id="fe648-105">propput (atributo)</span><span class="sxs-lookup"><span data-stu-id="fe648-105">propput attribute</span></span>

<span data-ttu-id="fe648-106">El atributo **\[ PROPPUT \]** especifica una función de configuración de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fe648-106">The **\[propput\]** attribute specifies a property-setting function.</span></span> <span data-ttu-id="fe648-107">La propiedad debe tener el mismo nombre que la función *.*</span><span class="sxs-lookup"><span data-stu-id="fe648-107">The property must have the same name as the function *.*</span></span>

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="fe648-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe648-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe648-109">*Optional-Property-Attributes*</span><span class="sxs-lookup"><span data-stu-id="fe648-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="fe648-110">Cero o más atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="fe648-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="fe648-111">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="fe648-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="fe648-112">Tipo de los datos devueltos por el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="fe648-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="fe648-113">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="fe648-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fe648-114">Nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="fe648-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="fe648-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="fe648-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="fe648-116">Cero o más parámetros para el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="fe648-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe648-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe648-117">Remarks</span></span>

<span data-ttu-id="fe648-118">Una función que tiene el atributo **\[ PROPPUT \]** también debe tener, como su último parámetro, un parámetro que tiene el **\[** atributo [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fe648-118">A function that has the **\[propput\]** attribute must also have, as its last parameter, a parameter that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="fe648-119">Como máximo, **\[** [](propget.md) **\]** se puede especificar una de propget, **\[ PROPPUT \]** y **\[** [**PROPPUTREF**](propputref.md) **\]** para una función.</span><span class="sxs-lookup"><span data-stu-id="fe648-119">At most, one of **\[**[**propget**](propget.md)**\]**, **\[propput\]** and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="fe648-120">Si el **\[** atributo [**LCID**](lcid.md) **\]** se utiliza en la lista de parámetros de una función que contiene un parámetro con el atributo **\[ PROPPUT \]** , el parámetro **\[ LCID \]** debe ser el segundo en el último.</span><span class="sxs-lookup"><span data-stu-id="fe648-120">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[propput\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="fe648-121">Marcas</span><span class="sxs-lookup"><span data-stu-id="fe648-121">Flags</span></span>

<span data-ttu-id="fe648-122">INVOCAr \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="fe648-122">INVOKE\_PROPERTYPUT</span></span>

## <a name="examples"></a><span data-ttu-id="fe648-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fe648-123">Examples</span></span>

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a><span data-ttu-id="fe648-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe648-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe648-125">Diferencias entre MIDL y MKTYPLIB</span><span class="sxs-lookup"><span data-stu-id="fe648-125">Differences Between MIDL and MKTYPLIB</span></span>](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[<span data-ttu-id="fe648-126">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="fe648-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fe648-127">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="fe648-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fe648-128">**propget**</span><span class="sxs-lookup"><span data-stu-id="fe648-128">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="fe648-129">**PROPPUTREF**</span><span class="sxs-lookup"><span data-stu-id="fe648-129">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="fe648-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="fe648-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 