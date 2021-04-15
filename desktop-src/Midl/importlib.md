---
title: importlib (atributo)
description: La Directiva \ importlib \ hace que los tipos que ya se han compilado en otra biblioteca de tipos estén disponibles para la biblioteca de tipos que se va a crear.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib (atributo) MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487546"
---
# <a name="importlib-attribute"></a><span data-ttu-id="834d7-104">importlib (atributo)</span><span class="sxs-lookup"><span data-stu-id="834d7-104">importlib attribute</span></span>

<span data-ttu-id="834d7-105">La directiva **\[ importlib \]** hace que los tipos que ya se han compilado en otra biblioteca de tipos estén disponibles para la biblioteca de tipos que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="834d7-105">The **\[importlib\]** directive makes types that have already been compiled into another type library available to the type library being created.</span></span>

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a><span data-ttu-id="834d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="834d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834d7-107">*Biblioteca: atributos*</span><span class="sxs-lookup"><span data-stu-id="834d7-107">*library-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="834d7-108">Cero o más atributos que se aplicarán a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="834d7-108">Zero or more attributes that will be applied to the library.</span></span>

</dd> <dt>

<span data-ttu-id="834d7-109">*nombre de biblioteca*</span><span class="sxs-lookup"><span data-stu-id="834d7-109">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="834d7-110">El identificador que los componentes de software usarán para denotar esta [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="834d7-110">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="834d7-111">*archivo a importar*</span><span class="sxs-lookup"><span data-stu-id="834d7-111">*file-to-import*</span></span> 
</dt> <dd>

<span data-ttu-id="834d7-112">Nombre y ubicación del archivo importado en tiempo de compilación de MIDL.</span><span class="sxs-lookup"><span data-stu-id="834d7-112">The name and location of the imported file at MIDL compile-time.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="834d7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="834d7-113">Remarks</span></span>

<span data-ttu-id="834d7-114">Todas las directivas **\[ importlib \]** deben preceder a las demás descripciones de tipos de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="834d7-114">All **\[importlib\]** directives must precede the other type descriptions in the library.</span></span> <span data-ttu-id="834d7-115">Tenga en cuenta que la biblioteca importada, así como la biblioteca generada, deben distribuirse con la aplicación para que esté disponible en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="834d7-115">Note that the imported library, as well as the generated library, must be distributed with the application so that it is available at run time.</span></span>

<span data-ttu-id="834d7-116">En la mayoría de los casos, debe usar la Directiva de **\[** [**importación**](import.md) **\]** de MIDL para hacer referencia a definiciones de otro. Archivo IDL en su. Archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="834d7-116">In most cases you should use the MIDL **\[**[**import**](import.md)**\]** directive to reference definitions from another .IDL file in your .IDL file.</span></span> <span data-ttu-id="834d7-117">Este método proporciona a la biblioteca de tipos toda la información del archivo original, mientras que **\[ importlib \]** solo aporta el contenido de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="834d7-117">This method provides your type library with all the information from the original file, whereas **\[importlib\]** only brings in the contents of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="834d7-118">La directiva **\[ importlib \]** hace que cualquier tipo definido en la biblioteca importada sea accesible desde dentro de la biblioteca que se está compilando.</span><span class="sxs-lookup"><span data-stu-id="834d7-118">The **\[importlib\]** directive makes any type defined in the imported library accessible from within the library being compiled.</span></span> <span data-ttu-id="834d7-119">Para evitar la ambigüedad cuando hay referencias duplicadas, se recomienda calificar cada una de ellas con el nombre de biblioteca adecuado, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="834d7-119">To avoid ambiguity when there are duplicate references, we recommend that you qualify each such reference with the appropriate library name, as follows:</span></span>

 

``` syntax
library_name.type
```

<span data-ttu-id="834d7-120">En ausencia de tal calificación, MIDL resuelve la ambigüedad de la referencia duplicada como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="834d7-120">In the absence of such qualification, MIDL resolves duplicate reference ambiguity as follows:</span></span>

-   <span data-ttu-id="834d7-121">A partir de la versión 3,1, MIDL usa la primera referencia que encuentra.</span><span class="sxs-lookup"><span data-stu-id="834d7-121">Effective with version 3.1, MIDL uses the first reference it finds.</span></span>
-   <span data-ttu-id="834d7-122">La versión 3,0 de MIDL, la primera versión de MIDL que podría generar bibliotecas de tipos, utiliza la última referencia encontrada.</span><span class="sxs-lookup"><span data-stu-id="834d7-122">Version 3.0 of MIDL, the first version of MIDL that could generate type libraries, uses the last reference it found.</span></span>

## <a name="examples"></a><span data-ttu-id="834d7-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="834d7-123">Examples</span></span>

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a><span data-ttu-id="834d7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="834d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834d7-125">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="834d7-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="834d7-126">**importar**</span><span class="sxs-lookup"><span data-stu-id="834d7-126">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="834d7-127">Importación de archivos de encabezado del sistema</span><span class="sxs-lookup"><span data-stu-id="834d7-127">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="834d7-128">Importar archivos y bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="834d7-128">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="834d7-129">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="834d7-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="834d7-130">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="834d7-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="834d7-131">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="834d7-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 