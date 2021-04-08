---
title: atributo HelpString
description: El atributo \ HelpString \ especifica una cadena de caracteres que se utiliza para describir el elemento al que se aplica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- atributo HelpString MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995144"
---
# <a name="helpstring-attribute"></a><span data-ttu-id="9ee5e-104">atributo HelpString</span><span class="sxs-lookup"><span data-stu-id="9ee5e-104">helpstring attribute</span></span>

<span data-ttu-id="9ee5e-105">El atributo **\[ HelpString \]** especifica una cadena de caracteres que se utiliza para describir el elemento al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="9ee5e-105">The **\[helpstring\]** attribute specifies a character string that is used to describe the element to which it applies.</span></span> <span data-ttu-id="9ee5e-106">Puede aplicar el atributo **\[ HelpString \]** a las instrucciones Library, importlib, interface, dispinterface, Module o coclass, definiciones de tipo, propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="9ee5e-106">You can apply the **\[helpstring\]** attribute to library, importlib, interface, dispinterface, module, or coclass statements, typedefs, properties, and methods.</span></span>

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a><span data-ttu-id="9ee5e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ee5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ee5e-108">*Help-Text-String*</span><span class="sxs-lookup"><span data-stu-id="9ee5e-108">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee5e-109">Cadena de caracteres terminada en cero que contiene el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="9ee5e-109">A zero-terminated string of characters containing help text.</span></span>

</dd> <dt>

<span data-ttu-id="9ee5e-110">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9ee5e-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee5e-111">Cero o más instrucciones de atributo de MIDL.</span><span class="sxs-lookup"><span data-stu-id="9ee5e-111">Zero or more MIDL attribute statements.</span></span>

</dd> <dt>

<span data-ttu-id="9ee5e-112">*Element*</span><span class="sxs-lookup"><span data-stu-id="9ee5e-112">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee5e-113">Una de las siguientes directivas: [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**CoClass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5e-113">One of the following directives: [**library**](library.md), **\[**[**importlib**](importlib.md)**\]**, [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee5e-114">*nombre del elemento*</span><span class="sxs-lookup"><span data-stu-id="9ee5e-114">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee5e-115">El nombre que otros componentes de software pueden usar para delimitar el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="9ee5e-115">The name that other software components can use to delineate the current element</span></span>

</dd> <dt>

<span data-ttu-id="9ee5e-116">*definición*</span><span class="sxs-lookup"><span data-stu-id="9ee5e-116">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee5e-117">Especifica las instrucciones que componen la definición del elemento.</span><span class="sxs-lookup"><span data-stu-id="9ee5e-117">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="9ee5e-118">*IDL-Statement*</span><span class="sxs-lookup"><span data-stu-id="9ee5e-118">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee5e-119">Una instrucción de definición de la interfaz MIDL como [**propget**](propget.md) o [**PROPPUT**](propput.md).</span><span class="sxs-lookup"><span data-stu-id="9ee5e-119">A MIDL interface definition statement such as [**propget**](propget.md) or [**propput**](propput.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ee5e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ee5e-120">Remarks</span></span>

<span data-ttu-id="9ee5e-121">Use las funciones [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) en las interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) y [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) para recuperar la cadena de ayuda.</span><span class="sxs-lookup"><span data-stu-id="9ee5e-121">Use the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="9ee5e-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9ee5e-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a><span data-ttu-id="9ee5e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ee5e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee5e-124">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="9ee5e-124">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="9ee5e-125">**importlib**</span><span class="sxs-lookup"><span data-stu-id="9ee5e-125">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="9ee5e-126">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="9ee5e-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="9ee5e-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="9ee5e-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="9ee5e-128">**destina**</span><span class="sxs-lookup"><span data-stu-id="9ee5e-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="9ee5e-129">**coclase**</span><span class="sxs-lookup"><span data-stu-id="9ee5e-129">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="9ee5e-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="9ee5e-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="9ee5e-131">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="9ee5e-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9ee5e-132">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="9ee5e-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9ee5e-133">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="9ee5e-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 