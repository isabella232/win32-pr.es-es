---
description: La tabla Verb contiene información de verbo de comando asociada a las extensiones de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del registro.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Tabla de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678585"
---
# <a name="verb-table"></a><span data-ttu-id="90542-104">Tabla de verbos</span><span class="sxs-lookup"><span data-stu-id="90542-104">Verb Table</span></span>

<span data-ttu-id="90542-105">La tabla Verb contiene información de verbo de comando asociada a las extensiones de nombre de archivo que se deben generar como parte del anuncio del producto.</span><span class="sxs-lookup"><span data-stu-id="90542-105">The Verb table contains command-verb information associated with file name extensions that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="90542-106">Cada fila genera un conjunto de claves y valores del registro.</span><span class="sxs-lookup"><span data-stu-id="90542-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="90542-107">La tabla de verbos tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="90542-107">The Verb table has the following columns.</span></span>



| <span data-ttu-id="90542-108">Columna</span><span class="sxs-lookup"><span data-stu-id="90542-108">Column</span></span>      | <span data-ttu-id="90542-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="90542-109">Type</span></span>                       | <span data-ttu-id="90542-110">Clave</span><span class="sxs-lookup"><span data-stu-id="90542-110">Key</span></span> | <span data-ttu-id="90542-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="90542-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="90542-112">Extensión\_</span><span class="sxs-lookup"><span data-stu-id="90542-112">Extension\_</span></span> | [<span data-ttu-id="90542-113">Texto</span><span class="sxs-lookup"><span data-stu-id="90542-113">Text</span></span>](text.md)           | <span data-ttu-id="90542-114">Y</span><span class="sxs-lookup"><span data-stu-id="90542-114">Y</span></span>   | <span data-ttu-id="90542-115">N</span><span class="sxs-lookup"><span data-stu-id="90542-115">N</span></span>        |
| <span data-ttu-id="90542-116">Verbo</span><span class="sxs-lookup"><span data-stu-id="90542-116">Verb</span></span>        | [<span data-ttu-id="90542-117">Texto</span><span class="sxs-lookup"><span data-stu-id="90542-117">Text</span></span>](text.md)           | <span data-ttu-id="90542-118">Y</span><span class="sxs-lookup"><span data-stu-id="90542-118">Y</span></span>   | <span data-ttu-id="90542-119">N</span><span class="sxs-lookup"><span data-stu-id="90542-119">N</span></span>        |
| <span data-ttu-id="90542-120">Secuencia</span><span class="sxs-lookup"><span data-stu-id="90542-120">Sequence</span></span>    | [<span data-ttu-id="90542-121">Entero</span><span class="sxs-lookup"><span data-stu-id="90542-121">Integer</span></span>](integer.md)     | <span data-ttu-id="90542-122">N</span><span class="sxs-lookup"><span data-stu-id="90542-122">N</span></span>   | <span data-ttu-id="90542-123">Y</span><span class="sxs-lookup"><span data-stu-id="90542-123">Y</span></span>        |
| <span data-ttu-id="90542-124">Get-Help</span><span class="sxs-lookup"><span data-stu-id="90542-124">Command</span></span>     | [<span data-ttu-id="90542-125">Formatea</span><span class="sxs-lookup"><span data-stu-id="90542-125">Formatted</span></span>](formatted.md) | <span data-ttu-id="90542-126">N</span><span class="sxs-lookup"><span data-stu-id="90542-126">N</span></span>   | <span data-ttu-id="90542-127">Y</span><span class="sxs-lookup"><span data-stu-id="90542-127">Y</span></span>        |
| <span data-ttu-id="90542-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="90542-128">Argument</span></span>    | [<span data-ttu-id="90542-129">Formatea</span><span class="sxs-lookup"><span data-stu-id="90542-129">Formatted</span></span>](formatted.md) | <span data-ttu-id="90542-130">N</span><span class="sxs-lookup"><span data-stu-id="90542-130">N</span></span>   | <span data-ttu-id="90542-131">Y</span><span class="sxs-lookup"><span data-stu-id="90542-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="90542-132">Columnas</span><span class="sxs-lookup"><span data-stu-id="90542-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="90542-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span><span class="sxs-lookup"><span data-stu-id="90542-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="90542-134">La extensión asociada a la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="90542-134">The extension associated with the table row.</span></span> <span data-ttu-id="90542-135">Esta columna es una clave externa de la primera columna de la [tabla de extensión](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="90542-135">This column is an external key to the first column of the [Extension table](extension-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="90542-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Solicitud</span><span class="sxs-lookup"><span data-stu-id="90542-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span>
</dt> <dd>

<span data-ttu-id="90542-137">El verbo para el comando.</span><span class="sxs-lookup"><span data-stu-id="90542-137">The verb for the command.</span></span>

</dd> <dt>

<span data-ttu-id="90542-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="90542-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="90542-139">Secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="90542-139">The sequence of the commands.</span></span> <span data-ttu-id="90542-140">Solo los verbos para los que la columna de secuencia no es NULL se utilizan para preparar una lista ordenada para el valor predeterminado de la clave de Shell.</span><span class="sxs-lookup"><span data-stu-id="90542-140">Only verbs for which the Sequence column is non-Null are used to prepare an ordered list for the default value of the shell key.</span></span> <span data-ttu-id="90542-141">El verbo con el valor más bajo de esta columna se convierte en el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="90542-141">The Verb with the lowest value in this column becomes the default verb.</span></span>

</dd> <dt>

<span data-ttu-id="90542-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span><span class="sxs-lookup"><span data-stu-id="90542-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="90542-143">Texto traducible que se muestra en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="90542-143">The localizable text displayed on the context menu.</span></span>

</dd> <dt>

<span data-ttu-id="90542-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="90542-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="90542-145">Valor de los argumentos de comando.</span><span class="sxs-lookup"><span data-stu-id="90542-145">Value for the command arguments.</span></span>

<span data-ttu-id="90542-146">Tenga en cuenta que la resolución de propiedades en el campo argumento es limitada.</span><span class="sxs-lookup"><span data-stu-id="90542-146">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="90542-147">Una propiedad con formato \[  \] de propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando el componente propietario del verbo está instalado.</span><span class="sxs-lookup"><span data-stu-id="90542-147">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component owning the verb is installed.</span></span> <span data-ttu-id="90542-148">Por ejemplo, para que el argumento " \[ \#MyDoc.doc\] " resuelva el valor correcto, el mismo proceso debe instalar el archivo MyDoc.doc y el componente que posee el verbo.</span><span class="sxs-lookup"><span data-stu-id="90542-148">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90542-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90542-149">Remarks</span></span>

<span data-ttu-id="90542-150">Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterExtensionInfo](registerextensioninfo-action.md) o la [acción UnregisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="90542-150">This table is referred to when the [RegisterExtensionInfo action](registerextensioninfo-action.md) or the [UnregisterExtensionInfo action](unregisterextensioninfo-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="90542-151">Validación</span><span class="sxs-lookup"><span data-stu-id="90542-151">Validation</span></span>

<dl>

[<span data-ttu-id="90542-152">ICE03</span><span class="sxs-lookup"><span data-stu-id="90542-152">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="90542-153">ICE06</span><span class="sxs-lookup"><span data-stu-id="90542-153">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="90542-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="90542-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="90542-155">ICE46</span><span class="sxs-lookup"><span data-stu-id="90542-155">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="90542-156">ICE69</span><span class="sxs-lookup"><span data-stu-id="90542-156">ICE69</span></span>](ice69.md)  
</dl>

 

 



