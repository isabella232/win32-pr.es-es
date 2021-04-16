---
title: atributo helpstringcontext
description: El atributo \ helpstringcontext \ especifica un identificador de contexto de ayuda de 32 bits en el archivo de ayuda. Puede aplicar el atributo \ helpstringcontext \ a la biblioteca, interfaz, dispinterface, módulo, coclase, instrucciones TypeDef, propiedades, parámetros y métodos.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- helpstringcontext (atributo) MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651330"
---
# <a name="helpstringcontext-attribute"></a><span data-ttu-id="7a30d-105">atributo helpstringcontext</span><span class="sxs-lookup"><span data-stu-id="7a30d-105">helpstringcontext attribute</span></span>

<span data-ttu-id="7a30d-106">El atributo **\[ helpstringcontext \]** especifica un identificador de contexto de ayuda de 32 bits en el archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="7a30d-106">The **\[helpstringcontext\]** attribute specifies a 32-bit Help context identifier in the Help file.</span></span> <span data-ttu-id="7a30d-107">Puede aplicar el atributo **\[ helpstringcontext \]** a la [**biblioteca**](library.md), [**interfaz**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**coclase**](coclass.md), instrucciones [**typedef**](typedef.md) , propiedades, parámetros y métodos.</span><span class="sxs-lookup"><span data-stu-id="7a30d-107">You can apply the **\[helpstringcontext\]** attribute to [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef**](typedef.md) statements, properties, parameters and methods.</span></span>

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a><span data-ttu-id="7a30d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a30d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a30d-109">*ContextId*</span><span class="sxs-lookup"><span data-stu-id="7a30d-109">*contextid*</span></span> 
</dt> <dd>

<span data-ttu-id="7a30d-110">Entero único que identifica el texto de ayuda asociado a la instrucción MIDL actual.</span><span class="sxs-lookup"><span data-stu-id="7a30d-110">A unique integer that identifies the help text associated with the current MIDL statement.</span></span>

</dd> <dt>

<span data-ttu-id="7a30d-111">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7a30d-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7a30d-112">Cero o más atributos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7a30d-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7a30d-113">*IDL-Statement*</span><span class="sxs-lookup"><span data-stu-id="7a30d-113">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="7a30d-114">La instrucción MIDL a la que se aplicará el atributo **\[ helpstringcontext \]** .</span><span class="sxs-lookup"><span data-stu-id="7a30d-114">The MIDL statement to which the **\[helpstringcontext\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a30d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a30d-115">Remarks</span></span>

<span data-ttu-id="7a30d-116">Use las funciones **GetDocumentation2** en las interfaces **ITypeLib2** e **ITypeInfo2** para recuperar la cadena de ayuda.</span><span class="sxs-lookup"><span data-stu-id="7a30d-116">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="7a30d-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7a30d-117">Examples</span></span>

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




