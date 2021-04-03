---
title: helpfile (atributo)
description: El atributo \ HelpFile \ establece el nombre del archivo de ayuda de una biblioteca de tipos. Todos los tipos de una biblioteca comparten el mismo archivo de ayuda.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- atributo HelpFile (MIDL)
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790023"
---
# <a name="helpfile-attribute"></a><span data-ttu-id="5bde5-105">helpfile (atributo)</span><span class="sxs-lookup"><span data-stu-id="5bde5-105">helpfile attribute</span></span>

<span data-ttu-id="5bde5-106">El atributo **\[ HelpFile \]** establece el nombre del archivo de ayuda de una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="5bde5-106">The **\[helpfile\]** attribute sets the name of the Help file for a type library.</span></span> <span data-ttu-id="5bde5-107">Todos los tipos de una biblioteca comparten el mismo archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="5bde5-107">All types in a library share the same Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a><span data-ttu-id="5bde5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bde5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bde5-109">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="5bde5-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="5bde5-110">Especifica un número de identificación único universal para la [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="5bde5-110">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bde5-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="5bde5-111">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="5bde5-112">Especifica el nombre del archivo que contiene el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="5bde5-112">Specifies the name of the file containing the help text.</span></span>

</dd> <dt>

<span data-ttu-id="5bde5-113">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5bde5-113">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5bde5-114">Especifica cero o más atributos que el compilador MIDL aplicará a la [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="5bde5-114">Specifies zero or more attributes that the MIDL compiler will apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bde5-115">*instrucciones de biblioteca*</span><span class="sxs-lookup"><span data-stu-id="5bde5-115">*library statements*</span></span> 
</dt> <dd>

<span data-ttu-id="5bde5-116">Especifica una o más instrucciones MIDL que definen la interfaz de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5bde5-116">Specifies one or more MIDL statements that define the library interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bde5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bde5-117">Remarks</span></span>

<span data-ttu-id="5bde5-118">Use las funciones **GetDocumentation** en las interfaces **ITypeLib** y **ITypeInfo** para recuperar el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="5bde5-118">Use the **GetDocumentation** functions in the **ITypeLib** and **ITypeInfo** interfaces to retrieve the file name.</span></span>

## <a name="examples"></a><span data-ttu-id="5bde5-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5bde5-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="5bde5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bde5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bde5-121">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="5bde5-121">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="5bde5-122">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="5bde5-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5bde5-123">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="5bde5-123">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5bde5-124">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="5bde5-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 