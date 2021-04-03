---
title: LCID (atributo)
description: El atributo \ LCID \ especifica un identificador de configuración regional y habilita la compatibilidad con el compilador MIDL específico de la configuración regional.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- LCID (atributo) MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789970"
---
# <a name="lcid-attribute"></a><span data-ttu-id="e8e56-104">LCID (atributo)</span><span class="sxs-lookup"><span data-stu-id="e8e56-104">lcid attribute</span></span>

<span data-ttu-id="e8e56-105">El atributo **\[ LCID \]** especifica un identificador de configuración regional y habilita la compatibilidad con el compilador de MIDL específico de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="e8e56-105">The **\[lcid\]** attribute specifies a locale identifier and enables locale-specific MIDL compiler support.</span></span>

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="e8e56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8e56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e56-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="e8e56-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-108">Especifica un número de identificación único universal para la [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="e8e56-108">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8e56-109">*LCID*</span><span class="sxs-lookup"><span data-stu-id="e8e56-109">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-110">Especifica el identificador de configuración regional de 32 bits usado en la compatibilidad con el idioma nacional de Windows.</span><span class="sxs-lookup"><span data-stu-id="e8e56-110">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="e8e56-111">Normalmente, el identificador de configuración regional se proporciona en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e8e56-111">Typically the locale identifier is given in hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="e8e56-112">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e8e56-112">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-113">Cero o más atributos que se van a aplicar a la [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="e8e56-113">Zero or more attributes to apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8e56-114">*nombre de biblioteca*</span><span class="sxs-lookup"><span data-stu-id="e8e56-114">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-115">Nombre por el que los componentes de software hacen referencia a la [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="e8e56-115">The name by which software components refer to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8e56-116">*Library-Definition-instrucciones*</span><span class="sxs-lookup"><span data-stu-id="e8e56-116">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-117">Una o más instrucciones MIDL que definen el contenido de la [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="e8e56-117">One or more MIDL statements which define the contents of the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8e56-118">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="e8e56-118">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-119">Especifica el nombre de la función en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="e8e56-119">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="e8e56-120">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e8e56-120">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-121">Cero o más atributos de MIDL que se aplicarán al parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="e8e56-121">Zero or more MIDL attributes that will be applied to the function parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e8e56-122">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="e8e56-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e56-123">Especifica el nombre del parámetro en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="e8e56-123">Specifies the name of the parameter in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8e56-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8e56-124">Remarks</span></span>

<span data-ttu-id="e8e56-125">La sintaxis de **\[ \] LCID** tiene dos formas diferentes; el efecto del atributo depende de la sintaxis que se utilice, ya sea de la sintaxis de la instrucción de la [**biblioteca**](library.md) o de la sintaxis del parámetro.</span><span class="sxs-lookup"><span data-stu-id="e8e56-125">The **\[lcid\]** syntax has two different forms; the effect of the attribute depends on which syntax you use — either the [**library**](library.md) statement syntax or the parameter syntax.</span></span>

<span data-ttu-id="e8e56-126">Cuando se aplica a la instrucción [**Library**](library.md) , junto con un argumento localeID, como se muestra en el primer ejemplo, el atributo **\[ LCID \]** identifica la configuración regional de una biblioteca de tipos o de un argumento de función y permite usar caracteres internacionales dentro del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e8e56-126">When applied to the [**library**](library.md) statement, along with a localeID argument, as shown in the first example, the **\[lcid\]** attribute identifies the locale for a type library or for a function argument and lets you use international characters inside the library block.</span></span>

<span data-ttu-id="e8e56-127">A partir de la versión 3.01.75 del compilador de MIDL, el identificador de configuración regional proporcionado por este atributo no solo decora la biblioteca de tipos resultante, sino que realmente cambia el comportamiento del compilador.</span><span class="sxs-lookup"><span data-stu-id="e8e56-127">Effective with version 3.01.75 of the MIDL compiler, the locale identifier supplied by this attribute not only decorates the resulting type library, but actually changes the behavior of the compiler.</span></span> <span data-ttu-id="e8e56-128">Dentro de una instrucción de [**biblioteca**](library.md) , desde el punto donde se usa el atributo **\[ LCID \]** , MIDL aceptará la entrada localizada según la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="e8e56-128">Within a [**library**](library.md) statement, from the point where the **\[lcid\]** attribute is used, MIDL will accept input localized according to the specified locale.</span></span> <span data-ttu-id="e8e56-129">En concreto, hay disponible compatibilidad total con idiomas asiáticos como japonés, Chino y Coreano (compatibilidad completa con DBCS).</span><span class="sxs-lookup"><span data-stu-id="e8e56-129">In particular, full support for Asian languages such as Japanese, Chinese and Korean (full DBCS support) is available.</span></span> <span data-ttu-id="e8e56-130">Las características admitidas por la localización son: comentarios, cadenas, helpstrings e identificadores.</span><span class="sxs-lookup"><span data-stu-id="e8e56-130">Features supported by the localization are: comments, strings, helpstrings and identifiers.</span></span>

<span data-ttu-id="e8e56-131">Utilice el modificador de compilador [**/LCID**](-lcid.md) para que esta compatibilidad de localización esté disponible en todo el archivo de entrada, incluidos el nombre de archivo y la ruta de acceso del directorio, en lugar de simplemente dentro del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e8e56-131">Use the [**/lcid**](-lcid.md) compiler switch to have this localization support available to the entire input file, including file name and directory path, rather than just inside the library block.</span></span>

<span data-ttu-id="e8e56-132">Cuando se aplica a un parámetro, el atributo **\[ LCID \]** permite pasar un identificador de configuración regional a una función, tal y como se muestra en el segundo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e8e56-132">When applied to a parameter, the **\[lcid\]** attribute lets you pass a locale identifier to a function, as shown in the second example.</span></span> <span data-ttu-id="e8e56-133">Las restricciones siguientes se aplican a los parámetros de **\[ LCID \]** :</span><span class="sxs-lookup"><span data-stu-id="e8e56-133">The following restrictions apply to **\[lcid\]** parameters:</span></span>

-   <span data-ttu-id="e8e56-134">Una función puede tener como máximo un parámetro **\[ LCID \]** .</span><span class="sxs-lookup"><span data-stu-id="e8e56-134">A function can have at most one **\[lcid\]** parameter.</span></span>
-   <span data-ttu-id="e8e56-135">El tipo de datos del parámetro debe ser [**largo**](long.md).</span><span class="sxs-lookup"><span data-stu-id="e8e56-135">The data type of the parameter must be [**long**](long.md).</span></span>
-   <span data-ttu-id="e8e56-136">La dirección del parámetro debe ser solo **\[** [**en**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e8e56-136">The direction of the parameter must be **\[**[**in**](in.md)**\]** only.</span></span>
-   <span data-ttu-id="e8e56-137">El parámetro **\[ LCID \]** debe seguir a cualquier otro parámetro, excepto un **\[** parámetro [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e8e56-137">The **\[lcid\]** parameter must follow any other parameters, except a **\[**[**retval**](retval.md)**\]** parameter.</span></span>
-   <span data-ttu-id="e8e56-138">No se puede aplicar el atributo **\[ LCID \]** a un parámetro [**dispinterface**](dispinterface.md) o [**CoClass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="e8e56-138">You cannot apply the **\[lcid\]** attribute to a [**dispinterface**](dispinterface.md) or [**coclass**](coclass.md) parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="e8e56-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8e56-139">Examples</span></span>

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a><span data-ttu-id="e8e56-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e56-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e56-141">**coclase**</span><span class="sxs-lookup"><span data-stu-id="e8e56-141">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="e8e56-142">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="e8e56-142">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="e8e56-143">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="e8e56-143">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e8e56-144">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="e8e56-144">**/lcid**</span></span>](-lcid.md)
</dt> <dt>

[<span data-ttu-id="e8e56-145">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="e8e56-145">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="e8e56-146">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="e8e56-146">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e8e56-147">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="e8e56-147">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e8e56-148">**retval**</span><span class="sxs-lookup"><span data-stu-id="e8e56-148">**retval**</span></span>](retval.md)
</dt> </dl>

 

 