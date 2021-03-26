---
description: En esta sección se describen las funciones de control de cadenas de Shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.
title: Funciones de control de cadenas de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002798"
---
# <a name="shell-string-handling-functions"></a><span data-ttu-id="f89fd-104">Funciones de control de cadenas de Shell</span><span class="sxs-lookup"><span data-stu-id="f89fd-104">Shell String Handling Functions</span></span>

<span data-ttu-id="f89fd-105">En esta sección se describen las funciones de control de cadenas de Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="f89fd-105">This section describes the Windows Shell string handling functions.</span></span> <span data-ttu-id="f89fd-106">Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="f89fd-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f89fd-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f89fd-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f89fd-108">Tema</span><span class="sxs-lookup"><span data-stu-id="f89fd-108">Topic</span></span></th>
<th><span data-ttu-id="f89fd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f89fd-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f89fd-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-111">Realiza una comparación entre dos caracteres.</span><span class="sxs-lookup"><span data-stu-id="f89fd-111">Performs a comparison between two characters.</span></span> <span data-ttu-id="f89fd-112">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-112">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-114">Recupera una cadena que se usa con websites al especificar las preferencias de idioma.</span><span class="sxs-lookup"><span data-stu-id="f89fd-114">Retrieves a string used with websites when specifying language preferences.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-116">Realiza una comparación con distinción entre mayúsculas y minúsculas de un número especificado de caracteres desde el principio de dos cadenas localizadas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-116">Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-118">Realiza una comparación sin distinción entre mayúsculas y minúsculas de un número especificado de caracteres desde el principio de dos cadenas localizadas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-118">Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-120">Compara un número especificado de caracteres desde el principio de dos cadenas localizadas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-120">Compares a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-122">Determina si un carácter representa un espacio.</span><span class="sxs-lookup"><span data-stu-id="f89fd-122">Determines whether a character represents a space.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-124">Extrae un recurso de texto especificado cuando se proporciona ese recurso en forma de cadena indirecta (una cadena que comienza con el símbolo "@").</span><span class="sxs-lookup"><span data-stu-id="f89fd-124">Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-126">Realiza una copia de una cadena en la memoria recién asignada.</span><span class="sxs-lookup"><span data-stu-id="f89fd-126">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-128">Anexa una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="f89fd-128">Appends one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f89fd-129">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="f89fd-129">Do not use.</span></span> <span data-ttu-id="f89fd-130">Vea la sección Comentarios para ver otras funciones.</span><span class="sxs-lookup"><span data-stu-id="f89fd-130">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-132">Copia y anexa caracteres de una cadena al final de otro.</span><span class="sxs-lookup"><span data-stu-id="f89fd-132">Copies and appends characters from one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f89fd-133">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="f89fd-133">Do not use.</span></span> <span data-ttu-id="f89fd-134">Vea la sección Comentarios para ver otras funciones.</span><span class="sxs-lookup"><span data-stu-id="f89fd-134">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-136">Concatena dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="f89fd-136">Concatenates two Unicode strings.</span></span> <span data-ttu-id="f89fd-137">Se usa cuando se requieren concatenaciones repetidas en el mismo búfer.</span><span class="sxs-lookup"><span data-stu-id="f89fd-137">Used when repeated concatenations to the same buffer are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-139">Busca en una cadena la primera aparición de un carácter que coincida con el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-139">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="f89fd-140">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-140">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-142">Busca en una cadena la primera aparición de un carácter que coincida con el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-142">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="f89fd-143">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-143">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-145">Busca en una cadena la primera aparición de un carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-145">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="f89fd-146">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-146">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-148">Busca en una cadena la primera aparición de un carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-148">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="f89fd-149">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-149">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-151">Compara dos cadenas para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="f89fd-151">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="f89fd-152">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-152">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-154">Compara cadenas mediante las reglas de intercalación de C en tiempo de ejecución (ASCII).</span><span class="sxs-lookup"><span data-stu-id="f89fd-154">Compares strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="f89fd-155">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-155">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-157">Compara dos cadenas para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="f89fd-157">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="f89fd-158">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-158">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-160">Compara dos cadenas mediante las reglas de intercalación en tiempo de ejecución de C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="f89fd-160">Compares two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="f89fd-161">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-161">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-163">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="f89fd-163">Compares two Unicode strings.</span></span> <span data-ttu-id="f89fd-164">Los dígitos de las cadenas se consideran como contenido numérico en lugar de texto.</span><span class="sxs-lookup"><span data-stu-id="f89fd-164">Digits in the strings are considered as numerical content rather than text.</span></span> <span data-ttu-id="f89fd-165">Esta prueba no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-165">This test is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-167">Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="f89fd-167">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="f89fd-168">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-168">The comparison is case-sensitive.</span></span> <span data-ttu-id="f89fd-169">La macro <strong>StrNCmp</strong> difiere de esta función solo en Name.</span><span class="sxs-lookup"><span data-stu-id="f89fd-169">The <strong>StrNCmp</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-171">Compara un número especificado de caracteres desde el principio de dos cadenas mediante las reglas de intercalación de C en tiempo de ejecución (ASCII).</span><span class="sxs-lookup"><span data-stu-id="f89fd-171">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="f89fd-172">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-172">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-174">Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="f89fd-174">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="f89fd-175">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-175">The comparison is not case-sensitive.</span></span> <span data-ttu-id="f89fd-176">La macro <strong>StrNCmpI</strong> difiere de esta función solo en Name.</span><span class="sxs-lookup"><span data-stu-id="f89fd-176">The <strong>StrNCmpI</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-178">Compara un número especificado de caracteres desde el principio de dos cadenas mediante las reglas de intercalación de C en tiempo de ejecución (ASCII).</span><span class="sxs-lookup"><span data-stu-id="f89fd-178">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="f89fd-179">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-179">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-181">Copia una cadena en otra.</span><span class="sxs-lookup"><span data-stu-id="f89fd-181">Copies one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f89fd-182">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="f89fd-182">Do not use.</span></span> <span data-ttu-id="f89fd-183">Vea la sección Comentarios para ver otras funciones.</span><span class="sxs-lookup"><span data-stu-id="f89fd-183">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-185">Copia un número especificado de caracteres desde el principio de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="f89fd-185">Copies a specified number of characters from the beginning of one string to another.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f89fd-186">No use esta función ni la macro <strong>StrNCpy</strong> .</span><span class="sxs-lookup"><span data-stu-id="f89fd-186">Do not use this function or the <strong>StrNCpy</strong> macro.</span></span> <span data-ttu-id="f89fd-187">Vea la sección Comentarios para ver otras funciones.</span><span class="sxs-lookup"><span data-stu-id="f89fd-187">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-189">Busca en una cadena la primera aparición de cualquiera de los grupos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f89fd-189">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="f89fd-190">El método de búsqueda distingue entre mayúsculas y minúsculas y el carácter <strong>nulo</strong> final se incluye en la coincidencia del patrón de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f89fd-190">The search method is case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-192">Busca en una cadena la primera aparición de cualquiera de los grupos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f89fd-192">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="f89fd-193">El método de búsqueda no distingue entre mayúsculas y minúsculas y el carácter <strong>nulo</strong> final se incluye en la coincidencia del patrón de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f89fd-193">The search method is not case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-195">Duplica una cadena.</span><span class="sxs-lookup"><span data-stu-id="f89fd-195">Duplicates a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-197">Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño.</span><span class="sxs-lookup"><span data-stu-id="f89fd-197">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-199">Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño.</span><span class="sxs-lookup"><span data-stu-id="f89fd-199">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="f89fd-200">Difiere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> en un tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="f89fd-200">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-202">Convierte un valor numérico en una cadena que representa el número en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño.</span><span class="sxs-lookup"><span data-stu-id="f89fd-202">Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="f89fd-203">Extiende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> ofreciendo la opción de redondear al dígito mostrado más próximo o descartar los dígitos no mostrados.</span><span class="sxs-lookup"><span data-stu-id="f89fd-203">Extends <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-205">Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño.</span><span class="sxs-lookup"><span data-stu-id="f89fd-205">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="f89fd-206">Difiere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> en un tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="f89fd-206">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-208">Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="f89fd-208">Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-210">Convierte un intervalo de tiempo, especificado en milisegundos, en una cadena.</span><span class="sxs-lookup"><span data-stu-id="f89fd-210">Converts a time interval, specified in milliseconds, to a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-212">Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="f89fd-212">Compares a specified number of characters from the beginning of two strings to determine if they are equal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-214">Anexa un número especificado de caracteres desde el principio de una cadena hasta el final de otro.</span><span class="sxs-lookup"><span data-stu-id="f89fd-214">Appends a specified number of characters from the beginning of one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f89fd-215">No use esta función ni la macro <strong>StrCatN</strong> .</span><span class="sxs-lookup"><span data-stu-id="f89fd-215">Do not use this function or the <strong>StrCatN</strong> macro.</span></span> <span data-ttu-id="f89fd-216">Vea la sección Comentarios para ver otras funciones.</span><span class="sxs-lookup"><span data-stu-id="f89fd-216">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-218">Busca en una cadena la primera aparición de un carácter incluido en un búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-218">Searches a string for the first occurrence of a character contained in a specified buffer.</span></span> <span data-ttu-id="f89fd-219">Esta búsqueda no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f89fd-219">This search does not include the terminating null character.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-221">Busca en una cadena la última aparición de un carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-221">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="f89fd-222">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-222">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-224">Busca en una cadena la última aparición de un carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-224">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="f89fd-225">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-225">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-227">Acepta una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> que contiene o apunta a una cadena y devuelve esa cadena como <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f89fd-227">Accepts a <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> that contains or points to a string, and returns that string as a <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-229">Convierte una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> en una cadena y coloca el resultado en un búfer.</span><span class="sxs-lookup"><span data-stu-id="f89fd-229">Converts an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-231">Toma una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> y devuelve un puntero a una cadena asignada que contiene el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="f89fd-231">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> and returns a pointer to an allocated string containing the display name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-233">Toma una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>, la convierte en una cadena y coloca el resultado en un búfer.</span><span class="sxs-lookup"><span data-stu-id="f89fd-233">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>, converts it to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-235">Busca la última aparición de una subcadena especificada en una cadena.</span><span class="sxs-lookup"><span data-stu-id="f89fd-235">Searches for the last occurrence of a specified substring within a string.</span></span> <span data-ttu-id="f89fd-236">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-236">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-238">Obtiene la longitud de una subcadena dentro de una cadena que se compone íntegramente de caracteres contenidos en un búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="f89fd-238">Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-240">Busca la primera aparición de una subcadena en una cadena.</span><span class="sxs-lookup"><span data-stu-id="f89fd-240">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="f89fd-241">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-241">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-243">Busca la primera aparición de una subcadena en una cadena.</span><span class="sxs-lookup"><span data-stu-id="f89fd-243">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="f89fd-244">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f89fd-244">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-246">Convierte una cadena que representa un valor decimal en un entero.</span><span class="sxs-lookup"><span data-stu-id="f89fd-246">Converts a string that represents a decimal value to an integer.</span></span> <span data-ttu-id="f89fd-247">La macro <strong>StrToLong</strong> es idéntica a esta función.</span><span class="sxs-lookup"><span data-stu-id="f89fd-247">The <strong>StrToLong</strong> macro is identical to this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-249">Convierte una cadena que representa un valor decimal o hexadecimal en un entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f89fd-249">Converts a string representing a decimal or hexadecimal value to a 64-bit integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-251">Convierte una cadena que representa un número decimal o hexadecimal en un entero.</span><span class="sxs-lookup"><span data-stu-id="f89fd-251">Converts a string representing a decimal or hexadecimal number to an integer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-253">Quita los caracteres inicial y final especificados de una cadena.</span><span class="sxs-lookup"><span data-stu-id="f89fd-253">Removes specified leading and trailing characters from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89fd-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-255">Toma una lista de argumentos de longitud variable y devuelve los valores de los argumentos como una cadena con formato de estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f89fd-255">Takes a variable-length argument list and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f89fd-256">No utilice esta función.</span><span class="sxs-lookup"><span data-stu-id="f89fd-256">Do not use this function.</span></span> <span data-ttu-id="f89fd-257">Vea la sección Comentarios para ver otras funciones.</span><span class="sxs-lookup"><span data-stu-id="f89fd-257">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89fd-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="f89fd-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="f89fd-259">Toma una lista de argumentos y devuelve los valores de los argumentos como una cadena con formato de estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f89fd-259">Takes a list of arguments and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f89fd-260">No utilice esta función.</span><span class="sxs-lookup"><span data-stu-id="f89fd-260">Do not use this function.</span></span> <span data-ttu-id="f89fd-261">Vea la sección Comentarios para ver otras funciones.</span><span class="sxs-lookup"><span data-stu-id="f89fd-261">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
