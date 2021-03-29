---
title: dispinterface (atributo)
description: La instrucción dispinterface define un conjunto de propiedades y métodos en los que se puede llamar a IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- atributo dispinterface MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904591"
---
# <a name="dispinterface-attribute"></a><span data-ttu-id="ed301-104">dispinterface (atributo)</span><span class="sxs-lookup"><span data-stu-id="ed301-104">dispinterface attribute</span></span>

<span data-ttu-id="ed301-105">La instrucción **dispinterface** define un conjunto de propiedades y métodos en los que se puede llamar a **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="ed301-105">The **dispinterface** statement defines a set of properties and methods on which you can call **IDispatch::Invoke**.</span></span> <span data-ttu-id="ed301-106">Se puede definir una interfaz dispinterface indicando explícitamente el conjunto de métodos y propiedades admitidos (sintaxis 1), o bien enumerando una sola interfaz (sintaxis 2).</span><span class="sxs-lookup"><span data-stu-id="ed301-106">A dispinterface may be defined by explicitly listing the set of supported methods and properties (Syntax 1), or by listing a single interface (Syntax 2).</span></span>

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a><span data-ttu-id="ed301-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed301-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed301-108">*attributes*</span><span class="sxs-lookup"><span data-stu-id="ed301-108">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ed301-109">Especifica los atributos que se aplican a toda la **dispinterface**.</span><span class="sxs-lookup"><span data-stu-id="ed301-109">Specifies attributes that apply to the entire **dispinterface**.</span></span> <span data-ttu-id="ed301-110">Se aceptan los siguientes atributos: **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**nonextensible (**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** y **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ed301-110">The following attributes are accepted: **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**nonextensible**](nonextensible.md)**\]**, **\[**[**oleautomation**](oleautomation.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="ed301-111">*dispinterface: nombre*</span><span class="sxs-lookup"><span data-stu-id="ed301-111">*dispinterface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ed301-112">Nombre por el que se conoce la **dispinterface** en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="ed301-112">The name by which the **dispinterface** is known in the type library.</span></span> <span data-ttu-id="ed301-113">Este nombre debe ser único en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="ed301-113">This name must be unique within the type library.</span></span>

</dd> <dt>

<span data-ttu-id="ed301-114">*lista de propiedades*</span><span class="sxs-lookup"><span data-stu-id="ed301-114">*property-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ed301-115">(Sintaxis 1) Lista opcional de propiedades admitidas por el objeto, declaradas en forma de variables.</span><span class="sxs-lookup"><span data-stu-id="ed301-115">(Syntax 1) An optional list of properties supported by the object, declared in the form of variables.</span></span> <span data-ttu-id="ed301-116">Esta es la forma abreviada para declarar las funciones de propiedad en la lista de métodos.</span><span class="sxs-lookup"><span data-stu-id="ed301-116">This is the short form for declaring the property functions in the methods list.</span></span> <span data-ttu-id="ed301-117">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ed301-117">See the comments section for details.</span></span>

</dd> <dt>

<span data-ttu-id="ed301-118">*lista de métodos*</span><span class="sxs-lookup"><span data-stu-id="ed301-118">*method-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ed301-119">(Sintaxis 1) Lista que consta de un prototipo de función para cada método y propiedad de la **dispinterface**.</span><span class="sxs-lookup"><span data-stu-id="ed301-119">(Syntax 1) A list comprising a function prototype for each method and property in the **dispinterface**.</span></span> <span data-ttu-id="ed301-120">Puede aparecer cualquier número de definiciones de función en *methlist*.</span><span class="sxs-lookup"><span data-stu-id="ed301-120">Any number of function definitions can appear in *methlist*.</span></span> <span data-ttu-id="ed301-121">Una función de *methlist* tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed301-121">A function in *methlist* has the following form:</span></span>

<span data-ttu-id="ed301-122">\*\*\[ \] \*\*\*attributes\*\*\*\*\* *ReturnType methname Type paramName ***(*** params \* \* *);**</span><span class="sxs-lookup"><span data-stu-id="ed301-122">**\[***attributes***\]** *returntype methname type paramname ***(*** params\*\*\*);*\*</span></span>

<span data-ttu-id="ed301-123">Se aceptan los siguientes atributos en un método de una **interfaz dispinterface**: **\[ HelpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**PROPPUT**](propput.md) **\]** , **\[** [**PROPPUTREF**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**vararg**](vararg.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ed301-123">The following attributes are accepted on a method in a **dispinterface**: **\[helpstring\]**, **\[helpcontext\]**, **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]**, **\[**[**propputref**](propputref.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**vararg**](vararg.md)**\]**.</span></span> <span data-ttu-id="ed301-124">Si se especifica **\[ \] vararg** , el último parámetro debe ser una matriz segura de tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="ed301-124">If **\[vararg\]** is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="ed301-125">La lista de parámetros es una lista delimitada por comas, donde cada elemento tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed301-125">The parameter list is a comma-delimited list, each element of which has the following form:</span></span>

<span data-ttu-id="ed301-126">**\[***sus***\]**</span><span class="sxs-lookup"><span data-stu-id="ed301-126">**\[***attributes***\]**</span></span>

<span data-ttu-id="ed301-127">El *tipo* puede ser cualquier tipo declarado o integrado, o un puntero a cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="ed301-127">The *type* can be any declared or built-in type, or a pointer to any type.</span></span> <span data-ttu-id="ed301-128">Los atributos de los parámetros son:</span><span class="sxs-lookup"><span data-stu-id="ed301-128">Attributes on parameters are:</span></span>

<span data-ttu-id="ed301-129">**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**Optional**](optional.md) **\]** , **\[ String \]**</span><span class="sxs-lookup"><span data-stu-id="ed301-129">**\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]**, **\[**[**optional**](optional.md)**\]**, **\[string\]**</span></span>

