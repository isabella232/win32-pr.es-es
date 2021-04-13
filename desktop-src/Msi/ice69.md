---
description: ICE69 comprueba que todas las subcadenas del formulario \[ $componentkey \] dentro de una cadena con formato no son componentes de referencias cruzadas.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278460"
---
# <a name="ice69"></a><span data-ttu-id="977c7-103">ICE69</span><span class="sxs-lookup"><span data-stu-id="977c7-103">ICE69</span></span>

<span data-ttu-id="977c7-104">ICE69 comprueba que todas las subcadenas del formulario \[ $componentkey \] dentro de una cadena [con formato](formatted.md) no son componentes de referencias cruzadas.</span><span class="sxs-lookup"><span data-stu-id="977c7-104">ICE69 checks that all substrings of the form \[$componentkey\] within a [formatted](formatted.md) string do not cross-reference components.</span></span> <span data-ttu-id="977c7-105">Una referencia entre componentes se produce cuando la \[ \] propiedad $componentkey de una cadena con formato hace referencia a un componente distinto del componente almacenado en la \_ columna componente de las tablas.</span><span class="sxs-lookup"><span data-stu-id="977c7-105">A cross-component reference occurs when the \[$componentkey\] property of a formatted string refers to a component other than the component stored in the Component\_ column of your tables.</span></span>

<span data-ttu-id="977c7-106">Los problemas con la referencia entre componentes surgen de la manera en que se evalúan las cadenas [con formato](formatted.md) .</span><span class="sxs-lookup"><span data-stu-id="977c7-106">Problems with cross-component referencing arise from the way [formatted](formatted.md) strings are evaluated.</span></span> <span data-ttu-id="977c7-107">Si el componente al que se hace referencia con la \[ \] propiedad $componentkey ya está instalado y no se cambia durante la instalación actual (por ejemplo, se vuelve a instalar, se mueve al origen, etc.), la expresión \[ $componentkey se \] evalúa como null, porque el estado de la acción del componente en \[ $componentkey \] es NULL.</span><span class="sxs-lookup"><span data-stu-id="977c7-107">If the component referenced with the \[$componentkey\] property is already installed and is not being changed during the current installation (for example, being reinstalled, moved to source, and so forth), the expression \[$componentkey\] evaluates to null, because the action state of the component in \[$componentkey\] is null.</span></span> <span data-ttu-id="977c7-108">Pueden producirse problemas similares durante las operaciones de actualización y reparación.</span><span class="sxs-lookup"><span data-stu-id="977c7-108">Similar problems can occur during upgrade and repair operations.</span></span>

## <a name="result"></a><span data-ttu-id="977c7-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="977c7-109">Result</span></span>

<span data-ttu-id="977c7-110">ICE69 devuelve un error si una \[ \] subcadena de $componentkey dentro de una cadena [con formato](formatted.md) hace referencia cruzada a un componente de otra característica.</span><span class="sxs-lookup"><span data-stu-id="977c7-110">ICE69 returns an error if a \[$componentkey\] substring within a [formatted](formatted.md) string cross-references a component in another feature.</span></span> <span data-ttu-id="977c7-111">ICE69 devuelve una advertencia si una \[ \] subcadena de $componentkey dentro de una cadena con formato hace referencia cruzada a un componente de la misma característica.</span><span class="sxs-lookup"><span data-stu-id="977c7-111">ICE69 returns a warning if a \[$componentkey\] substring within a formatted string cross-references a component in the same feature.</span></span> <span data-ttu-id="977c7-112">(La tabla [FeatureComponents](featurecomponents-table.md) se usa para determinar esta asignación.</span><span class="sxs-lookup"><span data-stu-id="977c7-112">(The [FeatureComponents](featurecomponents-table.md) table is used to determine this mapping.</span></span> <span data-ttu-id="977c7-113">Se debe asignar a la misma característica para la advertencia.</span><span class="sxs-lookup"><span data-stu-id="977c7-113">It must map to the same feature for the warning.</span></span> <span data-ttu-id="977c7-114">La referencia a los componentes de las características primarias o a los componentes que hacen referencia a las características secundarias se considera un error).</span><span class="sxs-lookup"><span data-stu-id="977c7-114">Referencing components in parent features or referencing components in child features is considered to be an error.)</span></span>

