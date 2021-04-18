---
description: ': Valida la tabla de actualización de una base de datos Windows Installer.'
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ':'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652862"
---
# <a name="ice61"></a><span data-ttu-id="1bbbc-103">:</span><span class="sxs-lookup"><span data-stu-id="1bbbc-103">ICE61</span></span>

<span data-ttu-id="1bbbc-104">: Comprueba la tabla de actualización para asegurarse de que se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="1bbbc-104">ICE61 checks the upgrade table to ensure that the following conditions are true:</span></span>

-   <span data-ttu-id="1bbbc-105">Todas las propiedades ActionProperty no se han creado previamente en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-105">All ActionProperty properties are not pre-authored in the Property table.</span></span>
-   <span data-ttu-id="1bbbc-106">Todas las propiedades de ActionProperty son propiedades públicas.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-106">All ActionProperty properties are Public Properties.</span></span>
-   <span data-ttu-id="1bbbc-107">Todas las propiedades de ActionProperty se incluyen en la propiedad [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="1bbbc-107">All ActionProperty properties are included in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>
-   <span data-ttu-id="1bbbc-108">Todas las propiedades de ActionProperty son únicas para cada registro de la tabla de actualización.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-108">All ActionProperty properties are unique to each record in the Upgrade table.</span></span>
-   <span data-ttu-id="1bbbc-109">Todos los valores de VersionMax no son menores que los valores de VersionMin correspondientes.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-109">All VersionMax values are not less than the corresponding VersionMin values.</span></span>
-   <span data-ttu-id="1bbbc-110">Los valores VersionMin y VersionMax son versiones de producto válidas.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-110">VersionMin and VersionMax values are valid product versions.</span></span> <span data-ttu-id="1bbbc-111">Vea la propiedad [**ProductVersion**](productversion.md) para el formato de versión de producto válido.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-111">See the [**ProductVersion**](productversion.md) property for the valid product version format.</span></span>
-   <span data-ttu-id="1bbbc-112">No se realiza ningún intento de quitar una versión más reciente o igual del producto actual.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-112">No attempt is made to remove a newer or equal version of the current product.</span></span>

<span data-ttu-id="1bbbc-113">Si no se corrige una advertencia o un error informados por:, generalmente se producen problemas en la actualización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-113">Failure to fix a warning or error reported by ICE61 generally leads to problems in upgrading your application.</span></span> <span data-ttu-id="1bbbc-114">En función del error exacto, podría ser cualquier cosa, desde la salida de los archivos de la versión anterior, la eliminación de los archivos de la versión anterior aunque sean necesarios para la nueva aplicación o un error completo de la actualización.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-114">Depending on the exact error, this could be anything from leaving files from the older version behind, deleting files from the older version even though they are needed by the new application, or complete failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="1bbbc-115">Resultado</span><span class="sxs-lookup"><span data-stu-id="1bbbc-115">Result</span></span>

<span data-ttu-id="1bbbc-116">: Expone una advertencia o un error si no se cumple alguna de las condiciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-116">ICE61 posts a warning or error if any of the above conditions are not true.</span></span>

## <a name="example"></a><span data-ttu-id="1bbbc-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1bbbc-117">Example</span></span>

<span data-ttu-id="1bbbc-118">: Notifica los siguientes errores y advertencias para los ejemplos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-118">ICE61 reports the following errors and warning for the examples shown.</span></span>

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

<span data-ttu-id="1bbbc-119">En este caso, la primera fila intentaría quitar un producto de la misma versión.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-119">In this case, the first row would try to remove a product of the same version.</span></span> <span data-ttu-id="1bbbc-120">(VersionMax columna es igual a la versión del producto en la tabla de propiedades).</span><span class="sxs-lookup"><span data-stu-id="1bbbc-120">(VersionMax column is equal to the product version in the Property table).</span></span>

<span data-ttu-id="1bbbc-121">Para corregir este error, use una versión de la columna VersionMax anterior a la versión actual especificada en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-121">To fix this error, use a version in the VersionMax column lower than the current version specified in the Property table.</span></span> <span data-ttu-id="1bbbc-122">Quite el bit **msidbUpgradeAttributesVersionMaxInclusive** de la columna Attributes si el valor de VersionMax es igual a la versión actual.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-122">Remove the **msidbUpgradeAttributesVersionMaxInclusive** bit from the Attributes column if the VersionMax is equal to the current version.</span></span> <span data-ttu-id="1bbbc-123">Si la intención es solo detectar el producto y no quitarlo, al agregar el bit **msidbUpgradeAttributesOnlyDetect** a la columna atributos también se corregirá este error.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-123">If the intent is only to detect the product and not remove it, adding the **msidbUpgradeAttributesOnlyDetect** bit to the Attributes column will also fix this error.</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

<span data-ttu-id="1bbbc-124">A menos que la propiedad se muestre en la propiedad [**SecureCustomProperties**](securecustomproperties.md) , la propiedad no se pasa al lado del servidor de la instalación cuando se encuentra la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-124">Unless the property is listed in the [**SecureCustomProperties**](securecustomproperties.md) property, the property is not passed to the server side of the install when the property is found.</span></span>

<span data-ttu-id="1bbbc-125">Para corregir este error, agregue la propiedad a [**SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="1bbbc-125">To fix this error, add the property to [**SecureCustomProperties**](securecustomproperties.md).</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

<span data-ttu-id="1bbbc-126">Las propiedades de actualización deben ser propiedades públicas del resultado que se va a pasar al lado del servidor de la instalación.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-126">Upgrade properties must be public properties for the result to be passed to the server side of the installation.</span></span>

<span data-ttu-id="1bbbc-127">Para corregir este error, utilice todas las letras mayúsculas en el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-127">To fix this error, use all uppercase letters in the property name.</span></span>

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

<span data-ttu-id="1bbbc-128">Una propiedad solo se puede usar en una fila de la tabla de actualización.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-128">A property can only be used in one row of the Upgrade table.</span></span>

<span data-ttu-id="1bbbc-129">Para corregir este error, use una propiedad diferente para la segunda fila.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-129">To fix this error, use a different property for the second row.</span></span>

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

<span data-ttu-id="1bbbc-130">La versión mínima debe ser inferior a la versión máxima.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-130">The minimum version must be less than the maximum version.</span></span>

<span data-ttu-id="1bbbc-131">Para corregir este error, compruebe los números de versión en busca de errores tipográficos.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-131">To fix this error, check your version numbers for typos.</span></span> <span data-ttu-id="1bbbc-132">Si son correctos y desea utilizar el intervalo entre las dos versiones, alterne para que VersionMin sea menor que VersionMax.</span><span class="sxs-lookup"><span data-stu-id="1bbbc-132">If they are correct and you want to use the range between the two versions, switch them so that VersionMin is less than VersionMax.</span></span>

[<span data-ttu-id="1bbbc-133">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="1bbbc-133">Property Table</span></span>](property-table.md)



| <span data-ttu-id="1bbbc-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1bbbc-134">Property</span></span>                                                 | <span data-ttu-id="1bbbc-135">Value</span><span class="sxs-lookup"><span data-stu-id="1bbbc-135">Value</span></span>                                  |
|----------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="1bbbc-136">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="1bbbc-136">**UpgradeCode**</span></span>](upgradecode.md)                       | <span data-ttu-id="1bbbc-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="1bbbc-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |
| [<span data-ttu-id="1bbbc-138">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="1bbbc-138">**ProductVersion**</span></span>](productversion.md)                 | <span data-ttu-id="1bbbc-139">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="1bbbc-139">2.01.0000</span></span>                              |
| [<span data-ttu-id="1bbbc-140">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="1bbbc-140">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="1bbbc-141">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1bbbc-141">OLDAPPFOUND</span></span>                            |



 

[<span data-ttu-id="1bbbc-142">Actualizar tabla</span><span class="sxs-lookup"><span data-stu-id="1bbbc-142">Upgrade Table</span></span>](upgrade-table.md)



| <span data-ttu-id="1bbbc-143">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="1bbbc-143">UpgradeCode</span></span>                            | <span data-ttu-id="1bbbc-144">VersionMin</span><span class="sxs-lookup"><span data-stu-id="1bbbc-144">VersionMin</span></span> | <span data-ttu-id="1bbbc-145">VersionMax</span><span class="sxs-lookup"><span data-stu-id="1bbbc-145">VersionMax</span></span> | <span data-ttu-id="1bbbc-146">Idioma</span><span class="sxs-lookup"><span data-stu-id="1bbbc-146">Language</span></span> | <span data-ttu-id="1bbbc-147">Atributos</span><span class="sxs-lookup"><span data-stu-id="1bbbc-147">Attributes</span></span> | <span data-ttu-id="1bbbc-148">Remove</span><span class="sxs-lookup"><span data-stu-id="1bbbc-148">Remove</span></span>                | <span data-ttu-id="1bbbc-149">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="1bbbc-149">ActionProperty</span></span>  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| <span data-ttu-id="1bbbc-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="1bbbc-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |            | <span data-ttu-id="1bbbc-151">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="1bbbc-151">2.01.0000</span></span>  |          | <span data-ttu-id="1bbbc-152">513</span><span class="sxs-lookup"><span data-stu-id="1bbbc-152">513</span></span>        |                       | <span data-ttu-id="1bbbc-153">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1bbbc-153">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="1bbbc-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="1bbbc-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> | <span data-ttu-id="1bbbc-155">2.01.0001</span><span class="sxs-lookup"><span data-stu-id="1bbbc-155">2.01.0001</span></span>  | <span data-ttu-id="1bbbc-156">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="1bbbc-156">2.01.0000</span></span>  |          |            |                       | <span data-ttu-id="1bbbc-157">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1bbbc-157">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="1bbbc-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span><span class="sxs-lookup"><span data-stu-id="1bbbc-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span></span> | <span data-ttu-id="1bbbc-159">1.00.0000</span><span class="sxs-lookup"><span data-stu-id="1bbbc-159">1.00.0000</span></span>  | <span data-ttu-id="1bbbc-160">2.00.0000</span><span class="sxs-lookup"><span data-stu-id="1bbbc-160">2.00.0000</span></span>  | <span data-ttu-id="1bbbc-161">3082</span><span class="sxs-lookup"><span data-stu-id="1bbbc-161">1033</span></span>     |            | <span data-ttu-id="1bbbc-162">\[AppFeatureEnglish\]</span><span class="sxs-lookup"><span data-stu-id="1bbbc-162">\[AppFeatureEnglish\]</span></span> | <span data-ttu-id="1bbbc-163">EnglishAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1bbbc-163">EnglishAPPFOUND</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1bbbc-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1bbbc-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bbbc-165">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="1bbbc-165">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



