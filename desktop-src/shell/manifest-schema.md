---
description: Estos elementos componen el esquema XML que se usa en el manifiesto de transferencia del Asistente para la publicación web y el orden de impresión en línea.
title: Transferir esquema de manifiesto
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997837"
---
# <a name="transfer-manifest-schema"></a><span data-ttu-id="92d09-103">Transferir esquema de manifiesto</span><span class="sxs-lookup"><span data-stu-id="92d09-103">Transfer Manifest Schema</span></span>

<span data-ttu-id="92d09-104">Estos elementos componen el esquema XML que se usa en el manifiesto de transferencia del Asistente para la publicación web y el orden de impresión en línea.</span><span class="sxs-lookup"><span data-stu-id="92d09-104">These elements make up the XML schema used in the Web Publishing and Online Print Ordering wizards' transfer manifest.</span></span>

<span data-ttu-id="92d09-105">Los siguientes elementos se definen para el manifiesto de transferencia.</span><span class="sxs-lookup"><span data-stu-id="92d09-105">The following elements are defined for the transfer manifest.</span></span>

-   [<span data-ttu-id="92d09-106">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="92d09-106">cancelledpage</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-107">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-108">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-110">failurepage</span><span class="sxs-lookup"><span data-stu-id="92d09-110">failurepage</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-111">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-112">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-114">Favoritos</span><span class="sxs-lookup"><span data-stu-id="92d09-114">favorite</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-115">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-116">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-117">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-118">file</span><span class="sxs-lookup"><span data-stu-id="92d09-118">file</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-119">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-120">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-121">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-121">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-122">FileList</span><span class="sxs-lookup"><span data-stu-id="92d09-122">filelist</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-123">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-124">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-125">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-126">directorio</span><span class="sxs-lookup"><span data-stu-id="92d09-126">folder</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-127">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-128">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-129">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-129">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-130">folderlist</span><span class="sxs-lookup"><span data-stu-id="92d09-130">folderlist</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-131">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-131">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-132">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-133">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-134">formdata</span><span class="sxs-lookup"><span data-stu-id="92d09-134">formdata</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-135">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-135">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-136">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-136">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-137">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-137">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-138">htmlui</span><span class="sxs-lookup"><span data-stu-id="92d09-138">htmlui</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-139">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-139">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-140">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-140">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-141">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-141">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-142">imageproperty</span><span class="sxs-lookup"><span data-stu-id="92d09-142">imageproperty</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-143">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-143">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-144">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-144">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-145">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-145">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-146">metadata</span><span class="sxs-lookup"><span data-stu-id="92d09-146">metadata</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-147">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-147">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-148">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-148">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-149">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-149">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-150">netplace</span><span class="sxs-lookup"><span data-stu-id="92d09-150">netplace</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-151">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-151">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-152">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-152">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-153">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-153">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-154">Exponer</span><span class="sxs-lookup"><span data-stu-id="92d09-154">post</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-155">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-155">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-156">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-156">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-157">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-157">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-158">cambiar el tamaño</span><span class="sxs-lookup"><span data-stu-id="92d09-158">resize</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-159">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-159">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-160">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-160">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-161">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-161">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-162">successpage</span><span class="sxs-lookup"><span data-stu-id="92d09-162">successpage</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-163">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-163">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-164">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-164">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-165">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-165">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-166">Destino</span><span class="sxs-lookup"><span data-stu-id="92d09-166">target</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-167">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-167">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-168">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-168">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-169">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-169">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-170">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="92d09-170">transfermanifest</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-171">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-171">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-172">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-172">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-173">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-173">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92d09-174">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-174">uploadinfo</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-175">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-175">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="92d09-176">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-176">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="92d09-177">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-177">Element Information</span></span>](#element-information)

## <a name="cancelledpage"></a><span data-ttu-id="92d09-178">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="92d09-178">cancelledpage</span></span>

<span data-ttu-id="92d09-179">Especifica la página HTML del lado servidor que se va a mostrar antes de que el asistente se cierre cuando el usuario haga clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="92d09-179">Specifies the server-side HTML page to display before the wizard is closed when the user clicks the **Cancel** button.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-180">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-180">Syntax</span></span>


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-181">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-181">Attributes</span></span>



| <span data-ttu-id="92d09-182">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-182">Attribute</span></span> | <span data-ttu-id="92d09-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-183">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-184">href</span><span class="sxs-lookup"><span data-stu-id="92d09-184">href</span></span>      | <span data-ttu-id="92d09-185">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-185">Required.</span></span> <span data-ttu-id="92d09-186">Dirección URL de la página HTML del lado servidor que se va a mostrar cuando el usuario haga clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="92d09-186">The URL of the server-side HTML page to display when the user clicks the **Cancel** button.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-187">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-187">Element Information</span></span>



| <span data-ttu-id="92d09-188">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-188">Parent Element</span></span>        | <span data-ttu-id="92d09-189">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-189">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="92d09-190">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-190">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-191">Ninguno</span><span class="sxs-lookup"><span data-stu-id="92d09-191">None</span></span>           |



 

## <a name="failurepage"></a><span data-ttu-id="92d09-192">failurepage</span><span class="sxs-lookup"><span data-stu-id="92d09-192">failurepage</span></span>

<span data-ttu-id="92d09-193">Especifica la página HTML del lado servidor que se va a mostrar si la carga no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="92d09-193">Specifies the server-side HTML page to display if the upload is not successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-194">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-194">Syntax</span></span>


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-195">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-195">Attributes</span></span>



| <span data-ttu-id="92d09-196">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-196">Attribute</span></span> | <span data-ttu-id="92d09-197">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-197">Description</span></span>                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-198">href</span><span class="sxs-lookup"><span data-stu-id="92d09-198">href</span></span>      | <span data-ttu-id="92d09-199">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-199">Required.</span></span> <span data-ttu-id="92d09-200">Dirección URL de la página HTML del servidor que se va a mostrar si la carga no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="92d09-200">The URL of the server-side HTML page to display if the upload is not successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-201">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-201">Element Information</span></span>



| <span data-ttu-id="92d09-202">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-202">Parent Element</span></span>        | <span data-ttu-id="92d09-203">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-203">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="92d09-204">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-204">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-205">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-205">None.</span></span> <span data-ttu-id="92d09-206">Se permite el texto.</span><span class="sxs-lookup"><span data-stu-id="92d09-206">Text is allowed.</span></span> |



 

## <a name="favorite"></a><span data-ttu-id="92d09-207">Favoritos</span><span class="sxs-lookup"><span data-stu-id="92d09-207">favorite</span></span>

<span data-ttu-id="92d09-208">Indica al asistente que cree una entrada de sitio web favorita en el menú **Favoritos** de la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="92d09-208">Instructs the wizard to create a favorite website entry in the **Favorites** menu for the given URL.</span></span> <span data-ttu-id="92d09-209">Si no se especifica este elemento, el elemento [htmlui](#syntax) se usa en su lugar.</span><span class="sxs-lookup"><span data-stu-id="92d09-209">If this element is not specified, then the [htmlui](#syntax) element is used in its place.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-210">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-210">Syntax</span></span>


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-211">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-211">Attributes</span></span>



| <span data-ttu-id="92d09-212">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-212">Attribute</span></span> | <span data-ttu-id="92d09-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-213">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="92d09-214">comment</span><span class="sxs-lookup"><span data-stu-id="92d09-214">comment</span></span>   | <span data-ttu-id="92d09-215">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-215">Required.</span></span> <span data-ttu-id="92d09-216">Comentario asociado a la entrada **Favoritos** .</span><span class="sxs-lookup"><span data-stu-id="92d09-216">The comment associated with the **Favorites** entry.</span></span>         |
| <span data-ttu-id="92d09-217">href</span><span class="sxs-lookup"><span data-stu-id="92d09-217">href</span></span>      | <span data-ttu-id="92d09-218">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-218">Required.</span></span> <span data-ttu-id="92d09-219">Dirección URL de la entrada de **Favoritos** .</span><span class="sxs-lookup"><span data-stu-id="92d09-219">The URL of the **Favorites** entry.</span></span>                          |
| <span data-ttu-id="92d09-220">name</span><span class="sxs-lookup"><span data-stu-id="92d09-220">name</span></span>      | <span data-ttu-id="92d09-221">Necesario.</span><span class="sxs-lookup"><span data-stu-id="92d09-221">Required.</span></span> <span data-ttu-id="92d09-222">El nombre de la dirección URL que aparece en el menú **Favoritos** .</span><span class="sxs-lookup"><span data-stu-id="92d09-222">The name for the URL that appears in the **Favorites** menu.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-223">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-223">Element Information</span></span>



| <span data-ttu-id="92d09-224">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-224">Parent Element</span></span>        | <span data-ttu-id="92d09-225">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-225">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="92d09-226">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-226">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-227">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-227">None.</span></span> <span data-ttu-id="92d09-228">Se permite el texto.</span><span class="sxs-lookup"><span data-stu-id="92d09-228">Text is allowed.</span></span> |



 

## <a name="file"></a><span data-ttu-id="92d09-229">archivo</span><span class="sxs-lookup"><span data-stu-id="92d09-229">file</span></span>

<span data-ttu-id="92d09-230">Describe un solo archivo que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="92d09-230">Describes a single file to be copied.</span></span> <span data-ttu-id="92d09-231">Se pueden incluir varios elementos de [archivo](#syntax) en un solo nodo [FileList](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-231">Multiple [file](#syntax) elements may be contained under a single [filelist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-232">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-232">Syntax</span></span>


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-233">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-233">Attributes</span></span>



| <span data-ttu-id="92d09-234">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-234">Attribute</span></span>   | <span data-ttu-id="92d09-235">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-235">Description</span></span>                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-236">ContentType</span><span class="sxs-lookup"><span data-stu-id="92d09-236">contenttype</span></span> | <span data-ttu-id="92d09-237">Opcional.</span><span class="sxs-lookup"><span data-stu-id="92d09-237">Optional.</span></span> <span data-ttu-id="92d09-238">Tipo MIME del archivo.</span><span class="sxs-lookup"><span data-stu-id="92d09-238">The MIME type of the file.</span></span>                                                                                                                                         |
| <span data-ttu-id="92d09-239">destination</span><span class="sxs-lookup"><span data-stu-id="92d09-239">destination</span></span> | <span data-ttu-id="92d09-240">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-240">Required.</span></span> <span data-ttu-id="92d09-241">Una ruta de acceso sugerida para el archivo una vez cargado.</span><span class="sxs-lookup"><span data-stu-id="92d09-241">A suggested path for the file once it is uploaded.</span></span> <span data-ttu-id="92d09-242">Esta ruta de acceso es relativa a la dirección URL de destino del sitio de carga.</span><span class="sxs-lookup"><span data-stu-id="92d09-242">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="92d09-243">El sitio de carga puede modificar este valor según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="92d09-243">The upload site can modify this value as necessary.</span></span> |
| <span data-ttu-id="92d09-244">extensión</span><span class="sxs-lookup"><span data-stu-id="92d09-244">extension</span></span>   | <span data-ttu-id="92d09-245">Opcional.</span><span class="sxs-lookup"><span data-stu-id="92d09-245">Optional.</span></span> <span data-ttu-id="92d09-246">La extensión de nombre de archivo del archivo.</span><span class="sxs-lookup"><span data-stu-id="92d09-246">The file name extension of the file.</span></span>                                                                                                                               |
| <span data-ttu-id="92d09-247">id</span><span class="sxs-lookup"><span data-stu-id="92d09-247">id</span></span>          | <span data-ttu-id="92d09-248">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-248">Required.</span></span> <span data-ttu-id="92d09-249">Índice numérico del archivo.</span><span class="sxs-lookup"><span data-stu-id="92d09-249">The numerical index of the file.</span></span>                                                                                                                                   |
| <span data-ttu-id="92d09-250">tamaño</span><span class="sxs-lookup"><span data-stu-id="92d09-250">size</span></span>        | <span data-ttu-id="92d09-251">Opcional.</span><span class="sxs-lookup"><span data-stu-id="92d09-251">Optional.</span></span> <span data-ttu-id="92d09-252">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="92d09-252">The size of the file, in bytes.</span></span>                                                                                                                                    |
| <span data-ttu-id="92d09-253">source</span><span class="sxs-lookup"><span data-stu-id="92d09-253">source</span></span>      | <span data-ttu-id="92d09-254">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-254">Required.</span></span> <span data-ttu-id="92d09-255">Ruta de acceso completa del sistema de archivos para el archivo.</span><span class="sxs-lookup"><span data-stu-id="92d09-255">The full file system path for the file.</span></span>                                                                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="92d09-256">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-256">Element Information</span></span>



| <span data-ttu-id="92d09-257">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-257">Parent Element</span></span>      | <span data-ttu-id="92d09-258">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-258">Child Elements</span></span>                                          |
|---------------------|---------------------------------------------------------|
| [<span data-ttu-id="92d09-259">FileList</span><span class="sxs-lookup"><span data-stu-id="92d09-259">filelist</span></span>](#syntax) | <span data-ttu-id="92d09-260">[metadatos](#syntax), [post](#syntax), [cambiar tamaño](#syntax)</span><span class="sxs-lookup"><span data-stu-id="92d09-260">[metadata](#syntax), [post](#syntax), [resize](#syntax)</span></span> |



 

## <a name="filelist"></a><span data-ttu-id="92d09-261">FileList</span><span class="sxs-lookup"><span data-stu-id="92d09-261">filelist</span></span>

<span data-ttu-id="92d09-262">Contenedor de elementos que describen los archivos que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="92d09-262">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="92d09-263">Varios elementos [FileList](#syntax) pueden estar contenidos en un único nodo [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-263">Multiple [filelist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-264">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-264">Syntax</span></span>


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-265">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-265">Attributes</span></span>



| <span data-ttu-id="92d09-266">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-266">Attribute</span></span>   | <span data-ttu-id="92d09-267">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-267">Description</span></span>      |
|-------------|------------------|
| <span data-ttu-id="92d09-268">usesfolders</span><span class="sxs-lookup"><span data-stu-id="92d09-268">usesfolders</span></span> | <span data-ttu-id="92d09-269">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="92d09-269">Not implemented.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-270">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-270">Element Information</span></span>



| <span data-ttu-id="92d09-271">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-271">Parent Element</span></span>              | <span data-ttu-id="92d09-272">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-272">Child Elements</span></span>  |
|-----------------------------|-----------------|
| [<span data-ttu-id="92d09-273">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="92d09-273">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="92d09-274">file</span><span class="sxs-lookup"><span data-stu-id="92d09-274">file</span></span>](#syntax) |



 

## <a name="folder"></a><span data-ttu-id="92d09-275">folder</span><span class="sxs-lookup"><span data-stu-id="92d09-275">folder</span></span>

<span data-ttu-id="92d09-276">Describe una carpeta en la que se almacenan los archivos.</span><span class="sxs-lookup"><span data-stu-id="92d09-276">Describes a folder in which files are stored.</span></span> <span data-ttu-id="92d09-277">Varios elementos de [carpeta](#syntax) pueden estar contenidos en un único nodo de [folderList](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-277">Multiple [folder](#syntax) elements may be contained under a single [folderlist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-278">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-278">Syntax</span></span>


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-279">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-279">Attributes</span></span>



| <span data-ttu-id="92d09-280">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-280">Attribute</span></span>   | <span data-ttu-id="92d09-281">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-281">Description</span></span>                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-282">destination</span><span class="sxs-lookup"><span data-stu-id="92d09-282">destination</span></span> | <span data-ttu-id="92d09-283">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-283">Required.</span></span> <span data-ttu-id="92d09-284">Una ruta de acceso sugerida para la carpeta una vez cargada.</span><span class="sxs-lookup"><span data-stu-id="92d09-284">A suggested path for the folder once it is uploaded.</span></span> <span data-ttu-id="92d09-285">Esta ruta de acceso es relativa a la dirección URL de destino del sitio de carga.</span><span class="sxs-lookup"><span data-stu-id="92d09-285">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="92d09-286">El sitio de carga puede modificar este valor según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="92d09-286">The upload site can modify this value as necessary.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-287">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-287">Element Information</span></span>



| <span data-ttu-id="92d09-288">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-288">Parent Element</span></span>        | <span data-ttu-id="92d09-289">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-289">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="92d09-290">folderlist</span><span class="sxs-lookup"><span data-stu-id="92d09-290">folderlist</span></span>](#syntax) | <span data-ttu-id="92d09-291">Ninguno</span><span class="sxs-lookup"><span data-stu-id="92d09-291">None</span></span>           |



 

## <a name="folderlist"></a><span data-ttu-id="92d09-292">folderlist</span><span class="sxs-lookup"><span data-stu-id="92d09-292">folderlist</span></span>

<span data-ttu-id="92d09-293">Contenedor de elementos que describen los archivos que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="92d09-293">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="92d09-294">Varios elementos [folderList](#syntax) pueden estar contenidos en un único nodo [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-294">Multiple [folderlist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-295">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-295">Syntax</span></span>


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-296">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-296">Attributes</span></span>

<span data-ttu-id="92d09-297">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-297">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="92d09-298">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-298">Element Information</span></span>



| <span data-ttu-id="92d09-299">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-299">Parent Element</span></span>              | <span data-ttu-id="92d09-300">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-300">Child Elements</span></span>    |
|-----------------------------|-------------------|
| [<span data-ttu-id="92d09-301">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="92d09-301">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="92d09-302">directorio</span><span class="sxs-lookup"><span data-stu-id="92d09-302">folder</span></span>](#syntax) |



 

## <a name="formdata"></a><span data-ttu-id="92d09-303">formdata</span><span class="sxs-lookup"><span data-stu-id="92d09-303">formdata</span></span>

<span data-ttu-id="92d09-304">Describe datos de formulario codificados en HTML opcionales que se pueden transferir con los archivos.</span><span class="sxs-lookup"><span data-stu-id="92d09-304">Describes optional HTML encoded form data that may be transferred with the files.</span></span> <span data-ttu-id="92d09-305">El servicio agrega este elemento si opta por cargar los archivos como una publicación de varias partes.</span><span class="sxs-lookup"><span data-stu-id="92d09-305">This element is added by the service if it elects to upload the files as a multi-part post.</span></span> <span data-ttu-id="92d09-306">Los datos del formulario, junto con información del elemento [post](#syntax) , se usan para crear el encabezado post.</span><span class="sxs-lookup"><span data-stu-id="92d09-306">The form data, together with information from the [post](#syntax) element, is used to create the post header.</span></span>

<span data-ttu-id="92d09-307">Varios elementos [formData](#syntax) pueden estar contenidos en un único nodo [uploadinfo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-307">Multiple [formdata](#syntax) elements may be contained under a single [uploadinfo](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-308">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-308">Syntax</span></span>


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-309">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-309">Attributes</span></span>



| <span data-ttu-id="92d09-310">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-310">Attribute</span></span> | <span data-ttu-id="92d09-311">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-311">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-312">name</span><span class="sxs-lookup"><span data-stu-id="92d09-312">name</span></span>      | <span data-ttu-id="92d09-313">Necesario.</span><span class="sxs-lookup"><span data-stu-id="92d09-313">Required.</span></span> <span data-ttu-id="92d09-314">Define el nombre de datos del formulario asociado a esta sección de la carga.</span><span class="sxs-lookup"><span data-stu-id="92d09-314">Defines the form data name associated with this section of the upload.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-315">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-315">Element Information</span></span>



| <span data-ttu-id="92d09-316">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-316">Parent Element</span></span>        | <span data-ttu-id="92d09-317">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-317">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="92d09-318">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-318">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-319">Ninguno</span><span class="sxs-lookup"><span data-stu-id="92d09-319">None</span></span>           |



 

## <a name="htmlui"></a><span data-ttu-id="92d09-320">htmlui</span><span class="sxs-lookup"><span data-stu-id="92d09-320">htmlui</span></span>

<span data-ttu-id="92d09-321">Dirección URL de la página HTML del servidor que se va a mostrar cuando se cierre el asistente.</span><span class="sxs-lookup"><span data-stu-id="92d09-321">The URL of the server-side HTML page to display when the wizard is closed.</span></span> <span data-ttu-id="92d09-322">Este elemento crea una entrada de página web favorita en el menú **Favoritos** si el elemento [favorito](#syntax) está ausente y se especifica el nombre descriptivo del sitio de carga.</span><span class="sxs-lookup"><span data-stu-id="92d09-322">This element creates a favorite webpage entry in the **Favorites** menu if the [favorite](#syntax) element is absent and the upload site's friendly name is specified.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-323">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-323">Syntax</span></span>


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-324">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-324">Attributes</span></span>



| <span data-ttu-id="92d09-325">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-325">Attribute</span></span> | <span data-ttu-id="92d09-326">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-326">Description</span></span>                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-327">href</span><span class="sxs-lookup"><span data-stu-id="92d09-327">href</span></span>      | <span data-ttu-id="92d09-328">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-328">Required.</span></span> <span data-ttu-id="92d09-329">Dirección URL de la página HTML del servidor que se va a mostrar cuando se cierre el asistente.</span><span class="sxs-lookup"><span data-stu-id="92d09-329">The URL of the server-side HTML page to display when the wizard is closed.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-330">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-330">Element Information</span></span>



| <span data-ttu-id="92d09-331">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-331">Parent Element</span></span>        | <span data-ttu-id="92d09-332">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-332">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="92d09-333">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-333">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-334">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-334">None.</span></span> <span data-ttu-id="92d09-335">Se permite el texto.</span><span class="sxs-lookup"><span data-stu-id="92d09-335">Text is allowed.</span></span> |



 

## <a name="imageproperty"></a><span data-ttu-id="92d09-336">imageproperty</span><span class="sxs-lookup"><span data-stu-id="92d09-336">imageproperty</span></span>

<span data-ttu-id="92d09-337">Especifica una propiedad de imagen relacionada con el archivo.</span><span class="sxs-lookup"><span data-stu-id="92d09-337">Specifies an image property relating to the file.</span></span> <span data-ttu-id="92d09-338">Varios elementos [imageproperty](#syntax) pueden estar contenidos en un solo nodo de [metadatos](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-338">Multiple [imageproperty](#syntax) elements may be contained under a single [metadata](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-339">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-339">Syntax</span></span>


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-340">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-340">Attributes</span></span>



| <span data-ttu-id="92d09-341">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-341">Attribute</span></span> | <span data-ttu-id="92d09-342">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-342">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="92d09-343">id</span><span class="sxs-lookup"><span data-stu-id="92d09-343">id</span></span>        | <span data-ttu-id="92d09-344">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-344">Required.</span></span> <span data-ttu-id="92d09-345">IDENTIFICADOR de la propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="92d09-345">The ID of the particular property.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-346">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-346">Element Information</span></span>



| <span data-ttu-id="92d09-347">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-347">Parent Element</span></span>      | <span data-ttu-id="92d09-348">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-348">Child Elements</span></span>         |
|---------------------|------------------------|
| [<span data-ttu-id="92d09-349">metadata</span><span class="sxs-lookup"><span data-stu-id="92d09-349">metadata</span></span>](#syntax) | <span data-ttu-id="92d09-350">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-350">None.</span></span> <span data-ttu-id="92d09-351">Se permite el texto.</span><span class="sxs-lookup"><span data-stu-id="92d09-351">Text is allowed.</span></span> |



 

## <a name="metadata"></a><span data-ttu-id="92d09-352">metadata</span><span class="sxs-lookup"><span data-stu-id="92d09-352">metadata</span></span>

<span data-ttu-id="92d09-353">Contenedor de elementos y texto que define los metadatos para el archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="92d09-353">A container for elements and text defining metadata for the particular file.</span></span> <span data-ttu-id="92d09-354">Varios elementos de [metadatos](#syntax) pueden estar contenidos en un solo nodo de [archivo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-354">Multiple [metadata](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-355">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-355">Syntax</span></span>


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-356">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-356">Attributes</span></span>

<span data-ttu-id="92d09-357">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-357">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="92d09-358">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-358">Element Information</span></span>



| <span data-ttu-id="92d09-359">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-359">Parent Element</span></span>  | <span data-ttu-id="92d09-360">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-360">Child Elements</span></span>           |
|-----------------|--------------------------|
| [<span data-ttu-id="92d09-361">file</span><span class="sxs-lookup"><span data-stu-id="92d09-361">file</span></span>](#syntax) | [<span data-ttu-id="92d09-362">imageproperty</span><span class="sxs-lookup"><span data-stu-id="92d09-362">imageproperty</span></span>](#syntax) |



 

## <a name="netplace"></a><span data-ttu-id="92d09-363">netplace</span><span class="sxs-lookup"><span data-stu-id="92d09-363">netplace</span></span>

<span data-ttu-id="92d09-364">Define el destino de un lugar de red que se crea en **mis sitios de red** cuando se completa la carga.</span><span class="sxs-lookup"><span data-stu-id="92d09-364">Defines the target for a network place that is created in **My Network Places** when the upload is complete.</span></span> <span data-ttu-id="92d09-365">La creación de un lugar de red se puede evitar a través del método [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="92d09-365">Creation of a network place can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-366">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-366">Syntax</span></span>


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-367">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-367">Attributes</span></span>



| <span data-ttu-id="92d09-368">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-368">Attribute</span></span> | <span data-ttu-id="92d09-369">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-369">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-370">comment</span><span class="sxs-lookup"><span data-stu-id="92d09-370">comment</span></span>   | <span data-ttu-id="92d09-371">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-371">Required.</span></span> <span data-ttu-id="92d09-372">El comentario que se muestra para el icono de ubicación de red cuando el cursor se sitúa sobre él.</span><span class="sxs-lookup"><span data-stu-id="92d09-372">The comment displayed for the network place icon when the cursor rests on it.</span></span>         |
| <span data-ttu-id="92d09-373">href</span><span class="sxs-lookup"><span data-stu-id="92d09-373">href</span></span>      | <span data-ttu-id="92d09-374">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-374">Required.</span></span> <span data-ttu-id="92d09-375">Dirección URL de la entrada de ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="92d09-375">The URL of the network place entry.</span></span>                                                   |
| <span data-ttu-id="92d09-376">name</span><span class="sxs-lookup"><span data-stu-id="92d09-376">name</span></span>      | <span data-ttu-id="92d09-377">Necesario.</span><span class="sxs-lookup"><span data-stu-id="92d09-377">Required.</span></span> <span data-ttu-id="92d09-378">Nombre del icono de ubicación de red que aparece en la carpeta **mis sitios de red** .</span><span class="sxs-lookup"><span data-stu-id="92d09-378">The name for the network place icon that appears in the **My Network Places** folder.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-379">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-379">Element Information</span></span>



| <span data-ttu-id="92d09-380">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-380">Parent Element</span></span>        | <span data-ttu-id="92d09-381">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-381">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="92d09-382">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-382">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-383">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-383">None.</span></span> <span data-ttu-id="92d09-384">Se permite el texto.</span><span class="sxs-lookup"><span data-stu-id="92d09-384">Text is allowed.</span></span> |



 

## <a name="post"></a><span data-ttu-id="92d09-385">post</span><span class="sxs-lookup"><span data-stu-id="92d09-385">post</span></span>

<span data-ttu-id="92d09-386">Dirección URL a la que se debe exponer el archivo.</span><span class="sxs-lookup"><span data-stu-id="92d09-386">URL to which the file should be posted.</span></span> <span data-ttu-id="92d09-387">El servicio agrega este elemento cuando la transferencia se realiza como una publicación de varias partes y, con [formData](#syntax), se usa para compilar el encabezado post.</span><span class="sxs-lookup"><span data-stu-id="92d09-387">This element is added by the service when the transfer is done as a multi-part post and, with [formdata](#syntax), is used to build the post header.</span></span> <span data-ttu-id="92d09-388">Si el servicio elige realizar la transferencia de archivos mediante World Wide Web la creación y control de versiones distribuidas (WebDAV), no debería agregar este elemento.</span><span class="sxs-lookup"><span data-stu-id="92d09-388">If the service chooses to perform the file transfer using World Wide Web Distributed Authoring and Versioning (WebDAV), it should not add this element.</span></span> <span data-ttu-id="92d09-389">Varios elementos [post](#syntax) pueden estar contenidos en un solo nodo [File](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-389">Multiple [post](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-390">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-390">Syntax</span></span>


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-391">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-391">Attributes</span></span>



| <span data-ttu-id="92d09-392">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-392">Attribute</span></span> | <span data-ttu-id="92d09-393">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-393">Description</span></span>                                                                    |
|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-394">nombreDeArchivo</span><span class="sxs-lookup"><span data-stu-id="92d09-394">filename</span></span>  | <span data-ttu-id="92d09-395">Opcional.</span><span class="sxs-lookup"><span data-stu-id="92d09-395">Optional.</span></span> <span data-ttu-id="92d09-396">Nombre del archivo expuesto.</span><span class="sxs-lookup"><span data-stu-id="92d09-396">The file name for the posted file.</span></span>                                   |
| <span data-ttu-id="92d09-397">href</span><span class="sxs-lookup"><span data-stu-id="92d09-397">href</span></span>      | <span data-ttu-id="92d09-398">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-398">Required.</span></span> <span data-ttu-id="92d09-399">Dirección URL de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="92d09-399">The URL of the destination folder.</span></span>                                   |
| <span data-ttu-id="92d09-400">name</span><span class="sxs-lookup"><span data-stu-id="92d09-400">name</span></span>      | <span data-ttu-id="92d09-401">Necesario.</span><span class="sxs-lookup"><span data-stu-id="92d09-401">Required.</span></span> <span data-ttu-id="92d09-402">Define el nombre de datos del formulario asociado a esta sección de la publicación.</span><span class="sxs-lookup"><span data-stu-id="92d09-402">Defines the form data name associated with this section of the post.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-403">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-403">Element Information</span></span>



| <span data-ttu-id="92d09-404">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-404">Parent Element</span></span>  | <span data-ttu-id="92d09-405">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-405">Child Elements</span></span>      |
|-----------------|---------------------|
| [<span data-ttu-id="92d09-406">file</span><span class="sxs-lookup"><span data-stu-id="92d09-406">file</span></span>](#syntax) | [<span data-ttu-id="92d09-407">formdata</span><span class="sxs-lookup"><span data-stu-id="92d09-407">formdata</span></span>](#syntax) |



 

## <a name="resize"></a><span data-ttu-id="92d09-408">resize</span><span class="sxs-lookup"><span data-stu-id="92d09-408">resize</span></span>

<span data-ttu-id="92d09-409">Define el escalado y la recompresión de un archivo de imagen en formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="92d09-409">Defines the scaling and recompression of an image file into JPEG format.</span></span> <span data-ttu-id="92d09-410">Si el archivo de código fuente ya está en formato JPEG y es menor o igual que el ancho y el alto especificados, no se ajusta.</span><span class="sxs-lookup"><span data-stu-id="92d09-410">If the source file is already in JPEG format and is less than or equal to the specified width and height, it is not sized.</span></span> <span data-ttu-id="92d09-411">Si el archivo de origen no es un archivo JPEG, se convierte.</span><span class="sxs-lookup"><span data-stu-id="92d09-411">If the source file is not a JPEG file, it is converted.</span></span> <span data-ttu-id="92d09-412">Se puede evitar el escalado, la recompresión y la conversión del archivo mediante el método [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="92d09-412">Scaling, recompression, and conversion of the file can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span> <span data-ttu-id="92d09-413">Varios elementos de [tamaño](#syntax) pueden estar contenidos en un solo nodo de [archivo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-413">Multiple [resize](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-414">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-414">Syntax</span></span>


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-415">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-415">Attributes</span></span>



| <span data-ttu-id="92d09-416">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-416">Attribute</span></span> | <span data-ttu-id="92d09-417">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-417">Description</span></span>                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-418">serie</span><span class="sxs-lookup"><span data-stu-id="92d09-418">cx</span></span>        | <span data-ttu-id="92d09-419">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-419">Required.</span></span> <span data-ttu-id="92d09-420">Ancho de la imagen, en píxeles, después de la carga.</span><span class="sxs-lookup"><span data-stu-id="92d09-420">The width of the image, in pixels, after uploading.</span></span> <span data-ttu-id="92d09-421">Si este valor es 0, **CX** se calcula a partir del valor **CY** para conservar las dimensiones relativas.</span><span class="sxs-lookup"><span data-stu-id="92d09-421">If this value is 0, then **cx** is calculated from the **cy** value to preserve relative dimensions.</span></span>  |
| <span data-ttu-id="92d09-422">cy</span><span class="sxs-lookup"><span data-stu-id="92d09-422">cy</span></span>        | <span data-ttu-id="92d09-423">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-423">Required.</span></span> <span data-ttu-id="92d09-424">Alto de la imagen, en píxeles, después de la carga.</span><span class="sxs-lookup"><span data-stu-id="92d09-424">The height of the image, in pixels, after uploading.</span></span> <span data-ttu-id="92d09-425">Si este valor es 0, **CY** se calcula a partir del valor de **CX** para conservar las dimensiones relativas.</span><span class="sxs-lookup"><span data-stu-id="92d09-425">If this value is 0, then **cy** is calculated from the **cx** value to preserve relative dimensions.</span></span> |
| <span data-ttu-id="92d09-426">calidad</span><span class="sxs-lookup"><span data-stu-id="92d09-426">quality</span></span>   | <span data-ttu-id="92d09-427">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-427">Required.</span></span> <span data-ttu-id="92d09-428">El valor de calidad JPEG, entre 0 y 100, y 100 es la calidad más alta.</span><span class="sxs-lookup"><span data-stu-id="92d09-428">The JPEG quality value, between 0 and 100, with 100 being the highest quality.</span></span>                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="92d09-429">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-429">Element Information</span></span>



| <span data-ttu-id="92d09-430">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-430">Parent Element</span></span>  | <span data-ttu-id="92d09-431">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-431">Child Elements</span></span> |
|-----------------|----------------|
| [<span data-ttu-id="92d09-432">file</span><span class="sxs-lookup"><span data-stu-id="92d09-432">file</span></span>](#syntax) | <span data-ttu-id="92d09-433">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-433">None.</span></span>          |



 

## <a name="successpage"></a><span data-ttu-id="92d09-434">successpage</span><span class="sxs-lookup"><span data-stu-id="92d09-434">successpage</span></span>

<span data-ttu-id="92d09-435">Especifica la página HTML del lado servidor que se va a mostrar si la carga se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="92d09-435">Specifies the server-side HTML page to display if the upload is successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-436">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-436">Syntax</span></span>


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-437">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-437">Attributes</span></span>



| <span data-ttu-id="92d09-438">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-438">Attribute</span></span> | <span data-ttu-id="92d09-439">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-439">Description</span></span>                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-440">href</span><span class="sxs-lookup"><span data-stu-id="92d09-440">href</span></span>      | <span data-ttu-id="92d09-441">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-441">Required.</span></span> <span data-ttu-id="92d09-442">Dirección URL de la página HTML del servidor que se va a mostrar si la carga se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="92d09-442">The URL of the server-side HTML page to display if the upload is successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-443">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-443">Element Information</span></span>



| <span data-ttu-id="92d09-444">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-444">Parent Element</span></span>        | <span data-ttu-id="92d09-445">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-445">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="92d09-446">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-446">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-447">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-447">None.</span></span> <span data-ttu-id="92d09-448">Se permite el texto.</span><span class="sxs-lookup"><span data-stu-id="92d09-448">Text is allowed.</span></span> |



 

## <a name="target"></a><span data-ttu-id="92d09-449">Destino</span><span class="sxs-lookup"><span data-stu-id="92d09-449">target</span></span>

<span data-ttu-id="92d09-450">Una carpeta de destino especificada en el formato UNC (Convención de nomenclatura universal) o como servidor WebDAV.</span><span class="sxs-lookup"><span data-stu-id="92d09-450">A destination folder specified in Universal Naming Convention (UNC) format or as a WebDAV server.</span></span> <span data-ttu-id="92d09-451">El servicio agrega este destino para especificar una carpeta de destino si la transferencia utiliza un protocolo WebDAV o de sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="92d09-451">The service adds this target to specify a destination folder if the transfer uses a WebDAV or file system protocol.</span></span> <span data-ttu-id="92d09-452">Si el servicio elige realizar la transferencia de archivos como una publicación de varias partes, no debe agregar este elemento.</span><span class="sxs-lookup"><span data-stu-id="92d09-452">If the service chooses to perform the file transfer as a multi-part post, it should not add this element.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-453">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-453">Syntax</span></span>


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-454">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-454">Attributes</span></span>



| <span data-ttu-id="92d09-455">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-455">Attribute</span></span> | <span data-ttu-id="92d09-456">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-456">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d09-457">href</span><span class="sxs-lookup"><span data-stu-id="92d09-457">href</span></span>      | <span data-ttu-id="92d09-458">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-458">Required.</span></span> <span data-ttu-id="92d09-459">Dirección URL de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="92d09-459">The URL of the destination folder.</span></span> <span data-ttu-id="92d09-460">Use el formulario **https://** para WebDAV o el formulario de **\\ \\ \\ recurso compartido de servidor** para UNC.</span><span class="sxs-lookup"><span data-stu-id="92d09-460">Use the **https://** form for WebDAV or the **\\\\server\\share** form for UNC.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-461">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-461">Element Information</span></span>



| <span data-ttu-id="92d09-462">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-462">Parent Element</span></span>        | <span data-ttu-id="92d09-463">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-463">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="92d09-464">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-464">uploadinfo</span></span>](#syntax) | <span data-ttu-id="92d09-465">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-465">None.</span></span> <span data-ttu-id="92d09-466">Se permite el texto.</span><span class="sxs-lookup"><span data-stu-id="92d09-466">Text is allowed.</span></span> |



 

## <a name="transfermanifest"></a><span data-ttu-id="92d09-467">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="92d09-467">transfermanifest</span></span>

<span data-ttu-id="92d09-468">Nodo primario del archivo de manifiesto de transferencia.</span><span class="sxs-lookup"><span data-stu-id="92d09-468">The parent node of the transfer manifest file.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-469">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-469">Syntax</span></span>


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-470">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-470">Attributes</span></span>

<span data-ttu-id="92d09-471">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92d09-471">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="92d09-472">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-472">Element Information</span></span>



| <span data-ttu-id="92d09-473">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-473">Parent Element</span></span> | <span data-ttu-id="92d09-474">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-474">Child Elements</span></span>                                                    |
|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="92d09-475">Ninguno</span><span class="sxs-lookup"><span data-stu-id="92d09-475">None</span></span>           | <span data-ttu-id="92d09-476">[FileList](#syntax), [folderList](#syntax), [uploadinfo](#syntax)</span><span class="sxs-lookup"><span data-stu-id="92d09-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span></span> |



 

## <a name="uploadinfo"></a><span data-ttu-id="92d09-477">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="92d09-477">uploadinfo</span></span>

<span data-ttu-id="92d09-478">Contenedor de elementos que proporcionan información del sitio de carga utilizado en la transacción.</span><span class="sxs-lookup"><span data-stu-id="92d09-478">A container for elements providing information from the upload site used in the transaction.</span></span> <span data-ttu-id="92d09-479">Varios elementos [uploadinfo](#syntax) pueden estar contenidos en un único nodo [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="92d09-479">Multiple [uploadinfo](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="92d09-480">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92d09-480">Syntax</span></span>


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="92d09-481">Atributos</span><span class="sxs-lookup"><span data-stu-id="92d09-481">Attributes</span></span>



| <span data-ttu-id="92d09-482">Atributo</span><span class="sxs-lookup"><span data-stu-id="92d09-482">Attribute</span></span>    | <span data-ttu-id="92d09-483">Descripción</span><span class="sxs-lookup"><span data-stu-id="92d09-483">Description</span></span>                                                                 |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="92d09-484">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="92d09-484">friendlyname</span></span> | <span data-ttu-id="92d09-485">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92d09-485">Required.</span></span> <span data-ttu-id="92d09-486">Un nombre descriptivo para el sitio web que se muestra en el asistente.</span><span class="sxs-lookup"><span data-stu-id="92d09-486">A friendly name for the website which is displayed in the wizard.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="92d09-487">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="92d09-487">Element Information</span></span>



| <span data-ttu-id="92d09-488">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="92d09-488">Parent Element</span></span>              | <span data-ttu-id="92d09-489">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92d09-489">Child Elements</span></span>                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92d09-490">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="92d09-490">transfermanifest</span></span>](#syntax) | <span data-ttu-id="92d09-491">[cancelledpage](#syntax), [failurepage](#syntax), [Favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span><span class="sxs-lookup"><span data-stu-id="92d09-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span></span> |



 

 

 