</dd> <dt>

<span data-ttu-id="ed301-130">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="ed301-130">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ed301-131">(Sintaxis 2) Nombre de la interfaz que se va a declarar como interfaz IDispatch.</span><span class="sxs-lookup"><span data-stu-id="ed301-131">(Syntax 2) The name of the interface to declare as an IDispatch interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed301-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed301-132">Remarks</span></span>

<span data-ttu-id="ed301-133">El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):</span><span class="sxs-lookup"><span data-stu-id="ed301-133">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="ed301-134">Parámetros obligatorios (parámetros que no tienen los \[ \] atributos DefaultValue u \[ opcional \] ),</span><span class="sxs-lookup"><span data-stu-id="ed301-134">Required parameters (parameters that do not have the \[defaultvalue\] or \[optional\] attributes),</span></span>
2.  <span data-ttu-id="ed301-135">parámetros opcionales con o sin el \[ \] atributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="ed301-135">optional parameters with or without the \[defaultvalue\] attribute,</span></span>
3.  <span data-ttu-id="ed301-136">parámetros con el \[ \] atributo opcional y sin el \[ \] atributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="ed301-136">parameters with the \[optional\] attribute and without the \[defaultvalue\] attribute,</span></span>
4.  <span data-ttu-id="ed301-137">\[parámetro [**LCID**](lcid.md) \] , si existe,</span><span class="sxs-lookup"><span data-stu-id="ed301-137">\[ [**lcid**](lcid.md)\] parameter, if any,</span></span>
5.  <span data-ttu-id="ed301-138">\[[**retval**](retval.md) \] parámetro</span><span class="sxs-lookup"><span data-stu-id="ed301-138">\[ [**retval**](retval.md)\] parameter</span></span>

<span data-ttu-id="ed301-139">Las funciones de método se especifican exactamente como se describe en la página de referencia del [**módulo**](module.md) , con la excepción de que \[ [](entry.md) \] no se permite el atributo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ed301-139">Method functions are specified exactly as described in the reference page for [**module**](module.md) except that the \[ [**entry**](entry.md)\] attribute is not allowed.</span></span> <span data-ttu-id="ed301-140">Tenga en cuenta que STDOLE32. TLB (STDOLE. TLB en sistemas de 16 bits) debe importarse, ya que una **dispinterface** hereda de IDispatch.</span><span class="sxs-lookup"><span data-stu-id="ed301-140">Note that STDOLE32.TLB (STDOLE.TLB on 16-bit systems) must be imported, because a **dispinterface** inherits from IDispatch.</span></span>

