---
title: Características del lenguaje ODL en MIDL
description: Atributos, palabras clave, instrucciones y directivas del lenguaje de descripción de objetos (ODL) que forman parte de MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL y ODL (MIDL), características del lenguaje
- ODL (MIDL), en MIDL
- ODL (MIDL), atributos
- ODL (MIDL), palabras clave
- ODL (MIDL), instrucciones
- ODL (MIDL), directivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903767"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="858b2-109">Características del lenguaje ODL en MIDL</span><span class="sxs-lookup"><span data-stu-id="858b2-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="858b2-110">La herramienta Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="858b2-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="858b2-111">En su lugar, utilice el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="858b2-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="858b2-112">En los temas siguientes se enumeran los atributos, las palabras clave, las instrucciones y las directivas del lenguaje de descripción de objetos (ODL) que ahora forman parte del Lenguaje de definición de interfaz de Microsoft (MIDL):</span><span class="sxs-lookup"><span data-stu-id="858b2-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="858b2-113">ODL (atributos)</span><span class="sxs-lookup"><span data-stu-id="858b2-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="858b2-114">Palabras clave, instrucciones y directivas ODL</span><span class="sxs-lookup"><span data-stu-id="858b2-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="858b2-115">ODL (atributos)</span><span class="sxs-lookup"><span data-stu-id="858b2-115">ODL Attributes</span></span>



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="858b2-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-116">\[[**appobject**](appobject.md)\]</span></span>         | <span data-ttu-id="858b2-117">\[[**enlazable**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-117">\[[**bindable**](bindable.md)\]</span></span>       |
| <span data-ttu-id="858b2-118">\[[**control**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-118">\[[**control**](control.md)\]</span></span>             | <span data-ttu-id="858b2-119">\[[**predeterminada**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-119">\[[**default**](default.md)\]</span></span>         |
| <span data-ttu-id="858b2-120">\[[**DefaultValue**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>   | <span data-ttu-id="858b2-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-121">\[[**displaybind**](displaybind.md)\]</span></span> |
| <span data-ttu-id="858b2-122">\[[**DllName**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-122">\[[**dllname**](dllname-str-.md)\]</span></span>        | <span data-ttu-id="858b2-123">\[[**BI**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-123">\[[**dual**](dual.md)\]</span></span>               |
| <span data-ttu-id="858b2-124">\[[**movimientos**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-124">\[[**entry**](entry.md)\]</span></span>                 | <span data-ttu-id="858b2-125">\[[**HelpContext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-125">\[[**helpcontext**](helpcontext.md)\]</span></span> |
| <span data-ttu-id="858b2-126">\[[**HelpString**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-126">\[[**helpstring**](helpstring.md)\]</span></span>       | <span data-ttu-id="858b2-127">\[[**HelpFile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-127">\[[**helpfile**](helpfile.md)\]</span></span>       |
| <span data-ttu-id="858b2-128">\[[**plusvalía**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-128">\[[**hidden**](hidden.md)\]</span></span>               | <span data-ttu-id="858b2-129">\[[**sesión**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-129">\[[**id**](id.md)\]</span></span>                   |
| <span data-ttu-id="858b2-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-130">\[[**immediatebind**](immediatebind.md)\]</span></span> | <span data-ttu-id="858b2-131">\[[**de**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-131">\[[**in**](in.md)\]</span></span>                   |
| <span data-ttu-id="858b2-132">\[[**LCID**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-132">\[[**lcid**](lcid.md)\]</span></span>                   | <span data-ttu-id="858b2-133">\[[**bajo**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-133">\[[**licensed**](licensed.md)\]</span></span>       |
| <span data-ttu-id="858b2-134">\[[**nonextensible (**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-134">\[[**nonextensible**](nonextensible.md)\]</span></span> | <span data-ttu-id="858b2-135">\[[**ODL**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-135">\[[**odl**](odl.md)\]</span></span>                 |
| <span data-ttu-id="858b2-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-136">\[[**oleautomation**](oleautomation.md)\]</span></span> | <span data-ttu-id="858b2-137">\[[**opta**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-137">\[[**optional**](optional.md)\]</span></span>       |
| <span data-ttu-id="858b2-138">\[[**enuncia**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-138">\[[**out**](out-idl.md)\]</span></span>                 | <span data-ttu-id="858b2-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-139">\[[**propget**](propget.md)\]</span></span>         |
| <span data-ttu-id="858b2-140">\[[**PROPPUT**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-140">\[[**propput**](propput.md)\]</span></span>             | <span data-ttu-id="858b2-141">\[[**PROPPUTREF**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-141">\[[**propputref**](propputref.md)\]</span></span>   |
| <span data-ttu-id="858b2-142">\[[**pública**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-142">\[[**public**](public.md)\]</span></span>               | <span data-ttu-id="858b2-143">\[[ **solo lectura**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-143">\[ [**readonly**](readonly.md)\]</span></span>      |
| <span data-ttu-id="858b2-144">\[[**requestedit**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-144">\[[**requestedit**](requestedit.md)\]</span></span>     | <span data-ttu-id="858b2-145">\[[**Restrict**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-145">\[[**restricted**](restricted.md)\]</span></span>   |
| <span data-ttu-id="858b2-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-146">\[[**retval**](retval.md)\]</span></span>               | <span data-ttu-id="858b2-147">\[[**fuentes**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-147">\[[**source**](source.md)\]</span></span>           |
| <span data-ttu-id="858b2-148">\[[**UUID**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-148">\[[**uuid**](uuid.md)\]</span></span>                   | <span data-ttu-id="858b2-149">[**vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-149">[**vararg**](vararg.md)\]</span></span>             |
| <span data-ttu-id="858b2-150">\[[**Versión**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-150">\[[**version**](version.md)\]</span></span>             | <span data-ttu-id="858b2-151">Ti</span><span class="sxs-lookup"><span data-stu-id="858b2-151">Â</span></span>                                      |



 

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="858b2-152">Palabras clave, instrucciones y directivas ODL</span><span class="sxs-lookup"><span data-stu-id="858b2-152">ODL Keywords, Statements, and Directives</span></span>



|                                        |
|----------------------------------------|
| [<span data-ttu-id="858b2-153">**coclase**</span><span class="sxs-lookup"><span data-stu-id="858b2-153">**coclass**</span></span>](coclass.md)             |
| [<span data-ttu-id="858b2-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="858b2-154">**dispinterface**</span></span>](dispinterface.md) |
| [<span data-ttu-id="858b2-155">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="858b2-155">**enum**</span></span>](enum.md)                   |
| <span data-ttu-id="858b2-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="858b2-156">\[[**importlib**](importlib.md)\]</span></span>     |
| [<span data-ttu-id="858b2-157">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="858b2-157">**interface**</span></span>](interface.md)         |
| [<span data-ttu-id="858b2-158">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="858b2-158">**library**</span></span>](library.md)             |
| [<span data-ttu-id="858b2-159">**destina**</span><span class="sxs-lookup"><span data-stu-id="858b2-159">**module**</span></span>](module.md)               |
| [<span data-ttu-id="858b2-160">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="858b2-160">**struct**</span></span>](struct.md)               |
| [<span data-ttu-id="858b2-161">**typedef**</span><span class="sxs-lookup"><span data-stu-id="858b2-161">**typedef**</span></span>](typedef.md)             |
| [<span data-ttu-id="858b2-162">**Unión**</span><span class="sxs-lookup"><span data-stu-id="858b2-162">**union**</span></span>](union.md)                 |



 

<span data-ttu-id="858b2-163">Para obtener información sobre cómo calcular las referencias de los tipos de automatización OLE, como **BSTR**, **Variant** y **SAFEARRAY**, vea [serialización de tipos de datos OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="858b2-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




