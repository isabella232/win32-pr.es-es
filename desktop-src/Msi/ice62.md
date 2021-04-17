---
description: ICE62 realiza comprobaciones exhaustivas en la tabla IsolatedComponent para los datos que pueden provocar un comportamiento inesperado.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667941"
---
# <a name="ice62"></a><span data-ttu-id="7e352-103">ICE62</span><span class="sxs-lookup"><span data-stu-id="7e352-103">ICE62</span></span>

<span data-ttu-id="7e352-104">ICE62 realiza comprobaciones exhaustivas en la [tabla IsolatedComponent](isolatedcomponent-table.md) para los datos que pueden provocar un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="7e352-104">ICE62 performs extensive checks on the [IsolatedComponent table](isolatedcomponent-table.md) for data that may cause unexpected behavior.</span></span>

<span data-ttu-id="7e352-105">Si no se corrige un error detectado por ICE62, puede producirse un error en el sistema de componentes aislados en una gran variedad de formas.</span><span class="sxs-lookup"><span data-stu-id="7e352-105">Failure to fix an error reported by ICE62 can result in a failure of the isolated component system in a wide variety of ways.</span></span> <span data-ttu-id="7e352-106">Por ejemplo, si no se establece el bit SharedDllRefCount para un componente compartido, el registro del componente podría quitarse cuando otra aplicación utiliza ese ComponentId y se desinstala.</span><span class="sxs-lookup"><span data-stu-id="7e352-106">For example, if the SharedDllRefCount bit is not set for a shared component, the registration for the component could be removed when another application uses that ComponentId and is uninstalled.</span></span>

## <a name="result"></a><span data-ttu-id="7e352-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="7e352-107">Result</span></span>

<span data-ttu-id="7e352-108">ICE62 publica una advertencia o un error cuando encuentra datos en la tabla IsolatedComponent que pueden producir un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="7e352-108">ICE62 posts a warning or error when it finds data in the IsolatedComponent table that may produce unexpected behavior.</span></span>

## <a name="example"></a><span data-ttu-id="7e352-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e352-109">Example</span></span>

<span data-ttu-id="7e352-110">ICE62 notifica los siguientes errores y advertencias para los ejemplos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="7e352-110">ICE62 reports the following errors and warning for the examples shown.</span></span>

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

<span data-ttu-id="7e352-111">Component2 aparece como componente de la aplicación para el aislamiento de component1.</span><span class="sxs-lookup"><span data-stu-id="7e352-111">Component2 is listed as the application component for the isolation of component1.</span></span> <span data-ttu-id="7e352-112">Sin embargo, Component2 tiene una ruta de acceso de clave del registro y no proporciona una ruta de acceso ejecutable válida que se pueda usar para aislar el componente.</span><span class="sxs-lookup"><span data-stu-id="7e352-112">However, Component2 has a registry key path, and does not provide a valid executable path to use to isolate the component.</span></span>

<span data-ttu-id="7e352-113">Para corregir este error, use otro componente como la aplicación del componente de modo aislado component1.</span><span class="sxs-lookup"><span data-stu-id="7e352-113">To fix this error, use a different component as the application for the isolated component Component1.</span></span>

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

<span data-ttu-id="7e352-114">Component1 aparece como un componente compartido aislado, pero no tiene establecido el bit SharedDllRefCount.</span><span class="sxs-lookup"><span data-stu-id="7e352-114">Component1 is listed as an isolated shared component, but does not have the SharedDllRefCount bit set.</span></span> <span data-ttu-id="7e352-115">Esto podría dar lugar a que la duración del componente sea incorrecta.</span><span class="sxs-lookup"><span data-stu-id="7e352-115">This could result in the lifetime of the component being incorrect.</span></span> <span data-ttu-id="7e352-116">Si otra aplicación utiliza este componente (aislado o no) y se desinstala, el registro del componente se quita pero la copia aislada de la aplicación permanece.</span><span class="sxs-lookup"><span data-stu-id="7e352-116">If another application uses this component (isolated or not) and is uninstalled, the registration for the component is removed but this application's isolated copy remains.</span></span> <span data-ttu-id="7e352-117">Esto provoca problemas de reparación y desinstalación.</span><span class="sxs-lookup"><span data-stu-id="7e352-117">This causes repair and uninstall problems.</span></span>

<span data-ttu-id="7e352-118">Para corregir este error, establezca el bit SharedDllRefCount para el componente.</span><span class="sxs-lookup"><span data-stu-id="7e352-118">To fix this error, set the SharedDllRefCount bit for the component.</span></span>

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

