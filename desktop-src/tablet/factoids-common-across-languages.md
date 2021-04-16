---
description: Un número de Factoids describe la entrada que es común a todos los reconocedores de lenguaje y no necesita tener formatos diferentes para distintos idiomas. En la tabla siguiente se enumeran los Factoids comunes a todos los lenguajes.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids común entre idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705705"
---
# <a name="factoids-common-across-languages"></a><span data-ttu-id="e2145-104">Factoids común entre idiomas</span><span class="sxs-lookup"><span data-stu-id="e2145-104">Factoids Common Across Languages</span></span>

<span data-ttu-id="e2145-105">Un número de Factoids describe la entrada que es común a todos los reconocedores de lenguaje y no necesita tener formatos diferentes para distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="e2145-105">A number of factoids describe input that is common to all language recognizers and need not have different formats for different languages.</span></span> <span data-ttu-id="e2145-106">En la tabla siguiente se enumeran los Factoids comunes a todos los lenguajes.</span><span class="sxs-lookup"><span data-stu-id="e2145-106">The following table lists factoids that are common across all languages.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2145-107">Factoid</span><span class="sxs-lookup"><span data-stu-id="e2145-107">Factoid</span></span></th>
<th><span data-ttu-id="e2145-108">Definición</span><span class="sxs-lookup"><span data-stu-id="e2145-108">Definition</span></span></th>
<th><span data-ttu-id="e2145-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e2145-109">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2145-110"><strong>Cifra</strong></span><span class="sxs-lookup"><span data-stu-id="e2145-110"><strong>Digit</strong></span></span></td>
<td><span data-ttu-id="e2145-111">Establece la diferencia para un solo dígito.</span><span class="sxs-lookup"><span data-stu-id="e2145-111">Sets bias for a single digit.</span></span> <span data-ttu-id="e2145-112">El reconocedor se sesga para devolver solo los dígitos únicos cuando se establece este valor de Factoid.</span><span class="sxs-lookup"><span data-stu-id="e2145-112">The recognizer is biased toward returning only single digits when this factoid is set.</span></span><br/></td>
<td><span data-ttu-id="e2145-113">0-9</span><span class="sxs-lookup"><span data-stu-id="e2145-113">0-9</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2145-114"><strong>Correo electrónico</strong></span><span class="sxs-lookup"><span data-stu-id="e2145-114"><strong>Email</strong></span></span></td>
<td><span data-ttu-id="e2145-115">Establece la diferencia de una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e2145-115">Sets bias for an email address.</span></span><br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2145-116"><strong>Web</strong></span><span class="sxs-lookup"><span data-stu-id="e2145-116"><strong>Web</strong></span></span></td>
<td><span data-ttu-id="e2145-117">Establece la diferencia para varios formatos de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e2145-117">Sets bias for various URL formats.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e2145-118">La configuración predeterminada del reconocedor incluye la Factoid <strong>Web</strong> .</span><span class="sxs-lookup"><span data-stu-id="e2145-118">The default settings for the recognizer include the <strong>Web</strong> factoid.</span></span> <span data-ttu-id="e2145-119">Por este motivo, es posible que no note una gran diferencia entre el Factoid <strong>Web</strong> y el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e2145-119">Because of this, you may not notice a large difference between the <strong>Web</strong> factoid and the default setting.</span></span> <span data-ttu-id="e2145-120">Sin embargo, la Factoid <strong>Web</strong> ayuda a eliminar los espacios entre las palabras de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e2145-120">However, the <strong>Web</strong> factoid does help eliminate spaces between words in a URL.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="e2145-121">http: \\ Microsoft.net</span><span class="sxs-lookup"><span data-stu-id="e2145-121">http:\\microsoft.net</span></span><br/> https://microsoft.us/<br/> <span data-ttu-id="e2145-122">https: \\ www.Microsoft.au </span><span class="sxs-lookup"><span data-stu-id="e2145-122">https:\\www.microsoft.au</span></span>\<br/> https://microsoft.com<br/> <span data-ttu-id="e2145-123">www.microsoft_world. com</span><span class="sxs-lookup"><span data-stu-id="e2145-123">www.microsoft_world.com</span></span><br/> <span data-ttu-id="e2145-124">www.microsoft.us </span><span class="sxs-lookup"><span data-stu-id="e2145-124">www.microsoft.us</span></span>\<br/> <span data-ttu-id="e2145-125">http: \\www.microsoft.com\myfile.htm</span><span class="sxs-lookup"><span data-stu-id="e2145-125">http:\\www.microsoft.com\myfile.htm</span></span><br/> <span data-ttu-id="e2145-126">http: \\www.microsoft.com\myfile.html</span><span class="sxs-lookup"><span data-stu-id="e2145-126">http:\\www.microsoft.com\myfile.html</span></span><br/> <span data-ttu-id="e2145-127">http: \\ www. Microsoft. com\myfile.asp</span><span class="sxs-lookup"><span data-stu-id="e2145-127">http:\\www.microsoft.com\myfile.asp</span></span><br/> <span data-ttu-id="e2145-128">http: \\ www.Microsoft.uk</span><span class="sxs-lookup"><span data-stu-id="e2145-128">http:\\www.microsoft.uk</span></span><br/> <span data-ttu-id="e2145-129">http: \\ www.Microsoft.info</span><span class="sxs-lookup"><span data-stu-id="e2145-129">http:\\www.microsoft.info</span></span><br/> <span data-ttu-id="e2145-130">www.microsoft.biz</span><span class="sxs-lookup"><span data-stu-id="e2145-130">www.microsoft.biz</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2145-131"><strong>Valor predeterminado</strong></span><span class="sxs-lookup"><span data-stu-id="e2145-131"><strong>Default</strong></span></span></td>
<td><span data-ttu-id="e2145-132">Devuelve el reconocedor a su configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2145-132">Returns the recognizer to its default settings.</span></span><br/></td>
<td><span data-ttu-id="e2145-133">La configuración predeterminada de Factoids para idiomas occidentales incluye el Diccionario del sistema, el Diccionario del usuario, varios signos de puntuación, y el <strong>Web</strong> y el <strong>número</strong> Factoids.</span><span class="sxs-lookup"><span data-stu-id="e2145-133">The default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the <strong>Web</strong> and <strong>Number</strong> factoids.</span></span><br/> <span data-ttu-id="e2145-134">La configuración predeterminada de Factoids para idiomas de Asia oriental incluye todos los caracteres admitidos por el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="e2145-134">The default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2145-135"><strong>None</strong></span><span class="sxs-lookup"><span data-stu-id="e2145-135"><strong>None</strong></span></span></td>
<td><span data-ttu-id="e2145-136">Deshabilita todos los Factoids, diccionarios y el modelo de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="e2145-136">Disables all factoids, dictionaries, and the language model.</span></span><br/></td>
<td><span data-ttu-id="e2145-137">Este Factoid solo debe usarse cuando no se desea que el reconocedor use ninguna regla o Diccionario de gramática, incluido el Diccionario del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2145-137">This factoid should be used only when you do not want the recognizer to use any grammar rules or dictionaries, including the system dictionary.</span></span> <span data-ttu-id="e2145-138">Este Factoid es útil para la entrada de cadenas aleatorias como códigos de producto.</span><span class="sxs-lookup"><span data-stu-id="e2145-138">This factoid is useful for input of random strings such as product codes.</span></span> <span data-ttu-id="e2145-139">No use la marca coerción con este Factoid.</span><span class="sxs-lookup"><span data-stu-id="e2145-139">Do not use the Coerce flag with this factoid.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




