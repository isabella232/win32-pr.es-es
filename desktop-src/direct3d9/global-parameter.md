---
description: Cada efecto compatible con DXSAS debe definir, como mínimo, un parámetro de efecto global único con la semántica global.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parámetro global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714733"
---
# <a name="global-parameter"></a><span data-ttu-id="84017-103">Parámetro global</span><span class="sxs-lookup"><span data-stu-id="84017-103">Global Parameter</span></span>

<span data-ttu-id="84017-104">Cada efecto compatible con DXSAS debe definir, como mínimo, un parámetro de efecto global único con la semántica global.</span><span class="sxs-lookup"><span data-stu-id="84017-104">Each DXSAS compliant effect must define, as a minimum, a single global effect parameter with the global semantic.</span></span> <span data-ttu-id="84017-105">El parámetro global también puede usar una o varias anotaciones opcionales.</span><span class="sxs-lookup"><span data-stu-id="84017-105">The global parameter can also use one or more optional annotations.</span></span> <span data-ttu-id="84017-106">La sintaxis es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="84017-106">The syntax is as follows:</span></span>


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



<span data-ttu-id="84017-107">donde:</span><span class="sxs-lookup"><span data-stu-id="84017-107">where:</span></span>

-   <span data-ttu-id="84017-108">VariableName es un nombre de variable de cadena de texto ASCII especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="84017-108">VariableName is a user-specified, ASCII text string variable name.</span></span>
-   <span data-ttu-id="84017-109">SasGlobal es la palabra clave semántica que identifica este parámetro como el parámetro DXSAS global.</span><span class="sxs-lookup"><span data-stu-id="84017-109">SasGlobal is the semantic keyword that identifies this parameter as the global DXSAS parameter.</span></span>
-   <span data-ttu-id="84017-110">SasVersion es la única anotación requerida.</span><span class="sxs-lookup"><span data-stu-id="84017-110">SasVersion is the only required annotation.</span></span>
-   <span data-ttu-id="84017-111">OptionalAnnotations puede incluir lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="84017-111">OptionalAnnotations can include the following:</span></span>
    -   [<span data-ttu-id="84017-112">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="84017-112">SasEffectAuthor</span></span>](#saseffectauthor)
    -   [<span data-ttu-id="84017-113">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="84017-113">SasEffectAuthoringSoftware</span></span>](#saseffectauthoringsoftware)
    -   [<span data-ttu-id="84017-114">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="84017-114">SasEffectCategory</span></span>](#saseffectcategory)
    -   [<span data-ttu-id="84017-115">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="84017-115">SasEffectCompany</span></span>](#saseffectcompany)
    -   [<span data-ttu-id="84017-116">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="84017-116">SasEffectDescription</span></span>](#saseffectdescription)
    -   [<span data-ttu-id="84017-117">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="84017-117">SasEffectHelp</span></span>](#saseffecthelp)
    -   [<span data-ttu-id="84017-118">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="84017-118">SasEffectRevision</span></span>](#saseffectrevision)

## <a name="sasversion"></a><span data-ttu-id="84017-119">SasVersion</span><span class="sxs-lookup"><span data-stu-id="84017-119">SasVersion</span></span>

<span data-ttu-id="84017-120">La única anotación necesaria es SasVersion.</span><span class="sxs-lookup"><span data-stu-id="84017-120">The only required annotation is SasVersion.</span></span> <span data-ttu-id="84017-121">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-121">It is declared like this:</span></span>


```
int3 SasVersion = { major, minor, revision };
```



<span data-ttu-id="84017-122">donde:</span><span class="sxs-lookup"><span data-stu-id="84017-122">where:</span></span>

-   <span data-ttu-id="84017-123">Major indica la versión principal de DXSAS.</span><span class="sxs-lookup"><span data-stu-id="84017-123">major indicates the DXSAS major release.</span></span> <span data-ttu-id="84017-124">Las versiones principales de DXSAS pueden contener cambios de barrido en el conjunto de semánticas y anotaciones definidas.</span><span class="sxs-lookup"><span data-stu-id="84017-124">Major releases of DXSAS can contain sweeping changes to the set of semantics and annotations defined.</span></span> <span data-ttu-id="84017-125">La semántica y las anotaciones se pueden agregar y quitar y, en general, no se garantiza la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="84017-125">Semantics and annotations can be added and removed and, in general, backward compatibility with previous releases is not guaranteed.</span></span>
-   <span data-ttu-id="84017-126">Minor indica la versión secundaria de SAS.</span><span class="sxs-lookup"><span data-stu-id="84017-126">minor indicates the SAS minor release.</span></span> <span data-ttu-id="84017-127">Las versiones secundarias de DXSAS pueden incluir la adición de nuevas semánticas o anotaciones.</span><span class="sxs-lookup"><span data-stu-id="84017-127">Minor releases of DXSAS can include the addition of new semantics or annotations.</span></span> <span data-ttu-id="84017-128">Además, la semántica y las anotaciones se pueden marcar como desusadas en el estándar DXSAS.</span><span class="sxs-lookup"><span data-stu-id="84017-128">Additionally, semantics and annotations may be marked as deprecated in the DXSAS standard.</span></span> <span data-ttu-id="84017-129">Las aplicaciones host todavía deben admitir la semántica y las anotaciones desusadas, pero pueden emitir un diagnóstico de advertencia cuando se use una semántica o una anotación de este tipo.</span><span class="sxs-lookup"><span data-stu-id="84017-129">Deprecated semantics and annotations must still be supported by host applications but can emit a warning diagnostic when such a semantic or annotation is used.</span></span> <span data-ttu-id="84017-130">Las versiones secundarias son compatibles con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="84017-130">Minor releases are backward compatible with previous releases.</span></span>
-   <span data-ttu-id="84017-131">revisión indica la revisión de DXSAS.</span><span class="sxs-lookup"><span data-stu-id="84017-131">revision indicates the DXSAS revision.</span></span> <span data-ttu-id="84017-132">Las revisiones de DXSAS solo existen como un medio para corregir errores, quitar ambigüedad y perfeccionar el estándar.</span><span class="sxs-lookup"><span data-stu-id="84017-132">Revisions of DXSAS exist only as a means to fix bugs, remove ambiguity, and refine the standard.</span></span> <span data-ttu-id="84017-133">Las revisiones del estándar son compatibles con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="84017-133">Revisions to the standard are backward compatible with previous releases.</span></span>

<span data-ttu-id="84017-134">La versión actual es 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="84017-134">The current version is 1.0.0.</span></span> <span data-ttu-id="84017-135">No hay ningún valor predeterminado para esta anotación.</span><span class="sxs-lookup"><span data-stu-id="84017-135">There is no default value for this annotation.</span></span>

## <a name="saseffectauthor"></a><span data-ttu-id="84017-136">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="84017-136">SasEffectAuthor</span></span>

<span data-ttu-id="84017-137">Esto declara a la persona que creó el efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-137">This declares the person who created the effect.</span></span> <span data-ttu-id="84017-138">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-138">It is declared like this:</span></span>


```
string SasEffectAuthor = "value";
```



<span data-ttu-id="84017-139">donde value es una cadena que identifica el autor del efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-139">where value is a string that identifies the effect author.</span></span> <span data-ttu-id="84017-140">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="84017-140">The default is an empty string.</span></span>

## <a name="saseffectauthoringsoftware"></a><span data-ttu-id="84017-141">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="84017-141">SasEffectAuthoringSoftware</span></span>

<span data-ttu-id="84017-142">Esto declara el software en el que se creó el efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-142">This declares the software that the effect was authored on.</span></span> <span data-ttu-id="84017-143">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-143">It is declared like this:</span></span>


```
string SasEffectAuthoringSoftware = "value";
```



<span data-ttu-id="84017-144">donde value es una cadena que identifica el software de creación de efectos.</span><span class="sxs-lookup"><span data-stu-id="84017-144">where value is a string that identifies the effect authoring software.</span></span> <span data-ttu-id="84017-145">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="84017-145">The default is an empty string.</span></span>

## <a name="saseffectcategory"></a><span data-ttu-id="84017-146">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="84017-146">SasEffectCategory</span></span>

<span data-ttu-id="84017-147">Esto declara la categoría del efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-147">This declares the effect category.</span></span> <span data-ttu-id="84017-148">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-148">It is declared like this:</span></span>


```
string SasEffectCategory = "value";
```



<span data-ttu-id="84017-149">donde valor es una cadena que identifica la categoría del efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-149">where value is a string that identifies the effect category.</span></span> <span data-ttu-id="84017-150">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="84017-150">The default is an empty string.</span></span> <span data-ttu-id="84017-151">La categoría se expresa mediante un valor similar a la ruta de acceso mediante la barra diagonal como delimitador.</span><span class="sxs-lookup"><span data-stu-id="84017-151">The category is expressed via a path-like value using the forward slash as a delimiter.</span></span> <span data-ttu-id="84017-152">Los efectos solo pueden pertenecer a una categoría, ya que no hay ninguna sintaxis para expresar la inclusión en varias rutas de acceso dentro de un valor de SasEffectCategory único.</span><span class="sxs-lookup"><span data-stu-id="84017-152">Effects can only belong to one category as there is no syntax for expressing inclusion in multiple paths within a single SasEffectCategory value.</span></span> <span data-ttu-id="84017-153">La aplicación host no trata el valor de esta anotación como lo distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84017-153">The value of this annotation is not treated as case-sensitive by the host application.</span></span>

## <a name="saseffectcompany"></a><span data-ttu-id="84017-154">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="84017-154">SasEffectCompany</span></span>

<span data-ttu-id="84017-155">Esto declara la compañía que creó el efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-155">This declares the company that created the effect.</span></span> <span data-ttu-id="84017-156">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-156">It is declared like this:</span></span>


```
string SasEffectCompany = "value";
```



<span data-ttu-id="84017-157">donde value es una cadena que identifica el nombre de la compañía a la que pertenece el efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-157">where value is a string that identifies the name of the company that owns the effect.</span></span> <span data-ttu-id="84017-158">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="84017-158">The default is an empty string.</span></span>

## <a name="saseffectdescription"></a><span data-ttu-id="84017-159">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="84017-159">SasEffectDescription</span></span>

<span data-ttu-id="84017-160">Esto describe el efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-160">This describes the effect.</span></span> <span data-ttu-id="84017-161">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-161">It is declared like this:</span></span>


```
string SasEffectDescription = "value";
```



<span data-ttu-id="84017-162">donde value es una cadena que describe el efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-162">where value is a string that describes the effect.</span></span> <span data-ttu-id="84017-163">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="84017-163">The default is an empty string.</span></span>

## <a name="saseffecthelp"></a><span data-ttu-id="84017-164">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="84017-164">SasEffectHelp</span></span>

<span data-ttu-id="84017-165">Se trata de una cadena de ayuda que se puede mostrar al usuario cada vez que se solicita ayuda sobre el efecto asociado.</span><span class="sxs-lookup"><span data-stu-id="84017-165">This is a help string that can be displayed to the user whenever help on the associated effect is requested.</span></span> <span data-ttu-id="84017-166">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-166">It is declared like this:</span></span>


```
string SasEffectHelp = "value";
```



<span data-ttu-id="84017-167">donde value es una cadena que se puede mostrar si el usuario solicita ayuda.</span><span class="sxs-lookup"><span data-stu-id="84017-167">where value is a string that can be displayed if the user requests help.</span></span> <span data-ttu-id="84017-168">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="84017-168">The default is an empty string.</span></span>

## <a name="saseffectrevision"></a><span data-ttu-id="84017-169">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="84017-169">SasEffectRevision</span></span>

<span data-ttu-id="84017-170">Esta anotación permite a las herramientas y los usuarios registrar el número de revisión del archivo de efectos asociado.</span><span class="sxs-lookup"><span data-stu-id="84017-170">This annotation allows tools and users to record the revision number of the associated effect file.</span></span> <span data-ttu-id="84017-171">Por ejemplo, los usuarios podrían insertar las palabras clave adecuadas en el valor de esta anotación para invocar la sustitución de palabras clave en su software de control de revisiones favorito.</span><span class="sxs-lookup"><span data-stu-id="84017-171">For example, users could insert appropriate keywords in the value of this annotation to invoke keyword substitution in their favorite revision control software.</span></span> <span data-ttu-id="84017-172">Se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84017-172">It is declared like this:</span></span>


```
string SasEffectRevision = "value";
```



<span data-ttu-id="84017-173">donde value es una cadena que identifica la revisión del efecto.</span><span class="sxs-lookup"><span data-stu-id="84017-173">where value is a string that identifies the effect revision.</span></span> <span data-ttu-id="84017-174">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="84017-174">The default is an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="84017-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="84017-175">Examples</span></span>

<span data-ttu-id="84017-176">A continuación se muestra un ejemplo en el que solo se usa la anotación única requerida:</span><span class="sxs-lookup"><span data-stu-id="84017-176">Here is an example that uses only the single, required annotation:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



<span data-ttu-id="84017-177">Este es un ejemplo que utiliza la anotación requerida y varias anotaciones opcionales:</span><span class="sxs-lookup"><span data-stu-id="84017-177">Here is an example that uses the required annotation and several optional annotations:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a><span data-ttu-id="84017-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84017-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84017-179">Referencia de las anotaciones y semánticas estándar de DirectX</span><span class="sxs-lookup"><span data-stu-id="84017-179">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