<span data-ttu-id="7e352-119">Component1 y Component2 se instalan con características diferentes.</span><span class="sxs-lookup"><span data-stu-id="7e352-119">Component1 and Component2 are installed by different features.</span></span> <span data-ttu-id="7e352-120">Component1 se instala mediante Feature1 y Component2 se instala mediante Característica2.</span><span class="sxs-lookup"><span data-stu-id="7e352-120">Component1 is installed by Feature1, and Component2 is installed by Feature2.</span></span> <span data-ttu-id="7e352-121">Feature1 no es un elemento primario de Característica2, por lo que es posible que la aplicación se instale, pero no el componente aislado, lo que interrumpe el aislamiento.</span><span class="sxs-lookup"><span data-stu-id="7e352-121">Feature1 is not a parent of Feature2, hence it is possible for the application to be installed but not the isolated component, breaking the isolation.</span></span>

<span data-ttu-id="7e352-122">Para corregir este error, agregue una entrada a la tabla FeatureComponents vinculando Component1 a la misma característica que (o una característica primaria de) la característica que instala Component2.</span><span class="sxs-lookup"><span data-stu-id="7e352-122">To fix this error, add an entry to the FeatureComponents table linking Component1 to the same feature as (or a parent feature of) the feature that installs Component2.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

<span data-ttu-id="7e352-123">Component1 tiene una condición en la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="7e352-123">Component1 has a condition in the Component table.</span></span> <span data-ttu-id="7e352-124">Si alguna vez cambia la condición de TRUE a FALSE durante la vigencia de una instalación en un equipo, el componente aislado podría quedar huérfano sin información de registro.</span><span class="sxs-lookup"><span data-stu-id="7e352-124">If this condition ever changes from TRUE to FALSE during the lifetime of an installation on a computer, the isolated component could be orphaned without registration information.</span></span>

<span data-ttu-id="7e352-125">Para corregir esta advertencia, quite la condición o cree la condición para que nunca pueda cambiar de TRUE a FALSE.</span><span class="sxs-lookup"><span data-stu-id="7e352-125">To fix this warning, remove the condition, or author the condition so that it can never change from TRUE to FALSE.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

<span data-ttu-id="7e352-126">Component1 está aislado para Component2 y Component3, y los dos componentes también se instalan en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="7e352-126">Component1 is isolated for both Component2 and Component3, and the two components are also installed to the same directory.</span></span> <span data-ttu-id="7e352-127">Las aplicaciones comparten un componente aislado, pero si se quita una aplicación, se quita el componente compartido, lo que hace que las demás aplicaciones pierdan el componente aislado.</span><span class="sxs-lookup"><span data-stu-id="7e352-127">The applications share an isolated component, but if one application is removed the shared component is removed as well causing the other applications to lose the isolated component.</span></span>

<span data-ttu-id="7e352-128">Para corregir esta advertencia, instale las aplicaciones en directorios diferentes o Compruebe si algunas de las aplicaciones requieren realmente un componente aislado.</span><span class="sxs-lookup"><span data-stu-id="7e352-128">To fix this warning, install the applications to different directories or check whether some of the applications truly require an isolated component.</span></span>