<span data-ttu-id="ed301-141">Puede declarar propiedades en las listas propiedades o métodos.</span><span class="sxs-lookup"><span data-stu-id="ed301-141">You can declare properties in either the properties or methods lists.</span></span> <span data-ttu-id="ed301-142">Al declarar las propiedades en la lista de propiedades, no se indica el tipo de acceso que admite la propiedad (es decir, get, Put o putref).</span><span class="sxs-lookup"><span data-stu-id="ed301-142">Declaring properties in the properties list does not indicate the type of access the property supports (that is, get, put, or putref).</span></span> <span data-ttu-id="ed301-143">Especifique el \[ atributo [**ReadOnly**](readonly.md) \] para las propiedades que no admiten Put o putref.</span><span class="sxs-lookup"><span data-stu-id="ed301-143">Specify the \[ [**readonly**](readonly.md)\] attribute for properties that don't support put or putref.</span></span> <span data-ttu-id="ed301-144">Si declara las funciones de propiedad en la lista de métodos, las funciones de una propiedad tienen el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="ed301-144">If you declare the property functions in the methods list, functions for one property all have the same identifier.</span></span>

<span data-ttu-id="ed301-145">Con la primera sintaxis, las propiedades: y METHODS: Tags son obligatorias.</span><span class="sxs-lookup"><span data-stu-id="ed301-145">Using the first syntax, the properties: and methods: tags are required.</span></span> <span data-ttu-id="ed301-146">\[ [](id.md) \] También se requiere el atributo ID en cada miembro.</span><span class="sxs-lookup"><span data-stu-id="ed301-146">The \[ [**id**](id.md)\] attribute is also required on each member.</span></span> <span data-ttu-id="ed301-147">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ed301-147">For example:</span></span>

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

<span data-ttu-id="ed301-148">A diferencia de los miembros de interfaz, los miembros dispinterface no pueden usar el atributo [**retval**](retval.md) para devolver un valor además de un código de error HRESULT.</span><span class="sxs-lookup"><span data-stu-id="ed301-148">Unlike interface members, dispinterface members cannot use the [**retval**](retval.md) attribute to return a value in addition to an HRESULT error code.</span></span> <span data-ttu-id="ed301-149">El \[ [](lcid.md) \] atributo LCID tampoco es válido para dispinterfaces, porque IDispatch:: Invoke pasa un LCID.</span><span class="sxs-lookup"><span data-stu-id="ed301-149">The \[ [**lcid**](lcid.md)\] attribute is likewise invalid for dispinterfaces, because IDispatch::Invoke passes an LCID.</span></span> <span data-ttu-id="ed301-150">Sin embargo, es posible volver a declarar una interfaz que utilice estos atributos.</span><span class="sxs-lookup"><span data-stu-id="ed301-150">However, it is possible to redeclare an interface that uses these attributes.</span></span>

<span data-ttu-id="ed301-151">Con la segunda sintaxis, las interfaces que admiten IDispatch y que se declaran anteriormente en un script ODL se pueden volver a declarar como interfaces IDispatch como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ed301-151">Using the second syntax, interfaces that support IDispatch and are declared earlier in an ODL script can be redeclared as IDispatch interfaces as follows:</span></span>

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

