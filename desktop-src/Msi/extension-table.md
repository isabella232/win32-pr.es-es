---
description: La tabla de extensión contiene información sobre los servidores de extensión de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del registro.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabla de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652529"
---
# <a name="extension-table"></a><span data-ttu-id="e1ac0-104">Tabla de extensión</span><span class="sxs-lookup"><span data-stu-id="e1ac0-104">Extension Table</span></span>

<span data-ttu-id="e1ac0-105">La tabla de extensión contiene información sobre los servidores de extensión de nombre de archivo que se deben generar como parte del anuncio del producto.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-105">The Extension table contains information about file name extension servers that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="e1ac0-106">Cada fila genera un conjunto de claves y valores del registro.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="e1ac0-107">La tabla de extensión contiene las columnas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-107">The Extension table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="e1ac0-108">Columna</span><span class="sxs-lookup"><span data-stu-id="e1ac0-108">Column</span></span>      | <span data-ttu-id="e1ac0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1ac0-109">Type</span></span>                         | <span data-ttu-id="e1ac0-110">Clave</span><span class="sxs-lookup"><span data-stu-id="e1ac0-110">Key</span></span> | <span data-ttu-id="e1ac0-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="e1ac0-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e1ac0-112">Extensión</span><span class="sxs-lookup"><span data-stu-id="e1ac0-112">Extension</span></span>   | [<span data-ttu-id="e1ac0-113">Texto</span><span class="sxs-lookup"><span data-stu-id="e1ac0-113">Text</span></span>](text.md)             | <span data-ttu-id="e1ac0-114">Y</span><span class="sxs-lookup"><span data-stu-id="e1ac0-114">Y</span></span>   | <span data-ttu-id="e1ac0-115">N</span><span class="sxs-lookup"><span data-stu-id="e1ac0-115">N</span></span>        |
| <span data-ttu-id="e1ac0-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-116">Component\_</span></span> | [<span data-ttu-id="e1ac0-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="e1ac0-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="e1ac0-118">Y</span><span class="sxs-lookup"><span data-stu-id="e1ac0-118">Y</span></span>   | <span data-ttu-id="e1ac0-119">N</span><span class="sxs-lookup"><span data-stu-id="e1ac0-119">N</span></span>        |
| <span data-ttu-id="e1ac0-120">Programa\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-120">ProgId\_</span></span>    | [<span data-ttu-id="e1ac0-121">Texto</span><span class="sxs-lookup"><span data-stu-id="e1ac0-121">Text</span></span>](text.md)             | <span data-ttu-id="e1ac0-122">N</span><span class="sxs-lookup"><span data-stu-id="e1ac0-122">N</span></span>   | <span data-ttu-id="e1ac0-123">Y</span><span class="sxs-lookup"><span data-stu-id="e1ac0-123">Y</span></span>        |
| <span data-ttu-id="e1ac0-124">Mine\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-124">MIME\_</span></span>      | [<span data-ttu-id="e1ac0-125">Texto</span><span class="sxs-lookup"><span data-stu-id="e1ac0-125">Text</span></span>](text.md)             | <span data-ttu-id="e1ac0-126">N</span><span class="sxs-lookup"><span data-stu-id="e1ac0-126">N</span></span>   | <span data-ttu-id="e1ac0-127">Y</span><span class="sxs-lookup"><span data-stu-id="e1ac0-127">Y</span></span>        |
| <span data-ttu-id="e1ac0-128">Característica\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-128">Feature\_</span></span>   | [<span data-ttu-id="e1ac0-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="e1ac0-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="e1ac0-130">N</span><span class="sxs-lookup"><span data-stu-id="e1ac0-130">N</span></span>   | <span data-ttu-id="e1ac0-131">N</span><span class="sxs-lookup"><span data-stu-id="e1ac0-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e1ac0-132">Columnas</span><span class="sxs-lookup"><span data-stu-id="e1ac0-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e1ac0-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span><span class="sxs-lookup"><span data-stu-id="e1ac0-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span></span>
</dt> <dd>

<span data-ttu-id="e1ac0-134">La extensión asociada a la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-134">The extension associated with the table row.</span></span> <span data-ttu-id="e1ac0-135">La extensión puede tener una longitud de hasta 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-135">The extension can be up to 255 characters long.</span></span> <span data-ttu-id="e1ac0-136">Escriba la extensión en este campo sin el punto anterior.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-136">Enter the extension in this field without the preceding period.</span></span>

</dd> <dt>

<span data-ttu-id="e1ac0-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e1ac0-138">Una clave externa a la primera columna de la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ac0-138">An external key to the first column of the [Component](component-table.md) table.</span></span> <span data-ttu-id="e1ac0-139">Esta columna hace referencia al componente que controla la instalación de la extensión.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-139">This column references the component that controls the installation of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="e1ac0-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>Programa\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span></span>
</dt> <dd>

<span data-ttu-id="e1ac0-141">IDENTIFICADOR de programa asociado a esta extensión.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-141">The Program ID associated with this extension.</span></span> <span data-ttu-id="e1ac0-142">Se trata de una clave externa en la tabla [ProgID](progid-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ac0-142">This is a foreign key into the [ProgId](progid-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="e1ac0-143"><span id="MIME_"></span><span id="mime_"></span>Mine\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span></span>
</dt> <dd>

<span data-ttu-id="e1ac0-144">El tipo de contenido que se va a escribir para la columna de extensión.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-144">The Content Type that is to be written for the Extension column.</span></span>

<span data-ttu-id="e1ac0-145">Una clave externa a la primera columna de la tabla [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ac0-145">An external key to the first column of the [MIME](mime-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="e1ac0-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="e1ac0-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="e1ac0-147">Una clave externa en la primera columna de la tabla de [características](feature-table.md) que especifica la característica que proporciona el servidor de extensión.</span><span class="sxs-lookup"><span data-stu-id="e1ac0-147">An external key into the first column of the [Feature](feature-table.md) table specifying the feature that provides the extension server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1ac0-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1ac0-148">Remarks</span></span>

<span data-ttu-id="e1ac0-149">Se hace referencia a la tabla de extensión cuando se ejecuta la acción [RegisterExtensionInfo](registerextensioninfo-action.md) o la acción [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ac0-149">The Extension table is referred to when the [RegisterExtensionInfo](registerextensioninfo-action.md) action or the [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) action is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="e1ac0-150">Validación</span><span class="sxs-lookup"><span data-stu-id="e1ac0-150">Validation</span></span>

<dl>

[<span data-ttu-id="e1ac0-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="e1ac0-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e1ac0-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="e1ac0-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e1ac0-153">ICE15</span><span class="sxs-lookup"><span data-stu-id="e1ac0-153">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="e1ac0-154">ICE19</span><span class="sxs-lookup"><span data-stu-id="e1ac0-154">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="e1ac0-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="e1ac0-155">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e1ac0-156">ICE41</span><span class="sxs-lookup"><span data-stu-id="e1ac0-156">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="e1ac0-157">ICE69</span><span class="sxs-lookup"><span data-stu-id="e1ac0-157">ICE69</span></span>](ice69.md)  
</dl>

 

 