<span data-ttu-id="977c7-115">ICE69 notifica un error si la \[ \# \] subcadena FileKey de una cadena [con formato](formatted.md) hace referencia a un archivo que no se especifica en la tabla de [archivos](file-table.md) como perteneciente al mismo componente.</span><span class="sxs-lookup"><span data-stu-id="977c7-115">ICE69 reports an error if the \[\#FileKey\] substring within a [formatted](formatted.md) string references a file which is not specified in the [File](file-table.md) table as belonging to the same component.</span></span>

## <a name="example"></a><span data-ttu-id="977c7-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="977c7-116">Example</span></span>

<span data-ttu-id="977c7-117">ICE69 notifica lo siguiente para los ejemplos mostrados.</span><span class="sxs-lookup"><span data-stu-id="977c7-117">ICE69 reports the following for the examples shown.</span></span>

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

<span data-ttu-id="977c7-118">Para corregir este error, no haga referencia cruzada a los componentes.</span><span class="sxs-lookup"><span data-stu-id="977c7-118">To fix this error, do not cross-reference components.</span></span> <span data-ttu-id="977c7-119">Cambie el \[ $componentkey \] para que coincida con el componente del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="977c7-119">Change the \[$componentkey\] to match the component of the shortcut.</span></span>

<span data-ttu-id="977c7-120">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="977c7-120">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="977c7-121">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="977c7-121">Shortcut</span></span>  | <span data-ttu-id="977c7-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="977c7-122">Component\_</span></span> | <span data-ttu-id="977c7-123">Argumento</span><span class="sxs-lookup"><span data-stu-id="977c7-123">Argument</span></span>     |
|-----------|-------------|--------------|
| <span data-ttu-id="977c7-124">Prueba</span><span class="sxs-lookup"><span data-stu-id="977c7-124">Test</span></span>      | <span data-ttu-id="977c7-125">QuickTest</span><span class="sxs-lookup"><span data-stu-id="977c7-125">QuickTest</span></span>   | <span data-ttu-id="977c7-126">-v \[ $Test\]</span><span class="sxs-lookup"><span data-stu-id="977c7-126">-v \[$Test\]</span></span> |
| <span data-ttu-id="977c7-127">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="977c7-127">Shortcut2</span></span> | <span data-ttu-id="977c7-128">QuickTest</span><span class="sxs-lookup"><span data-stu-id="977c7-128">QuickTest</span></span>   | <span data-ttu-id="977c7-129">\[$Test 2\]</span><span class="sxs-lookup"><span data-stu-id="977c7-129">\[$Test2\]</span></span>   |



 

<span data-ttu-id="977c7-130">Las tablas de [extensión](extension-table.md) y de [verbo](verb-table.md) son casos especiales en los que la tabla de verbos hace referencia a una extensión que pertenece a un componente.</span><span class="sxs-lookup"><span data-stu-id="977c7-130">The [Verb](verb-table.md) and [Extension](extension-table.md) tables are special cases in that the Verb table references an extension that belongs to a component.</span></span> <span data-ttu-id="977c7-131">Sin embargo, una extensión puede pertenecer a varios componentes porque la clave principal de la tabla de extensión se compone de las columnas de extensión y componente \_ .</span><span class="sxs-lookup"><span data-stu-id="977c7-131">An Extension, however, can belong to multiple components because the primary key for the extension table is made up of the Extension and Component\_ columns.</span></span> <span data-ttu-id="977c7-132">Lógicamente, puede tener la siguiente situación.</span><span class="sxs-lookup"><span data-stu-id="977c7-132">You can logically have the following situation.</span></span>

<span data-ttu-id="977c7-133">[Tabla de verbos](verb-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="977c7-133">[Verb Table](verb-table.md) (partial)</span></span>



| <span data-ttu-id="977c7-134">Extensión</span><span class="sxs-lookup"><span data-stu-id="977c7-134">Extension</span></span> | <span data-ttu-id="977c7-135">Verbo\_</span><span class="sxs-lookup"><span data-stu-id="977c7-135">Verb\_</span></span> | <span data-ttu-id="977c7-136">Argumento</span><span class="sxs-lookup"><span data-stu-id="977c7-136">Argument</span></span>                |
|-----------|--------|-------------------------|
| <span data-ttu-id="977c7-137">TST</span><span class="sxs-lookup"><span data-stu-id="977c7-137">tst</span></span>       | <span data-ttu-id="977c7-138">abrir</span><span class="sxs-lookup"><span data-stu-id="977c7-138">open</span></span>   | <span data-ttu-id="977c7-139">-v \[ $COMP 1 \] \[ $COMP 2\]</span><span class="sxs-lookup"><span data-stu-id="977c7-139">-v \[$comp1\]\[$comp2\]</span></span> |



 

<span data-ttu-id="977c7-140">[Tabla de extensión](extension-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="977c7-140">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="977c7-141">Extensión</span><span class="sxs-lookup"><span data-stu-id="977c7-141">Extension</span></span> | <span data-ttu-id="977c7-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="977c7-142">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="977c7-143">TST</span><span class="sxs-lookup"><span data-stu-id="977c7-143">tst</span></span>       | <span data-ttu-id="977c7-144">COMP1</span><span class="sxs-lookup"><span data-stu-id="977c7-144">comp1</span></span>       |
| <span data-ttu-id="977c7-145">TST</span><span class="sxs-lookup"><span data-stu-id="977c7-145">tst</span></span>       | <span data-ttu-id="977c7-146">COMP2</span><span class="sxs-lookup"><span data-stu-id="977c7-146">comp2</span></span>       |



 

[<span data-ttu-id="977c7-147">Tabla FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="977c7-147">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="977c7-148">Característica\_</span><span class="sxs-lookup"><span data-stu-id="977c7-148">Feature\_</span></span> | <span data-ttu-id="977c7-149">Componente\_</span><span class="sxs-lookup"><span data-stu-id="977c7-149">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="977c7-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="977c7-150">Feature1</span></span>  | <span data-ttu-id="977c7-151">QuickTest</span><span class="sxs-lookup"><span data-stu-id="977c7-151">QuickTest</span></span>   |
| <span data-ttu-id="977c7-152">Feature1</span><span class="sxs-lookup"><span data-stu-id="977c7-152">Feature1</span></span>  | <span data-ttu-id="977c7-153">Prueba</span><span class="sxs-lookup"><span data-stu-id="977c7-153">Test</span></span>        |
| <span data-ttu-id="977c7-154">Característica2</span><span class="sxs-lookup"><span data-stu-id="977c7-154">Feature2</span></span>  | <span data-ttu-id="977c7-155">Test2</span><span class="sxs-lookup"><span data-stu-id="977c7-155">Test2</span></span>       |



 

<span data-ttu-id="977c7-156">En este caso, debe asegurarse de que al menos una de las \[ propiedades de $componentkey se \] evalúe como un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="977c7-156">In this case, you must ensure that at least one of the \[$componentkey\] properties evaluates to a non-null value.</span></span> <span data-ttu-id="977c7-157">Sin embargo, \[ cada \] propiedad $componentkey de la columna argument de la tabla Verb ( \[ $comp 1 \] y \[ $COMP 2 \] en el ejemplo anterior) debe hacer referencia a un componente posible incluido en la extensión asociada al verbo.</span><span class="sxs-lookup"><span data-stu-id="977c7-157">However, every \[$componentkey\] property in the Argument column of the Verb table (\[$comp1\] and \[$comp2\] in the above example) must reference a possible component included with the extension associated with the verb.</span></span> <span data-ttu-id="977c7-158">Una referencia como \[ $COMP 3 \] produciría una advertencia de ICE69.</span><span class="sxs-lookup"><span data-stu-id="977c7-158">A reference like \[$comp3\] would result in a warning from ICE69.</span></span>

<span data-ttu-id="977c7-159">La [tabla AppID](appid-table.md) tiene una situación similar a la de la tabla Verb.</span><span class="sxs-lookup"><span data-stu-id="977c7-159">The [AppId table](appid-table.md) has a similar situation to the Verb table.</span></span> <span data-ttu-id="977c7-160">Usa la [tabla de clases](class-table.md) para su referencia de componente.</span><span class="sxs-lookup"><span data-stu-id="977c7-160">It uses the [Class table](class-table.md) for its component reference.</span></span> <span data-ttu-id="977c7-161">En este caso, la tabla AppId se valida de la misma manera que la validación Verb-Extension (ahora AppId-Class).</span><span class="sxs-lookup"><span data-stu-id="977c7-161">In this case, the AppId table is validated in the same way as the Verb-Extension validation (now AppId-Class).</span></span>

<span data-ttu-id="977c7-162">La columna de argumento de la tabla de clase se valida como el [acceso directo](shortcut-table.md), el [registro](registry-table.md)y las tablas similares.</span><span class="sxs-lookup"><span data-stu-id="977c7-162">The Class table's Argument column is validated like the [Shortcut](shortcut-table.md), [Registry](registry-table.md), and similar tables.</span></span>

## <a name="table-used-during-execution-only-if-found"></a><span data-ttu-id="977c7-163">Tabla utilizada durante la ejecución (solo si se encuentra)</span><span class="sxs-lookup"><span data-stu-id="977c7-163">Table used during execution (only if found)</span></span>

[<span data-ttu-id="977c7-164">IniFile</span><span class="sxs-lookup"><span data-stu-id="977c7-164">IniFile</span></span>](inifile-table.md)

[<span data-ttu-id="977c7-165">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="977c7-165">RemoveIniFile</span></span>](removeinifile-table.md)

[<span data-ttu-id="977c7-166">Registro</span><span class="sxs-lookup"><span data-stu-id="977c7-166">Registry</span></span>](registry-table.md)

[<span data-ttu-id="977c7-167">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="977c7-167">RemoveRegistry</span></span>](removeregistry-table.md)

[<span data-ttu-id="977c7-168">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="977c7-168">ServiceControl</span></span>](servicecontrol-table.md)

[<span data-ttu-id="977c7-169">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="977c7-169">ServiceInstall</span></span>](serviceinstall-table.md)

[<span data-ttu-id="977c7-170">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="977c7-170">Shortcut</span></span>](shortcut-table.md)

[<span data-ttu-id="977c7-171">Verbo</span><span class="sxs-lookup"><span data-stu-id="977c7-171">Verb</span></span>](verb-table.md)

[<span data-ttu-id="977c7-172">Extensión</span><span class="sxs-lookup"><span data-stu-id="977c7-172">Extension</span></span>](extension-table.md)

[<span data-ttu-id="977c7-173">Clase</span><span class="sxs-lookup"><span data-stu-id="977c7-173">Class</span></span>](class-table.md)

[<span data-ttu-id="977c7-174">AppId</span><span class="sxs-lookup"><span data-stu-id="977c7-174">AppId</span></span>](appid-table.md)

[<span data-ttu-id="977c7-175">Entorno</span><span class="sxs-lookup"><span data-stu-id="977c7-175">Environment</span></span>](environment-table.md)

## <a name="related-topics"></a><span data-ttu-id="977c7-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="977c7-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="977c7-177">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="977c7-177">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



