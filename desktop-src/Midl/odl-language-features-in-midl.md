---
title: Características del lenguaje ODL en MIDL
description: Atributos, palabras clave, instrucciones y directivas del lenguaje de descripción de objetos (ODL) que forman parte de MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL y ODL MIDL, características del lenguaje
- ODL MIDL , en MIDL
- ODL MIDL , atributos
- ODL MIDL , palabras clave
- ODL MIDL , instrucciones
- ODL MIDL , directivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db346a664ed7b8f7beeacfe73cc928a924befe10
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119790"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="719ab-109">Características del lenguaje ODL en MIDL</span><span class="sxs-lookup"><span data-stu-id="719ab-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="719ab-110">La Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="719ab-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="719ab-111">En su lugar, use el compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="719ab-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="719ab-112">En los temas siguientes se incluyen los atributos, palabras clave, instrucciones y directivas del Lenguaje de descripción de objetos (ODL) que ahora forman parte de la Lenguaje de definición de interfaz de Microsoft (MIDL):</span><span class="sxs-lookup"><span data-stu-id="719ab-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="719ab-113">Atributos de ODL</span><span class="sxs-lookup"><span data-stu-id="719ab-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="719ab-114">Palabras clave, instrucciones y directivas de ODL</span><span class="sxs-lookup"><span data-stu-id="719ab-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="719ab-115">Atributos de ODL</span><span class="sxs-lookup"><span data-stu-id="719ab-115">ODL Attributes</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="719ab-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-116">\[[**appobject**](appobject.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-117">\[[**Enlazable**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-117">\[[**bindable**](bindable.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-118">\[[**Control**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-118">\[[**control**](control.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-119">\[[**Predeterminado**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-119">\[[**default**](default.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-120">\[[**Defaultvalue**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-121">\[[**displaybind**](displaybind.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-122">\[[**Dllname**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-122">\[[**dllname**](dllname-str-.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-123">\[[**Doble**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-123">\[[**dual**](dual.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-124">\[[**Entrada**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-124">\[[**entry**](entry.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-125">\[[**Helpcontext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-125">\[[**helpcontext**](helpcontext.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-126">\[[**helpstring**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-126">\[[**helpstring**](helpstring.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-127">\[[**Helpfile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-127">\[[**helpfile**](helpfile.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-128">\[[**Oculto**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-128">\[[**hidden**](hidden.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-129">\[[**Id**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-129">\[[**id**](id.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-130">\[[**immediatebind**](immediatebind.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-131">\[[**En**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-131">\[[**in**](in.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-132">\[[**Lcid**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-132">\[[**lcid**](lcid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-133">\[[**Licencia**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-133">\[[**licensed**](licensed.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-134">\[[**nonextensible**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-134">\[[**nonextensible**](nonextensible.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-135">\[[**Odl**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-135">\[[**odl**](odl.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-136">\[[**oleautomation**](oleautomation.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-137">\[[**Opcional**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-137">\[[**optional**](optional.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-138">\[[**out**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-138">\[[**out**](out-idl.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-139">\[[**propget**](propget.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-140">\[[**propput**](propput.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-141">\[[**propputref**](propputref.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-142">\[[**Público**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-142">\[[**public**](public.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-143">\[[ **readonly**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-143">\[ [**readonly**](readonly.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-144">\[[**requestedit**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-144">\[[**requestedit**](requestedit.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-145">\[[**Restringido**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-145">\[[**restricted**](restricted.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-146">\[[**Retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-146">\[[**retval**](retval.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-147">\[[**Fuente**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-147">\[[**source**](source.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-148">\[[**Uuid**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-148">\[[**uuid**](uuid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-149">[**yrg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-149">[**vararg**](vararg.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="719ab-150">\[[**Versión**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-150">\[[**version**](version.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="719ab-151">Â</span><span class="sxs-lookup"><span data-stu-id="719ab-151">Â</span></span>
    :::column-end:::
:::row-end:::

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="719ab-152">Palabras clave, instrucciones y directivas de ODL</span><span class="sxs-lookup"><span data-stu-id="719ab-152">ODL Keywords, Statements, and Directives</span></span>

[<span data-ttu-id="719ab-153">**coclase**</span><span class="sxs-lookup"><span data-stu-id="719ab-153">**coclass**</span></span>](coclass.md)

[<span data-ttu-id="719ab-154">**Dispinterface**</span><span class="sxs-lookup"><span data-stu-id="719ab-154">**dispinterface**</span></span>](dispinterface.md)

[<span data-ttu-id="719ab-155">**Enum**</span><span class="sxs-lookup"><span data-stu-id="719ab-155">**enum**</span></span>](enum.md)

<span data-ttu-id="719ab-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="719ab-156">\[[**importlib**](importlib.md)\]</span></span>

[<span data-ttu-id="719ab-157">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="719ab-157">**interface**</span></span>](interface.md)

[<span data-ttu-id="719ab-158">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="719ab-158">**library**</span></span>](library.md)

[<span data-ttu-id="719ab-159">**Módulo**</span><span class="sxs-lookup"><span data-stu-id="719ab-159">**module**</span></span>](module.md)

[<span data-ttu-id="719ab-160">**Estructura**</span><span class="sxs-lookup"><span data-stu-id="719ab-160">**struct**</span></span>](struct.md)

[<span data-ttu-id="719ab-161">**Typedef**</span><span class="sxs-lookup"><span data-stu-id="719ab-161">**typedef**</span></span>](typedef.md)

[<span data-ttu-id="719ab-162">**Unión**</span><span class="sxs-lookup"><span data-stu-id="719ab-162">**union**</span></span>](union.md)

<span data-ttu-id="719ab-163">Para obtener información sobre cómo serializar tipos de automatización OLE, como **BSTR,** **VARIANT** y **SAFEARRAY**, vea [Serializar tipos de datos OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="719ab-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




