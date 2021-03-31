---
title: defaultcollelem (atributo)
description: El atributo \ defaultcollelem \ marca una propiedad como una función de descriptor de acceso para un elemento de la colección predeterminada.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- defaultcollelem (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077698"
---
# <a name="defaultcollelem-attribute"></a><span data-ttu-id="4ac09-104">defaultcollelem (atributo)</span><span class="sxs-lookup"><span data-stu-id="4ac09-104">defaultcollelem attribute</span></span>

<span data-ttu-id="4ac09-105">El atributo **\[ defaultcollelem \]** marca una propiedad como una función de descriptor de acceso para un elemento de la colección predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4ac09-105">The **\[defaultcollelem\]** attribute flags a property as an accessor function for an element of the default collection.</span></span>

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="4ac09-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ac09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ac09-107">*Property-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4ac09-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4ac09-108">Otros atributos que se aplican a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4ac09-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="4ac09-109">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="4ac09-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4ac09-110">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="4ac09-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="4ac09-111">*nombre de propiedad*</span><span class="sxs-lookup"><span data-stu-id="4ac09-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4ac09-112">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4ac09-112">The name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="4ac09-113">*prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="4ac09-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4ac09-114">Lista de cero o más parámetros asociados a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4ac09-114">A list of zero or more parameters associated with the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ac09-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ac09-115">Remarks</span></span>

<span data-ttu-id="4ac09-116">El atributo **\[ defaultcollelem \]** se usa para la optimización del código de Visual BasicÂ®.</span><span class="sxs-lookup"><span data-stu-id="4ac09-116">The **\[defaultcollelem\]** attribute is used for Visual BasicÂ® code optimization.</span></span> <span data-ttu-id="4ac09-117">Si un miembro de una interfaz o dispinterface se marca como una función de descriptor de acceso, la llamada irá directamente a ese miembro.</span><span class="sxs-lookup"><span data-stu-id="4ac09-117">If a member of an interface or dispinterface is flagged as an accessor function, then the call will go directly to that member.</span></span>

<span data-ttu-id="4ac09-118">El uso de **\[ defaultcollelem \]** debe ser coherente para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="4ac09-118">Use of **\[defaultcollelem\]** must be consistent for a property.</span></span> <span data-ttu-id="4ac09-119">Por ejemplo, si usa el atributo en una propiedad *Get* , también debe estar presente en una propiedad *Let* .</span><span class="sxs-lookup"><span data-stu-id="4ac09-119">For example, if you use the attribute on a *Get* property, it must also be present on a *Let* property.</span></span>

### <a name="typeflags-representation"></a><span data-ttu-id="4ac09-120">Representación TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="4ac09-120">Typeflags Representation</span></span>

<span data-ttu-id="4ac09-121">La presencia de FUNCFLAG \_ FDEFAULTCOLLELEM o VARFLAG \_ FDEFAULTCOLLELEM.</span><span class="sxs-lookup"><span data-stu-id="4ac09-121">The presence of FUNCFLAG\_FDEFAULTCOLLELEM or VARFLAG\_FDEFAULTCOLLELEM.</span></span>

## <a name="examples"></a><span data-ttu-id="4ac09-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4ac09-122">Examples</span></span>

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a><span data-ttu-id="4ac09-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ac09-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac09-124">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="4ac09-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4ac09-125">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="4ac09-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4ac09-126">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="4ac09-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 