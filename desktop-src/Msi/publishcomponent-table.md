---
description: La tabla PublishComponent asocia los componentes enumerados en la tabla componente con una cadena de texto de calificador y un GUID de ID. de categoría.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabla PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677774"
---
# <a name="publishcomponent-table"></a><span data-ttu-id="e0ef1-103">Tabla PublishComponent</span><span class="sxs-lookup"><span data-stu-id="e0ef1-103">PublishComponent Table</span></span>

<span data-ttu-id="e0ef1-104">La tabla PublishComponent asocia los componentes enumerados en la [tabla componente](component-table.md) con una cadena de texto de calificador y un GUID de ID. de categoría.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-104">The PublishComponent table associates components listed in the [Component table](component-table.md) with a qualifier text-string and a category ID GUID.</span></span> <span data-ttu-id="e0ef1-105">Los componentes con funcionalidad paralela que se han agrupado de esta manera se denominan componentes calificados.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-105">Components with parallel functionality that have been grouped together in this way are referred to as qualified components.</span></span> <span data-ttu-id="e0ef1-106">Vea [componentes calificados](qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-106">See [Qualified Components](qualified-components.md).</span></span> <span data-ttu-id="e0ef1-107">Esto proporciona al instalador un método para direccionamiento indirecto de un solo nivel al hacer referencia a los componentes.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-107">This provides the installer with a method for single-level indirection when referring to components.</span></span> <span data-ttu-id="e0ef1-108">Vea [uso de componentes calificados](using-qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-108">See [Using Qualified Components](using-qualified-components.md).</span></span>

<span data-ttu-id="e0ef1-109">La tabla PublishComponent tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-109">The PublishComponent table has the following columns.</span></span>



| <span data-ttu-id="e0ef1-110">Columna</span><span class="sxs-lookup"><span data-stu-id="e0ef1-110">Column</span></span>      | <span data-ttu-id="e0ef1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0ef1-111">Type</span></span>                         | <span data-ttu-id="e0ef1-112">Clave</span><span class="sxs-lookup"><span data-stu-id="e0ef1-112">Key</span></span> | <span data-ttu-id="e0ef1-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="e0ef1-113">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e0ef1-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e0ef1-114">ComponentId</span></span> | [<span data-ttu-id="e0ef1-115">GUID</span><span class="sxs-lookup"><span data-stu-id="e0ef1-115">GUID</span></span>](guid.md)             | <span data-ttu-id="e0ef1-116">Y</span><span class="sxs-lookup"><span data-stu-id="e0ef1-116">Y</span></span>   | <span data-ttu-id="e0ef1-117">N</span><span class="sxs-lookup"><span data-stu-id="e0ef1-117">N</span></span>        |
| <span data-ttu-id="e0ef1-118">Qualifier</span><span class="sxs-lookup"><span data-stu-id="e0ef1-118">Qualifier</span></span>   | [<span data-ttu-id="e0ef1-119">Texto</span><span class="sxs-lookup"><span data-stu-id="e0ef1-119">Text</span></span>](text.md)             | <span data-ttu-id="e0ef1-120">Y</span><span class="sxs-lookup"><span data-stu-id="e0ef1-120">Y</span></span>   | <span data-ttu-id="e0ef1-121">N</span><span class="sxs-lookup"><span data-stu-id="e0ef1-121">N</span></span>        |
| <span data-ttu-id="e0ef1-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="e0ef1-122">Component\_</span></span> | [<span data-ttu-id="e0ef1-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="e0ef1-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="e0ef1-124">Y</span><span class="sxs-lookup"><span data-stu-id="e0ef1-124">Y</span></span>   | <span data-ttu-id="e0ef1-125">N</span><span class="sxs-lookup"><span data-stu-id="e0ef1-125">N</span></span>        |
| <span data-ttu-id="e0ef1-126">AppData</span><span class="sxs-lookup"><span data-stu-id="e0ef1-126">AppData</span></span>     | [<span data-ttu-id="e0ef1-127">Texto</span><span class="sxs-lookup"><span data-stu-id="e0ef1-127">Text</span></span>](text.md)             | <span data-ttu-id="e0ef1-128">N</span><span class="sxs-lookup"><span data-stu-id="e0ef1-128">N</span></span>   | <span data-ttu-id="e0ef1-129">Y</span><span class="sxs-lookup"><span data-stu-id="e0ef1-129">Y</span></span>        |
| <span data-ttu-id="e0ef1-130">Característica\_</span><span class="sxs-lookup"><span data-stu-id="e0ef1-130">Feature\_</span></span>   | [<span data-ttu-id="e0ef1-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="e0ef1-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="e0ef1-132">N</span><span class="sxs-lookup"><span data-stu-id="e0ef1-132">N</span></span>   | <span data-ttu-id="e0ef1-133">N</span><span class="sxs-lookup"><span data-stu-id="e0ef1-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e0ef1-134">Columnas</span><span class="sxs-lookup"><span data-stu-id="e0ef1-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e0ef1-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="e0ef1-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="e0ef1-136">[GUID](guid.md) de cadena que representa la categoría de componentes que se agrupan.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-136">A string [GUID](guid.md) that represents the category of components being grouped together.</span></span> <span data-ttu-id="e0ef1-137">Tenga en cuenta que el título de esta columna es engañoso.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-137">Note that this column's title is misleading.</span></span> <span data-ttu-id="e0ef1-138">Este es el GUID de la categoría de componentes completos y no es el mismo GUID que aparece en la columna ComponentId de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-138">This is the GUID for the category of qualified components and is not the same GUID appearing in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="e0ef1-139">Aquí hace referencia a un servidor que proporciona la funcionalidad de un componente a clientes externos en lugar de al propio componente.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-139">Here it refers to a server that provides the functionality of a component to external clients rather than the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Calificador</span><span class="sxs-lookup"><span data-stu-id="e0ef1-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifier</span></span>
</dt> <dd>

<span data-ttu-id="e0ef1-141">Cadena de texto que califica el valor de la columna ComponentId.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-141">A text string that qualifies the value in the ComponentId column.</span></span> <span data-ttu-id="e0ef1-142">Un calificador se usa para distinguir varias formas del mismo componente, como un componente que se implementa en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-142">A qualifier is used to distinguish multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span> <span data-ttu-id="e0ef1-143">Estas son las cadenas de texto del calificador devueltas por [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-143">These are the qualifier text-strings returned by [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="e0ef1-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e0ef1-145">Clave externa en la columna uno de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-145">External key into column one of the [Component table](component-table.md).</span></span> <span data-ttu-id="e0ef1-146">Este identificador hace referencia al registro del componente completo en la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-146">This identifier refers to the qualified component's record in the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span><span class="sxs-lookup"><span data-stu-id="e0ef1-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span></span>
</dt> <dd>

<span data-ttu-id="e0ef1-148">Texto traducible opcional que describe el componente calificado de este registro.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-148">An optional localizable text describing the qualified component of this record.</span></span> <span data-ttu-id="e0ef1-149">Normalmente, la aplicación analiza la cadena y se puede mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-149">The string is commonly parsed by the application and can be displayed to the user.</span></span> <span data-ttu-id="e0ef1-150">Debe describir el componente calificado.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-150">It should describe the qualified component.</span></span> <span data-ttu-id="e0ef1-151">Se puede recuperar con [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-151">This can be retrieved with [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="e0ef1-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="e0ef1-153">Clave externa en la columna uno de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-153">External key into column one of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="e0ef1-154">Esta es la característica que usa este componente calificado.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-154">This is the feature using this qualified component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0ef1-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0ef1-155">Remarks</span></span>

<span data-ttu-id="e0ef1-156">Se hace referencia a esta tabla cuando se ejecuta la acción [PublishComponents](publishcomponents-action.md) o la [acción UnpublishComponents](unpublishcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e0ef1-156">This table is referred to when the [PublishComponents action](publishcomponents-action.md) or the [UnpublishComponents action](unpublishcomponents-action.md) is executed.</span></span>

<span data-ttu-id="e0ef1-157">Tenga en cuenta que el nombre de esta tabla es engañoso.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-157">Note that the name of this table is misleading.</span></span> <span data-ttu-id="e0ef1-158">Esta tabla no es necesaria para crear anuncios.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-158">This table is not required in order to author advertisement.</span></span> <span data-ttu-id="e0ef1-159">Vea la columna atributos de la tabla [componente](component-table.md) y la [tabla de características](feature-table.md) para obtener información sobre cómo establecer el estado de instalación de los componentes en anunciar.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-159">See the Attributes column of the [Component table](component-table.md) and [Feature table](feature-table.md) for information on how to set the installation state of components to advertise.</span></span>

## <a name="validation"></a><span data-ttu-id="e0ef1-160">Validación</span><span class="sxs-lookup"><span data-stu-id="e0ef1-160">Validation</span></span>

<dl>

[<span data-ttu-id="e0ef1-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="e0ef1-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e0ef1-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="e0ef1-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e0ef1-163">ICE19</span><span class="sxs-lookup"><span data-stu-id="e0ef1-163">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="e0ef1-164">ICE22</span><span class="sxs-lookup"><span data-stu-id="e0ef1-164">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="e0ef1-165">ICE32</span><span class="sxs-lookup"><span data-stu-id="e0ef1-165">ICE32</span></span>](ice32.md)  
</dl>

 

 



