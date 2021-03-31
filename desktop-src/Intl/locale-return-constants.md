---
description: '\_Constantes devueltas por la configuración regional \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Constantes de LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278610"
---
# <a name="locale_return-constants"></a><span data-ttu-id="8728a-103">\_Constantes devueltas por la configuración regional \*</span><span class="sxs-lookup"><span data-stu-id="8728a-103">LOCALE\_RETURN\* Constants</span></span>

<span data-ttu-id="8728a-104">En este tema se definen las \_ constantes de retorno de la configuración regional \* utilizadas por NLS.</span><span class="sxs-lookup"><span data-stu-id="8728a-104">This topic defines the LOCALE\_RETURN\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8728a-105">Value</span><span class="sxs-lookup"><span data-stu-id="8728a-105">Value</span></span></th>
<th><span data-ttu-id="8728a-106">Significado</span><span class="sxs-lookup"><span data-stu-id="8728a-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8728a-107">LOCALE_RETURN_GENITIVE_NAMES</span><span class="sxs-lookup"><span data-stu-id="8728a-107">LOCALE_RETURN_GENITIVE_NAMES</span></span></td>
<td><span data-ttu-id="8728a-108"><strong>Windows 7 y versiones posteriores:</strong> Recupere los nombres de genitivo de los meses, que son los nombres que se usan cuando los nombres de los meses se combinan con otros elementos.</span><span class="sxs-lookup"><span data-stu-id="8728a-108"><strong>Windows 7 and later:</strong> Retrieve the genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="8728a-109">Por ejemplo, en ucraniano, el equivalente de enero se escribe &quot; Січень &quot; cuando el mes se denomina por sí solo.</span><span class="sxs-lookup"><span data-stu-id="8728a-109">For example, in Ukrainian the equivalent of January is written &quot;Січень&quot; when the month is named alone.</span></span> <span data-ttu-id="8728a-110">Sin embargo, cuando el nombre del mes se usa en combinación, por ejemplo, en una fecha como el 5 de enero de 2003, se usa la forma genitivo del nombre.</span><span class="sxs-lookup"><span data-stu-id="8728a-110">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="8728a-111">En el ejemplo ucraniano, el nombre del mes en genitivo se muestra como &quot; 5 січня 2003 &quot; .</span><span class="sxs-lookup"><span data-stu-id="8728a-111">For the Ukrainian example, the genitive month name is displayed as &quot;5 січня 2003&quot;.</span></span> <span data-ttu-id="8728a-112">La lista de nombres de meses de genitivo comienza con enero y está delimitada por signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="8728a-112">The list of genitive month names begins with January and is semicolon-delimited.</span></span> <span data-ttu-id="8728a-113">Si no hay 13 meses, use un punto y coma en su lugar al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="8728a-113">If there is no 13th month, use a semicolon in its place at the end of the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8728a-114">Los nombres de mes de genitivo no existen en todos los idiomas.</span><span class="sxs-lookup"><span data-stu-id="8728a-114">Genitive month names do not exist in all languages.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8728a-115">LOCALE_RETURN_NUMBER</span><span class="sxs-lookup"><span data-stu-id="8728a-115">LOCALE_RETURN_NUMBER</span></span></td>
<td><span data-ttu-id="8728a-116"><strong>Windows Me/98, Windows NT 4,0 y versiones posteriores:</strong> Recupere un número.</span><span class="sxs-lookup"><span data-stu-id="8728a-116"><strong>Windows Me/98, Windows NT 4.0 and later:</strong> Retrieve a number.</span></span> <span data-ttu-id="8728a-117">Esta constante provoca que <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recuperen un valor como un número en lugar de como una cadena.</span><span class="sxs-lookup"><span data-stu-id="8728a-117">This constant causes <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> to retrieve a value as a number instead of as a string.</span></span> <span data-ttu-id="8728a-118">El búfer que recibe el valor debe ser al menos la longitud de un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="8728a-118">The buffer that receives the value must be at least the length of a DWORD value.</span></span> <span data-ttu-id="8728a-119">Esta constante se puede combinar con cualquier otra constante que tenga un nombre que comience por &quot; LOCALE_I &quot; .</span><span class="sxs-lookup"><span data-stu-id="8728a-119">This constant can be combined with any other constant having a name that begins with &quot;LOCALE_I&quot;.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




