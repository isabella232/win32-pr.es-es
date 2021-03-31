---
description: Los componentes calificados son un método de direccionamiento indirecto y se pueden usar para agrupar componentes con funcionalidad paralela en categorías.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Uso de componentes calificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154366"
---
# <a name="using-qualified-components"></a><span data-ttu-id="3b129-103">Uso de componentes calificados</span><span class="sxs-lookup"><span data-stu-id="3b129-103">Using Qualified Components</span></span>

<span data-ttu-id="3b129-104">Los componentes calificados son un método de direccionamiento indirecto y se pueden usar para agrupar componentes con funcionalidad paralela en categorías.</span><span class="sxs-lookup"><span data-stu-id="3b129-104">Qualified components are a method of indirection and can be used to group components with parallel functionality into categories.</span></span>

<span data-ttu-id="3b129-105">Para devolver la ruta de acceso completa e instalar un [componente completo](qualified-components.md), llame a [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span><span class="sxs-lookup"><span data-stu-id="3b129-105">To return the full path and install a [qualified component](qualified-components.md), call [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span></span>

<span data-ttu-id="3b129-106">Para enumerar todos los calificadores de componente cualificados y las cadenas descriptivas, llame a [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="3b129-106">To enumerate all of the qualified component qualifiers and descriptive strings, call [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

<span data-ttu-id="3b129-107">**Para agrupar los componentes en una categoría de componente calificado**</span><span class="sxs-lookup"><span data-stu-id="3b129-107">**To group components together into a qualified-component category**</span></span>

1.  <span data-ttu-id="3b129-108">Debe haber un registro en la [tabla de componentes](component-table.md) para cada componente incluido en la nueva categoría de componentes calificados.</span><span class="sxs-lookup"><span data-stu-id="3b129-108">There must be a record in the [Component table](component-table.md) for each component that is included in the new category of qualified components.</span></span> <span data-ttu-id="3b129-109">Cree los campos en la tabla de componentes de la misma forma que para los componentes normales.</span><span class="sxs-lookup"><span data-stu-id="3b129-109">Author the fields in the Component table the same as for ordinary components.</span></span> <span data-ttu-id="3b129-110">Tenga en cuenta que cada componente calificado debe tener un GUID de identificador de componente único escrito en la columna ComponentId de la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="3b129-110">Note that each qualified component must have a unique component ID GUID entered in the ComponentId column of the Component table.</span></span>
2.  <span data-ttu-id="3b129-111">Generar una cadena de texto de calificador para cada componente calificado.</span><span class="sxs-lookup"><span data-stu-id="3b129-111">Generate a qualifier text string for each qualified component.</span></span> <span data-ttu-id="3b129-112">El calificador debe ser una cadena de texto única que se pueda generar fácilmente al buscar un componente calificado.</span><span class="sxs-lookup"><span data-stu-id="3b129-112">The qualifier must be unique text string that can be easily generated when searching for a qualified component.</span></span> <span data-ttu-id="3b129-113">Por ejemplo, si los componentes de la categoría se califican por idioma, el identificador numérico de la configuración regional (LCID) es una cadena de calificador razonable.</span><span class="sxs-lookup"><span data-stu-id="3b129-113">For example, if the components in the category are being qualified by language, the numeric locale identifier (LCID) is a reasonable qualifier string.</span></span>
3.  <span data-ttu-id="3b129-114">Agregue un registro en la [tabla PublishComponent](publishcomponent-table.md) para cada componente calificado.</span><span class="sxs-lookup"><span data-stu-id="3b129-114">Add a record in the [PublishComponent table](publishcomponent-table.md) for each qualified component.</span></span> <span data-ttu-id="3b129-115">Especifique los identificadores de componente completo de la columna componente de la tabla componente en la \_ columna componente de la tabla PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="3b129-115">Enter the qualified-component identifiers from the Component column of the Component table into the Component\_ column of the PublishComponent table.</span></span> <span data-ttu-id="3b129-116">Escriba las cadenas de calificador de cada componente calificado en la columna calificador.</span><span class="sxs-lookup"><span data-stu-id="3b129-116">Enter the qualifier strings for each qualified component into the Qualifier column.</span></span> <span data-ttu-id="3b129-117">Escriba una cadena traducida que se mostrará al usuario y que describa el componente calificado en la columna AppData opcional.</span><span class="sxs-lookup"><span data-stu-id="3b129-117">Enter a localized string to be displayed to the user and describing the qualified component into the optional AppData column.</span></span> <span data-ttu-id="3b129-118">Se debe colocar una cadena explicativa en el campo AppData, como "Diccionario francés", en lugar de solo el LCID numérico.</span><span class="sxs-lookup"><span data-stu-id="3b129-118">An explanatory string should be put in the AppData field, such as "French Dictionary," rather than just the numeric LCID.</span></span> <span data-ttu-id="3b129-119">Escriba el nombre de la característica que usa este componente en la columna de la característica \_ .</span><span class="sxs-lookup"><span data-stu-id="3b129-119">Enter the name of the feature that uses this component into the Feature\_ column.</span></span> <span data-ttu-id="3b129-120">El identificador de característica de este campo también debe aparecer en la columna característica de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b129-120">The feature identifier in this field must also be listed in the Feature column of the [Feature table](feature-table.md).</span></span>
4.  <span data-ttu-id="3b129-121">Genere un GUID de categoría para esta categoría de componentes calificados.</span><span class="sxs-lookup"><span data-stu-id="3b129-121">Generate a category GUID for this category of qualified components.</span></span> <span data-ttu-id="3b129-122">Debe ser un [GUID](guid.md)válido.</span><span class="sxs-lookup"><span data-stu-id="3b129-122">This must be a valid [GUID](guid.md).</span></span> <span data-ttu-id="3b129-123">Si utiliza una utilidad como GUIDGEN para generar el GUID, asegúrese de que contiene solo letras mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="3b129-123">If you use a utility such as GUIDGEN to generate the GUID be sure that it contains only uppercase letters.</span></span> <span data-ttu-id="3b129-124">Para cada componente calificado en esta categoría, escriba el GUID de la categoría en el campo ComponentId de la [tabla PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b129-124">For every qualified component in this category, enter the category GUID into the ComponentId field of the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="3b129-125">En el ejemplo siguiente se muestra cómo se crea la categoría de "plantillas de FAX" de los componentes calificados en las tablas componente, característica y PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="3b129-125">The following example illustrates how the "FAX Templates" category of qualified components are authored into the Component, Feature, and PublishComponent tables.</span></span>

[<span data-ttu-id="3b129-126">Tabla PublishComponent</span><span class="sxs-lookup"><span data-stu-id="3b129-126">PublishComponent table</span></span>](publishcomponent-table.md)



| <span data-ttu-id="3b129-127">ComponentId</span><span class="sxs-lookup"><span data-stu-id="3b129-127">ComponentId</span></span>                  | <span data-ttu-id="3b129-128">Qualifier</span><span class="sxs-lookup"><span data-stu-id="3b129-128">Qualifier</span></span> | <span data-ttu-id="3b129-129">AppData</span><span class="sxs-lookup"><span data-stu-id="3b129-129">AppData</span></span>             | <span data-ttu-id="3b129-130">Característica\_</span><span class="sxs-lookup"><span data-stu-id="3b129-130">Feature\_</span></span>   | <span data-ttu-id="3b129-131">Componente\_</span><span class="sxs-lookup"><span data-stu-id="3b129-131">Component\_</span></span>    |
|------------------------------|-----------|---------------------|-------------|----------------|
| <span data-ttu-id="3b129-132">{GUID de categoría de plantilla de FAX}</span><span class="sxs-lookup"><span data-stu-id="3b129-132">{FAX Template Category GUID}</span></span> | <span data-ttu-id="3b129-133">3082</span><span class="sxs-lookup"><span data-stu-id="3b129-133">1033</span></span>      | <span data-ttu-id="3b129-134">Plantilla de Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="3b129-134">US English template</span></span> | <span data-ttu-id="3b129-135">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-135">FAXTemplate</span></span> | <span data-ttu-id="3b129-136">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="3b129-136">FAXTemplateENU</span></span> |
|                              | <span data-ttu-id="3b129-137">1041</span><span class="sxs-lookup"><span data-stu-id="3b129-137">1041</span></span>      | <span data-ttu-id="3b129-138">Plantilla en Japonés</span><span class="sxs-lookup"><span data-stu-id="3b129-138">Japanese template</span></span>   | <span data-ttu-id="3b129-139">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-139">FAXTemplate</span></span> | <span data-ttu-id="3b129-140">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="3b129-140">FAXTemplateJPN</span></span> |
|                              | <span data-ttu-id="3b129-141">1054</span><span class="sxs-lookup"><span data-stu-id="3b129-141">1054</span></span>      | <span data-ttu-id="3b129-142">Plantilla tailandesa</span><span class="sxs-lookup"><span data-stu-id="3b129-142">Thai template</span></span>       | <span data-ttu-id="3b129-143">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-143">FAXTemplate</span></span> | <span data-ttu-id="3b129-144">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="3b129-144">FAXTemplateTHA</span></span> |
|                              | <span data-ttu-id="3b129-145">1031</span><span class="sxs-lookup"><span data-stu-id="3b129-145">1031</span></span>      | <span data-ttu-id="3b129-146">Plantilla alemana</span><span class="sxs-lookup"><span data-stu-id="3b129-146">German template</span></span>     | <span data-ttu-id="3b129-147">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-147">FAXTemplate</span></span> | <span data-ttu-id="3b129-148">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="3b129-148">FAXTemplateDEU</span></span> |



 

<span data-ttu-id="3b129-149">[Tabla de componentes](component-table.md) (tabla parcial)</span><span class="sxs-lookup"><span data-stu-id="3b129-149">[Component table](component-table.md) (partial table)</span></span>



| <span data-ttu-id="3b129-150">Componente</span><span class="sxs-lookup"><span data-stu-id="3b129-150">Component</span></span>      | <span data-ttu-id="3b129-151">ComponentId</span><span class="sxs-lookup"><span data-stu-id="3b129-151">ComponentId</span></span>                                  |
|----------------|----------------------------------------------|
| <span data-ttu-id="3b129-152">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="3b129-152">FAXTemplateENU</span></span> | <span data-ttu-id="3b129-153">{*Plantilla de fax (Inglés de EE. UU.) GUID del componente*}</span><span class="sxs-lookup"><span data-stu-id="3b129-153">{*FAX Template (US English) component GUID*}</span></span> |
| <span data-ttu-id="3b129-154">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="3b129-154">FAXTemplateJPN</span></span> | <span data-ttu-id="3b129-155">{*GUID del componente de plantilla de fax (japonés)*}</span><span class="sxs-lookup"><span data-stu-id="3b129-155">{*FAX Template (Japanese) component GUID*}</span></span>   |
| <span data-ttu-id="3b129-156">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="3b129-156">FAXTemplateTHA</span></span> | <span data-ttu-id="3b129-157">{*GUID del componente de plantilla de fax (tailandés)*}</span><span class="sxs-lookup"><span data-stu-id="3b129-157">{*FAX Template (Thai) component GUID*}</span></span>       |
| <span data-ttu-id="3b129-158">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="3b129-158">FAXTemplateDEU</span></span> | <span data-ttu-id="3b129-159">{*GUID del componente de plantilla de fax (alemán)*}</span><span class="sxs-lookup"><span data-stu-id="3b129-159">{*FAX Template (German) component GUID*}</span></span>     |



 

<span data-ttu-id="3b129-160">[Tabla de características](feature-table.md) (tabla parcial)</span><span class="sxs-lookup"><span data-stu-id="3b129-160">[Feature table](feature-table.md) (partial table)</span></span>



| <span data-ttu-id="3b129-161">Característica</span><span class="sxs-lookup"><span data-stu-id="3b129-161">Feature</span></span>     |
|-------------|
| <span data-ttu-id="3b129-162">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-162">FAXTemplate</span></span> |
| <span data-ttu-id="3b129-163">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-163">FAXTemplate</span></span> |
| <span data-ttu-id="3b129-164">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-164">FAXTemplate</span></span> |
| <span data-ttu-id="3b129-165">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="3b129-165">FAXTemplate</span></span> |



 

 

 



