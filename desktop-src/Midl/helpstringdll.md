---
title: atributo helpstringdll
description: El atributo \ helpstringdll \ establece el nombre del archivo DLL que se va a usar para realizar una búsqueda de cadena de documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- helpstringdll (atributo) MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995154"
---
# <a name="helpstringdll-attribute"></a><span data-ttu-id="94fca-104">atributo helpstringdll</span><span class="sxs-lookup"><span data-stu-id="94fca-104">helpstringdll attribute</span></span>

<span data-ttu-id="94fca-105">El atributo **\[ helpstringdll \]** establece el nombre del archivo DLL que se va a usar para realizar una búsqueda de cadena de documento.</span><span class="sxs-lookup"><span data-stu-id="94fca-105">The **\[helpstringdll\]** attribute sets the name of the DLL to use to perform a document string lookup.</span></span>

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a><span data-ttu-id="94fca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94fca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94fca-107">*Help-Text-String*</span><span class="sxs-lookup"><span data-stu-id="94fca-107">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="94fca-108">Una cadena de caracteres terminada en cero que especifica el nombre de archivo completo de un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="94fca-108">A zero-terminated string of characters specifying the fully qualified file name of a DLL.</span></span>

</dd> <dt>

<span data-ttu-id="94fca-109">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="94fca-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="94fca-110">Otros atributos que se aplican a la instrucción Library en conjunto.</span><span class="sxs-lookup"><span data-stu-id="94fca-110">Other attributes that apply to the library statement as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="94fca-111">*nombre de biblioteca*</span><span class="sxs-lookup"><span data-stu-id="94fca-111">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="94fca-112">El identificador que los componentes de software usarán para denotar esta [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="94fca-112">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="94fca-113">*Library-Definition-instrucciones*</span><span class="sxs-lookup"><span data-stu-id="94fca-113">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="94fca-114">Una o más instrucciones MIDL que definen la interfaz de la [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="94fca-114">One or more MIDL statement which define the interface of the [**library**](library.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94fca-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94fca-115">Remarks</span></span>

<span data-ttu-id="94fca-116">Utilice el atributo **\[ helpstringdll \]** en una instrucción Library para especificar, como una cadena de caracteres, el nombre de archivo completo de una biblioteca de vínculos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="94fca-116">Use the **\[helpstringdll\]** attribute on a library statement to specify, as a character string, the fully qualified file name of a dynamic link library.</span></span> <span data-ttu-id="94fca-117">Esto permite que un usuario vea una descripción del archivo DLL con el visor de objetos.</span><span class="sxs-lookup"><span data-stu-id="94fca-117">This allows a user to view a description of the DLL with the object viewer.</span></span>

<span data-ttu-id="94fca-118">Use las funciones **GetDocumentation2** en las interfaces **ITypeLib2** e **ITypeInfo2** para recuperar la cadena de ayuda.</span><span class="sxs-lookup"><span data-stu-id="94fca-118">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="94fca-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="94fca-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fca-120">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="94fca-120">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="94fca-121">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="94fca-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="94fca-122">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="94fca-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="94fca-123">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="94fca-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 