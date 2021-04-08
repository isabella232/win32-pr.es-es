---
title: helpcontext (atributo)
description: El atributo \ HelpContext \ especifica un identificador de contexto que permite al usuario ver información sobre este elemento en el archivo de ayuda.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- atributo ContextoDeAyuda (MIDL)
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995157"
---
# <a name="helpcontext-attribute"></a><span data-ttu-id="cce75-104">helpcontext (atributo)</span><span class="sxs-lookup"><span data-stu-id="cce75-104">helpcontext attribute</span></span>

<span data-ttu-id="cce75-105">El \[  \] atributo HelpContext especifica un identificador de contexto que permite al usuario ver información sobre este elemento en el archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="cce75-105">The \[**helpcontext**\] attribute specifies a context identifier that lets the user view information about this element in the Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a><span data-ttu-id="cce75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cce75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce75-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="cce75-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="cce75-108">Especifica un número de identificación único universal para la [**biblioteca**](library.md), \[ [**importlib**](importlib.md) \] , [**interfaz**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**typedef**](typedef.md), **métodos**, **\[ propiedades \]** o [**coclase**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="cce75-108">Specifies a universally unique identification number for the [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[property\]**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce75-109">*HelpContext: valor*</span><span class="sxs-lookup"><span data-stu-id="cce75-109">*helpcontext-value*</span></span> 
</dt> <dd>

<span data-ttu-id="cce75-110">Entero único que identifica el texto de ayuda asociado al elemento MIDL actual.</span><span class="sxs-lookup"><span data-stu-id="cce75-110">A unique integer that identifies the help text associated with the current MIDL element.</span></span>

</dd> <dt>

<span data-ttu-id="cce75-111">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="cce75-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="cce75-112">Especifica una lista de uno o más atributos que se aplican al elemento MIDL en conjunto.</span><span class="sxs-lookup"><span data-stu-id="cce75-112">Specifies a list of one or more attributes that apply to the MIDL element as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="cce75-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="cce75-113">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="cce75-114">Una de las siguientes directivas: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**CoClass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="cce75-114">One of the following directives: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce75-115">*nombre del elemento*</span><span class="sxs-lookup"><span data-stu-id="cce75-115">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cce75-116">El nombre que otros componentes de software pueden usar para delimitar el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="cce75-116">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="cce75-117">*Figura*</span><span class="sxs-lookup"><span data-stu-id="cce75-117">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="cce75-118">Especifica las instrucciones que componen la definición del elemento.</span><span class="sxs-lookup"><span data-stu-id="cce75-118">Specifies statements that make up the element definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cce75-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cce75-119">Remarks</span></span>

<span data-ttu-id="cce75-120">El \[  \] atributo HelpContext se puede aplicar a los elementos siguientes: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**CoClass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="cce75-120">The \[**helpcontext**\] attribute can be applied to the following elements: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

<span data-ttu-id="cce75-121">*HelpContext-Value* es un identificador de contexto de 32 bits dentro del archivo de ayuda que se puede recuperar con las [**funciones GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) en las interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) y [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .</span><span class="sxs-lookup"><span data-stu-id="cce75-121">The *helpcontext-value* is a 32-bit context identifier within the Help file that can be retrieved with the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="cce75-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cce75-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="cce75-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cce75-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce75-124">**coclase**</span><span class="sxs-lookup"><span data-stu-id="cce75-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="cce75-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="cce75-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="cce75-126">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="cce75-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="cce75-127">**importlib**</span><span class="sxs-lookup"><span data-stu-id="cce75-127">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="cce75-128">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="cce75-128">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="cce75-129">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="cce75-129">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="cce75-130">**destina**</span><span class="sxs-lookup"><span data-stu-id="cce75-130">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="cce75-131">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="cce75-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="cce75-132">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="cce75-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="cce75-133">**typedef**</span><span class="sxs-lookup"><span data-stu-id="cce75-133">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 