[<span data-ttu-id="7e352-129">Tabla IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="7e352-129">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="7e352-130">Componente \_ compartido</span><span class="sxs-lookup"><span data-stu-id="7e352-130">Component\_Shared</span></span> | <span data-ttu-id="7e352-131">Aplicación de componentes \_</span><span class="sxs-lookup"><span data-stu-id="7e352-131">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="7e352-132">Component1</span><span class="sxs-lookup"><span data-stu-id="7e352-132">Component1</span></span>        | <span data-ttu-id="7e352-133">Component2</span><span class="sxs-lookup"><span data-stu-id="7e352-133">Component2</span></span>             |
| <span data-ttu-id="7e352-134">Component1</span><span class="sxs-lookup"><span data-stu-id="7e352-134">Component1</span></span>        | <span data-ttu-id="7e352-135">Component3</span><span class="sxs-lookup"><span data-stu-id="7e352-135">Component3</span></span>             |



 

[<span data-ttu-id="7e352-136">Tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="7e352-136">Component Table</span></span>](component-table.md)



| <span data-ttu-id="7e352-137">Componente</span><span class="sxs-lookup"><span data-stu-id="7e352-137">Component</span></span>  | <span data-ttu-id="7e352-138">ComponentId</span><span class="sxs-lookup"><span data-stu-id="7e352-138">ComponentId</span></span> | <span data-ttu-id="7e352-139">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="7e352-139">Directory\_</span></span> | <span data-ttu-id="7e352-140">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e352-140">Attributes</span></span> | <span data-ttu-id="7e352-141">Condición</span><span class="sxs-lookup"><span data-stu-id="7e352-141">Condition</span></span>   | <span data-ttu-id="7e352-142">Rutas</span><span class="sxs-lookup"><span data-stu-id="7e352-142">KeyPath</span></span>   |
|------------|-------------|-------------|------------|-------------|-----------|
| <span data-ttu-id="7e352-143">Component1</span><span class="sxs-lookup"><span data-stu-id="7e352-143">Component1</span></span> |             | <span data-ttu-id="7e352-144">Dir1</span><span class="sxs-lookup"><span data-stu-id="7e352-144">Dir1</span></span>        | <span data-ttu-id="7e352-145">0</span><span class="sxs-lookup"><span data-stu-id="7e352-145">0</span></span>          | <span data-ttu-id="7e352-146">Mi condición</span><span class="sxs-lookup"><span data-stu-id="7e352-146">MYCONDITION</span></span> | <span data-ttu-id="7e352-147">Archivo1</span><span class="sxs-lookup"><span data-stu-id="7e352-147">File1</span></span>     |
| <span data-ttu-id="7e352-148">Component2</span><span class="sxs-lookup"><span data-stu-id="7e352-148">Component2</span></span> |             | <span data-ttu-id="7e352-149">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="7e352-149">TARGETDIR</span></span>   | <span data-ttu-id="7e352-150">4</span><span class="sxs-lookup"><span data-stu-id="7e352-150">4</span></span>          |             | <span data-ttu-id="7e352-151">Registry2</span><span class="sxs-lookup"><span data-stu-id="7e352-151">Registry2</span></span> |
| <span data-ttu-id="7e352-152">Component3</span><span class="sxs-lookup"><span data-stu-id="7e352-152">Component3</span></span> |             | <span data-ttu-id="7e352-153">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="7e352-153">TARGETDIR</span></span>   | <span data-ttu-id="7e352-154">0</span><span class="sxs-lookup"><span data-stu-id="7e352-154">0</span></span>          |             | <span data-ttu-id="7e352-155">File3</span><span class="sxs-lookup"><span data-stu-id="7e352-155">File3</span></span>     |



 

[<span data-ttu-id="7e352-156">FeatureComponentsTable</span><span class="sxs-lookup"><span data-stu-id="7e352-156">FeatureComponentsTable</span></span>](featurecomponents-table.md)



| <span data-ttu-id="7e352-157">Característica\_</span><span class="sxs-lookup"><span data-stu-id="7e352-157">Feature\_</span></span> | <span data-ttu-id="7e352-158">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7e352-158">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="7e352-159">Feature1</span><span class="sxs-lookup"><span data-stu-id="7e352-159">Feature1</span></span>  | <span data-ttu-id="7e352-160">Component1</span><span class="sxs-lookup"><span data-stu-id="7e352-160">Component1</span></span>  |
| <span data-ttu-id="7e352-161">Característica2</span><span class="sxs-lookup"><span data-stu-id="7e352-161">Feature2</span></span>  | <span data-ttu-id="7e352-162">Component2</span><span class="sxs-lookup"><span data-stu-id="7e352-162">Component2</span></span>  |
| <span data-ttu-id="7e352-163">Feature1</span><span class="sxs-lookup"><span data-stu-id="7e352-163">Feature1</span></span>  | <span data-ttu-id="7e352-164">Component3</span><span class="sxs-lookup"><span data-stu-id="7e352-164">Component3</span></span>  |



 

<span data-ttu-id="7e352-165">[Tabla de características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7e352-165">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="7e352-166">Característica</span><span class="sxs-lookup"><span data-stu-id="7e352-166">Feature</span></span>  | <span data-ttu-id="7e352-167">Característica \_ principal</span><span class="sxs-lookup"><span data-stu-id="7e352-167">Feature\_Parent</span></span> |
|----------|-----------------|
| <span data-ttu-id="7e352-168">Feature1</span><span class="sxs-lookup"><span data-stu-id="7e352-168">Feature1</span></span> |                 |
| <span data-ttu-id="7e352-169">Característica2</span><span class="sxs-lookup"><span data-stu-id="7e352-169">Feature2</span></span> |                 |



 

## <a name="related-topics"></a><span data-ttu-id="7e352-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e352-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e352-171">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="7e352-171">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



