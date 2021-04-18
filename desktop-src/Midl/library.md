---
title: atributo de biblioteca
description: La instrucción Library contiene toda la información que el compilador MIDL utiliza para generar una biblioteca de tipos.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- MIDL (atributo de biblioteca)
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665821"
---
# <a name="library-attribute"></a><span data-ttu-id="f0923-104">atributo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0923-104">library attribute</span></span>

<span data-ttu-id="f0923-105">La instrucción **Library** contiene toda la información que el compilador MIDL utiliza para generar una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="f0923-105">The **library** statement contains all the information that the MIDL compiler uses to generate a type library.</span></span>

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="f0923-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0923-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0923-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="f0923-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="f0923-108">Especifica un número de identificación único universal para la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f0923-108">Specifies a universally unique identification number for the library.</span></span>

</dd> <dt>

<span data-ttu-id="f0923-109">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f0923-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f0923-110">Especifica atributos adicionales que se aplican a toda la instrucción **Library** .</span><span class="sxs-lookup"><span data-stu-id="f0923-110">Specifies additional attributes that apply to the entire **library** statement.</span></span> <span data-ttu-id="f0923-111">Entre los atributos permitidos se incluyen **\[** [**control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md), **\]** **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** y **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f0923-111">Allowable attributes include **\[**[**control**](control.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**lcid**](lcid.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f0923-112">*nombre de biblioteca*</span><span class="sxs-lookup"><span data-stu-id="f0923-112">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f0923-113">Nombre por el que los componentes de software hacen referencia a la **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="f0923-113">The name by which software components refer to the **library**.</span></span>

</dd> <dt>

<span data-ttu-id="f0923-114">*Library-Definition-instrucciones*</span><span class="sxs-lookup"><span data-stu-id="f0923-114">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="f0923-115">Una o más instrucciones MIDL que definen el contenido de la **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="f0923-115">One or more MIDL statements which define the contents of the **library**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0923-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0923-116">Remarks</span></span>

<span data-ttu-id="f0923-117">Las instrucciones dentro del bloque de biblioteca pueden utilizar elementos que se declaran dentro o fuera del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f0923-117">Statements inside the library block can use elements that are declared inside or outside of the library block.</span></span> <span data-ttu-id="f0923-118">Las instrucciones de biblioteca pueden utilizar esos elementos como tipos base, heredar de esos elementos o simplemente hacer referencia a ellos en una línea, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f0923-118">Library statements can use those elements as base types, inheriting from those elements, or by simply referencing them on a line, as follows:</span></span>

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

<span data-ttu-id="f0923-119">El compilador MIDL creará una biblioteca de tipos que incluye las definiciones de todos los elementos dentro del bloque de biblioteca, así como las definiciones de los elementos definidos fuera y a los que se haga referencia desde dentro del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f0923-119">The MIDL compiler will create a type library that includes definitions for every element inside the library block, plus definitions for any elements defined outside and referenced from within the library block.</span></span>

<span data-ttu-id="f0923-120">Para obtener información sobre la generación de una biblioteca de tipos y de código auxiliar y encabezados de proxy a partir de un único archivo IDL, vea [generar un archivo dll de proxy y una biblioteca de tipos desde un solo archivo IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span><span class="sxs-lookup"><span data-stu-id="f0923-120">For information on generating both a type library and proxy stubs and headers from a single IDL file see [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f0923-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f0923-121">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a><span data-ttu-id="f0923-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0923-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0923-123">Contenido de una biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f0923-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="f0923-124">**control**</span><span class="sxs-lookup"><span data-stu-id="f0923-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="f0923-125">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="f0923-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f0923-126">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="f0923-126">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="f0923-127">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="f0923-127">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="f0923-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="f0923-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="f0923-129">**plusvalía**</span><span class="sxs-lookup"><span data-stu-id="f0923-129">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="f0923-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="f0923-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="f0923-131">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="f0923-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f0923-132">**Restrict**</span><span class="sxs-lookup"><span data-stu-id="f0923-132">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="f0923-133">**Versión**</span><span class="sxs-lookup"><span data-stu-id="f0923-133">**version**</span></span>](version.md)
</dt> </dl>

 

 