<span data-ttu-id="ed301-152">En el ejemplo anterior se declaran todos los miembros de Hello y todos los miembros que Hello hereda como compatibles con IDispatch.</span><span class="sxs-lookup"><span data-stu-id="ed301-152">The preceding example declares all the members of hello and all the members that hello inherits as supporting IDispatch.</span></span> <span data-ttu-id="ed301-153">En este caso, si Hello se declaró anteriormente con \[ \] \[ los miembros LCID y retval \] que devolvieron Valores HRESULT, MkTypLib quitaría cada \[ \] parámetro de LCID y el tipo de valor devuelto HRESULT, y en su lugar marcaría el tipo de valor devuelto como el del \[ \] parámetro retval.</span><span class="sxs-lookup"><span data-stu-id="ed301-153">In this case, if hello were declared earlier with \[lcid\] and \[retval\] members that returned HRESULTs, MkTypLib would remove each \[lcid\] parameter and HRESULT return type, and instead mark the return type as that of the \[retval\] parameter.</span></span>

> [!Note]  
> <span data-ttu-id="ed301-154">La herramienta Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="ed301-154">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="ed301-155">En su lugar, utilice el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="ed301-155">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="ed301-156">Las propiedades y los métodos de una interfaz dispinterface no forman parte de la VTBL de la dispinterface.</span><span class="sxs-lookup"><span data-stu-id="ed301-156">The properties and methods of a dispinterface are not part of the VTBL of the dispinterface.</span></span> <span data-ttu-id="ed301-157">Por consiguiente, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) y [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) no se pueden usar para implementar IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="ed301-157">Consequently, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) and [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) cannot be used to implement IDispatch::Invoke.</span></span> <span data-ttu-id="ed301-158">La dispinterface se utiliza cuando una aplicación necesita exponer funciones existentes que no son VTBL a través de la automatización.</span><span class="sxs-lookup"><span data-stu-id="ed301-158">The dispinterface is used when an application needs to expose existing non-VTBL functions through Automation.</span></span> <span data-ttu-id="ed301-159">Estas aplicaciones pueden implementar IDispatch:: Invoke examinando el parámetro dispidMember y llamando directamente a la función correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ed301-159">These applications can implement IDispatch::Invoke by examining the dispidMember parameter and directly calling the corresponding function.</span></span>

## <a name="examples"></a><span data-ttu-id="ed301-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ed301-160">Examples</span></span>

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="ed301-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed301-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed301-162">**bindable**</span><span class="sxs-lookup"><span data-stu-id="ed301-162">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="ed301-163">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="ed301-163">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="ed301-164">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="ed301-164">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="ed301-165">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="ed301-165">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="ed301-166">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="ed301-166">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="ed301-167">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="ed301-167">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="ed301-168">**plusvalía**</span><span class="sxs-lookup"><span data-stu-id="ed301-168">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="ed301-169">**de**</span><span class="sxs-lookup"><span data-stu-id="ed301-169">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="ed301-170">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="ed301-170">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="ed301-171">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="ed301-171">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="ed301-172">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="ed301-172">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="ed301-173">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="ed301-173">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ed301-174">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="ed301-174">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ed301-175">**opta**</span><span class="sxs-lookup"><span data-stu-id="ed301-175">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="ed301-176">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="ed301-176">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ed301-177">**nonextensible**</span><span class="sxs-lookup"><span data-stu-id="ed301-177">**nonextensible**</span></span>](nonextensible.md)
</dt> <dt>

[<span data-ttu-id="ed301-178">**propget**</span><span class="sxs-lookup"><span data-stu-id="ed301-178">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="ed301-179">**PROPPUT**</span><span class="sxs-lookup"><span data-stu-id="ed301-179">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="ed301-180">**PROPPUTREF**</span><span class="sxs-lookup"><span data-stu-id="ed301-180">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="ed301-181">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="ed301-181">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="ed301-182">**Restrict**</span><span class="sxs-lookup"><span data-stu-id="ed301-182">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="ed301-183">**string**</span><span class="sxs-lookup"><span data-stu-id="ed301-183">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="ed301-184">**uuid**</span><span class="sxs-lookup"><span data-stu-id="ed301-184">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="ed301-185">**vararg**</span><span class="sxs-lookup"><span data-stu-id="ed301-185">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="ed301-186">**Versión**</span><span class="sxs-lookup"><span data-stu-id="ed301-186">**version**</span></span>](version.md)
</dt> </dl>

 

 