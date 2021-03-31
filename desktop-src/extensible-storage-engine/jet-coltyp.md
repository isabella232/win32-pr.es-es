---
description: 'Más información acerca de: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912682"
---
# <a name="jet_coltyp"></a><span data-ttu-id="b4583-103">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="b4583-103">JET_COLTYP</span></span>


<span data-ttu-id="b4583-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b4583-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_coltyp"></a><span data-ttu-id="b4583-105">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="b4583-105">JET_COLTYP</span></span>

<span data-ttu-id="b4583-106">El **JET_COLTYP** grupo de constantes describen todos los tipos de columna posibles que se pueden encontrar en una tabla.</span><span class="sxs-lookup"><span data-stu-id="b4583-106">The **JET_COLTYP** group of constants describe all possible column types that can be found in a table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4583-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="b4583-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="b4583-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4583-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4583-109">JET_coltypNil</span><span class="sxs-lookup"><span data-stu-id="b4583-109">JET_coltypNil</span></span><br />
<span data-ttu-id="b4583-110">0</span><span class="sxs-lookup"><span data-stu-id="b4583-110">0</span></span></p></td>
<td><p><span data-ttu-id="b4583-111">Un tipo de columna no válido.</span><span class="sxs-lookup"><span data-stu-id="b4583-111">An invalid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-112">JET_coltypBit</span><span class="sxs-lookup"><span data-stu-id="b4583-112">JET_coltypBit</span></span><br />
<span data-ttu-id="b4583-113">1</span><span class="sxs-lookup"><span data-stu-id="b4583-113">1</span></span></p></td>
<td><p><span data-ttu-id="b4583-114">Un tipo de columna que permite tres valores: <strong>true</strong>, <strong>false</strong>o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4583-114">A column type that allows three values: <strong>True</strong>, <strong>False</strong>, or <strong>NULL</strong>.</span></span> <span data-ttu-id="b4583-115">Este tipo de columna tiene un byte de longitud y tiene un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="b4583-115">This type of column is one byte in length and is a fixed size.</span></span> <span data-ttu-id="b4583-116"><strong>False</strong> se ordena antes que <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4583-116"><strong>False</strong> sorts before <strong>True</strong>.</span></span> <span data-ttu-id="b4583-117">Tenga en cuenta que el tamaño de este tipo no coincide con el tamaño del tipo booleano Variant.</span><span class="sxs-lookup"><span data-stu-id="b4583-117">Note that the size of this type does not match the size of the variant Boolean type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-118">JET_coltypUnsignedByte</span><span class="sxs-lookup"><span data-stu-id="b4583-118">JET_coltypUnsignedByte</span></span><br />
<span data-ttu-id="b4583-119">2</span><span class="sxs-lookup"><span data-stu-id="b4583-119">2</span></span></p></td>
<td><p><span data-ttu-id="b4583-120">Entero de 1 byte sin signo que puede tomar valores entre 0 (cero) y 255.</span><span class="sxs-lookup"><span data-stu-id="b4583-120">A 1-byte unsigned integer that can take on values between 0 (zero) and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-121">JET_coltypShort</span><span class="sxs-lookup"><span data-stu-id="b4583-121">JET_coltypShort</span></span><br />
<span data-ttu-id="b4583-122">3</span><span class="sxs-lookup"><span data-stu-id="b4583-122">3</span></span></p></td>
<td><p><span data-ttu-id="b4583-123">Entero de 2 bytes con signo que puede tomar valores entre-32768 y 32767.</span><span class="sxs-lookup"><span data-stu-id="b4583-123">A 2-byte signed integer that can take on values between -32768 and 32767.</span></span> <span data-ttu-id="b4583-124">Los valores negativos se ordenan antes que los valores positivos.</span><span class="sxs-lookup"><span data-stu-id="b4583-124">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-125">JET_coltypLong</span><span class="sxs-lookup"><span data-stu-id="b4583-125">JET_coltypLong</span></span><br />
<span data-ttu-id="b4583-126">4</span><span class="sxs-lookup"><span data-stu-id="b4583-126">4</span></span></p></td>
<td><p><span data-ttu-id="b4583-127">Entero de 4 bytes con signo que puede tomar valores entre-2147483648 y 2147483647.</span><span class="sxs-lookup"><span data-stu-id="b4583-127">A 4-byte signed integer that can take on values between - 2147483648 and 2147483647.</span></span> <span data-ttu-id="b4583-128">Los valores negativos se ordenan antes que los valores positivos.</span><span class="sxs-lookup"><span data-stu-id="b4583-128">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-129">JET_coltypCurrency</span><span class="sxs-lookup"><span data-stu-id="b4583-129">JET_coltypCurrency</span></span><br />
<span data-ttu-id="b4583-130">5</span><span class="sxs-lookup"><span data-stu-id="b4583-130">5</span></span></p></td>
<td><p><span data-ttu-id="b4583-131">Entero de 8 bytes con signo que puede tomar valores entre-9223372036854775808 y 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="b4583-131">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="b4583-132">Los valores negativos se ordenan antes que los valores positivos.</span><span class="sxs-lookup"><span data-stu-id="b4583-132">Negative values sort before positive values.</span></span> <span data-ttu-id="b4583-133">Este tipo de columna es idéntico al tipo de divisa variante.</span><span class="sxs-lookup"><span data-stu-id="b4583-133">This column type is identical to the variant currency type.</span></span> <span data-ttu-id="b4583-134">Este tipo de columna también se puede utilizar como un entero de 8 bytes con signo nativo.</span><span class="sxs-lookup"><span data-stu-id="b4583-134">This column type can also be used as a native 8-byte signed integer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-135">JET_coltypIEEESingle</span><span class="sxs-lookup"><span data-stu-id="b4583-135">JET_coltypIEEESingle</span></span><br />
<span data-ttu-id="b4583-136">6</span><span class="sxs-lookup"><span data-stu-id="b4583-136">6</span></span></p></td>
<td><p><span data-ttu-id="b4583-137">Número de punto flotante de precisión sencilla (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="b4583-137">A single-precision (4-byte) floating point number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-138">JET_coltypIEEEDouble</span><span class="sxs-lookup"><span data-stu-id="b4583-138">JET_coltypIEEEDouble</span></span><br />
<span data-ttu-id="b4583-139">7</span><span class="sxs-lookup"><span data-stu-id="b4583-139">7</span></span></p></td>
<td><p><span data-ttu-id="b4583-140">Número de punto flotante de doble precisión (8 bytes).</span><span class="sxs-lookup"><span data-stu-id="b4583-140">A double-precision (8-byte) floating point number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-141">JET_coltypDateTime</span><span class="sxs-lookup"><span data-stu-id="b4583-141">JET_coltypDateTime</span></span><br />
<span data-ttu-id="b4583-142">8</span><span class="sxs-lookup"><span data-stu-id="b4583-142">8</span></span></p></td>
<td><p><span data-ttu-id="b4583-143">Número de punto flotante de doble precisión (8 bytes) que representa una fecha en días fraccionarios desde el año 1900.</span><span class="sxs-lookup"><span data-stu-id="b4583-143">A double-precision (8-byte) floating point number that represents a date in fractional days since the year 1900.</span></span> <span data-ttu-id="b4583-144">Este tipo de columna es idéntico al tipo de fecha Variant.</span><span class="sxs-lookup"><span data-stu-id="b4583-144">This column type is identical to the variant date type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-145">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="b4583-145">JET_coltypBinary</span></span><br />
<span data-ttu-id="b4583-146">9</span><span class="sxs-lookup"><span data-stu-id="b4583-146">9</span></span></p></td>
<td><p><span data-ttu-id="b4583-147">Columna binaria sin formato de longitud fija o variable que puede tener hasta 255 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="b4583-147">A fixed or variable length, raw binary column that can be up to 255 bytes in length.</span></span></p>
<p><span data-ttu-id="b4583-148">Este tipo de columna se puede usar para implementar un GUID si se configura como una columna binaria de 16 bytes de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="b4583-148">This column type can be used to implement a GUID if configured as a fixed length, 16-byte binary column.</span></span> <span data-ttu-id="b4583-149">La única ADVERTENCIA es que la ordenación relativa de los valores de un índice en una columna de este tipo no coincidirá con el orden relativo de la representación de la cadena del registro estándar de un GUID (es decir, &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</span><span class="sxs-lookup"><span data-stu-id="b4583-149">The only caveat is that the relative ordering of values in an index over such a column will not match the relative ordering of the standard registry-string rendering of a GUID (that is &quot;{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-150">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="b4583-150">JET_coltypText</span></span><br />
<span data-ttu-id="b4583-151">10</span><span class="sxs-lookup"><span data-stu-id="b4583-151">10</span></span></p></td>
<td><p><span data-ttu-id="b4583-152">Columna de texto de longitud fija o variable que puede tener hasta 255 caracteres ASCII de longitud o 127 caracteres Unicode de longitud.</span><span class="sxs-lookup"><span data-stu-id="b4583-152">A fixed or variable length text column that can be up to 255 ASCII characters in length or 127 Unicode characters in length.</span></span></p>
<p><span data-ttu-id="b4583-153">Todas las cadenas se almacenan como un número de caracteres contado.</span><span class="sxs-lookup"><span data-stu-id="b4583-153">All strings are stored as a counted number of characters.</span></span> <span data-ttu-id="b4583-154">No es necesario que las cadenas terminen en NULL.</span><span class="sxs-lookup"><span data-stu-id="b4583-154">The strings need not be null terminated.</span></span> <span data-ttu-id="b4583-155">Además, no es necesario que el recuento incluya un terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="b4583-155">Further, it is not necessary for the count to include a null terminator.</span></span> <span data-ttu-id="b4583-156">Por último, se pueden almacenar los caracteres nulos incrustados.</span><span class="sxs-lookup"><span data-stu-id="b4583-156">Finally, embedded null characters can be stored.</span></span></p>
<p><span data-ttu-id="b4583-157">Las cadenas ASCII siempre se tratan como no distinguir mayúsculas de minúsculas para la ordenación y la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b4583-157">ASCII strings are always treated as case insensitive for sorting and searching purposes.</span></span> <span data-ttu-id="b4583-158">Además, solo se tienen en cuenta los caracteres que preceden al primer carácter nulo (si existen) para la ordenación y la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b4583-158">Further, only the characters preceding the first null character (if any) are considered for sorting and searching.</span></span></p>
<p><span data-ttu-id="b4583-159">Las cadenas Unicode usan la API de Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> para crear claves de ordenación que se utilizan posteriormente para ordenar y buscar los datos.</span><span class="sxs-lookup"><span data-stu-id="b4583-159">Unicode strings use the Win32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> to create sort keys that are subsequently used for sorting and searching that data.</span></span> <span data-ttu-id="b4583-160">De forma predeterminada, las cadenas Unicode se consideran en la configuración regional de Inglés de EE. UU. y se ordenan y se buscan mediante las siguientes marcas de normalización: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="b4583-160">By default, Unicode strings are considered to be in the U.S. English locale and are sorted and searched using the following normalization flags: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="b4583-161">En Windows 2000, es posible personalizar estas marcas por índice para incluir también NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="b4583-161">In Windows 2000, it is possible to customize these flags per index to also include NORM_IGNORENONSPACE.</span></span> <span data-ttu-id="b4583-162">En Windows XP y versiones posteriores, es posible solicitar cualquier combinación de las siguientes marcas de normalización por índice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH y SORT_STRINGSORT.</span><span class="sxs-lookup"><span data-stu-id="b4583-162">In Windows XP and later releases, it is possible to request any combination of the following normalization flags per index: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH, and SORT_STRINGSORT.</span></span></p>
<p><span data-ttu-id="b4583-163">En todas las versiones, es posible personalizar la configuración regional por índice.</span><span class="sxs-lookup"><span data-stu-id="b4583-163">In all releases, it is possible to customize the locale per index.</span></span> <span data-ttu-id="b4583-164">Se puede usar cualquier configuración regional siempre que se haya instalado en el equipo el paquete de idioma adecuado.</span><span class="sxs-lookup"><span data-stu-id="b4583-164">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="b4583-165">Por último, se omiten por completo cualquier carácter nulo que se encuentre en una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="b4583-165">Finally, any null characters encountered in a Unicode string are completely ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-166">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="b4583-166">JET_coltypLongBinary</span></span><br />
<span data-ttu-id="b4583-167">11</span><span class="sxs-lookup"><span data-stu-id="b4583-167">11</span></span></p></td>
<td><p><span data-ttu-id="b4583-168">Columna binaria sin formato de longitud fija o variable que puede tener hasta 2147483647 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="b4583-168">A fixed or variable length, raw binary column that can be up to 2147483647 bytes in length.</span></span> <span data-ttu-id="b4583-169">Este tipo se considera un valor largo.</span><span class="sxs-lookup"><span data-stu-id="b4583-169">This type is considered to be a Long Value.</span></span> <span data-ttu-id="b4583-170">Un valor largo es especial porque puede ser grande y porque se puede tener acceso a él como un flujo.</span><span class="sxs-lookup"><span data-stu-id="b4583-170">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="b4583-171">De lo contrario, este tipo es idéntico a JET_coltypBinary.</span><span class="sxs-lookup"><span data-stu-id="b4583-171">This type is otherwise identical to JET_coltypBinary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-172">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="b4583-172">JET_coltypLongText</span></span><br />
<span data-ttu-id="b4583-173">12</span><span class="sxs-lookup"><span data-stu-id="b4583-173">12</span></span></p></td>
<td><p><span data-ttu-id="b4583-174">Columna de texto de longitud fija o variable que puede tener hasta 2147483647 caracteres ASCII de longitud o 1073741823 caracteres Unicode de longitud.</span><span class="sxs-lookup"><span data-stu-id="b4583-174">A fixed or variable length, text column that can be up to 2147483647 ASCII characters in length or 1073741823 Unicode characters in length.</span></span> <span data-ttu-id="b4583-175">Este tipo se considera un valor largo.</span><span class="sxs-lookup"><span data-stu-id="b4583-175">This type is considered to be a Long Value.</span></span> <span data-ttu-id="b4583-176">Un valor largo es especial porque puede ser grande y porque se puede tener acceso a él como un flujo.</span><span class="sxs-lookup"><span data-stu-id="b4583-176">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="b4583-177">De lo contrario, este tipo es idéntico a JET_coltypText.</span><span class="sxs-lookup"><span data-stu-id="b4583-177">This type is otherwise identical to JET_coltypText.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-178">JET_coltypSLV</span><span class="sxs-lookup"><span data-stu-id="b4583-178">JET_coltypSLV</span></span><br />
<span data-ttu-id="b4583-179">13</span><span class="sxs-lookup"><span data-stu-id="b4583-179">13</span></span></p></td>
<td><p><span data-ttu-id="b4583-180">Este tipo de columna está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b4583-180">This column type is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-181">JET_coltypUnsignedLong</span><span class="sxs-lookup"><span data-stu-id="b4583-181">JET_coltypUnsignedLong</span></span><br />
<span data-ttu-id="b4583-182">14</span><span class="sxs-lookup"><span data-stu-id="b4583-182">14</span></span></p></td>
<td><p><span data-ttu-id="b4583-183">Entero de 4 bytes sin signo que puede tomar valores entre 0 (cero) y 4294967295.</span><span class="sxs-lookup"><span data-stu-id="b4583-183">A 4-byte unsigned integer that can take on values between 0 (zero) and 4294967295.</span></span></p>
<p><span data-ttu-id="b4583-184"><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b4583-184"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-185">JET_coltypLongLong</span><span class="sxs-lookup"><span data-stu-id="b4583-185">JET_coltypLongLong</span></span><br />
<span data-ttu-id="b4583-186">15</span><span class="sxs-lookup"><span data-stu-id="b4583-186">15</span></span></p></td>
<td><p><span data-ttu-id="b4583-187">Entero de 8 bytes con signo que puede tomar valores entre-9223372036854775808 y 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="b4583-187">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="b4583-188">Los valores negativos se ordenan antes que los valores positivos.</span><span class="sxs-lookup"><span data-stu-id="b4583-188">Negative values sort before positive values.</span></span></p>
<p><span data-ttu-id="b4583-189"><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b4583-189"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-190">JET_coltypGUID</span><span class="sxs-lookup"><span data-stu-id="b4583-190">JET_coltypGUID</span></span><br />
<span data-ttu-id="b4583-191">16</span><span class="sxs-lookup"><span data-stu-id="b4583-191">16</span></span></p></td>
<td><p><span data-ttu-id="b4583-192">Columna binaria de 16 bytes de longitud fija que representa de forma nativa el tipo de datos GUID.</span><span class="sxs-lookup"><span data-stu-id="b4583-192">A fixed length 16 byte binary column that natively represents the GUID data type.</span></span> <span data-ttu-id="b4583-193">Los valores de las columnas GUID se ordenan de la misma manera en que esos valores se ordenarían como cadenas en formato estándar (es decir, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span><span class="sxs-lookup"><span data-stu-id="b4583-193">GUID column values sort in the same way that those values would sort as strings when in standard form (i.e. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span></span></p>
<p><span data-ttu-id="b4583-194"><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b4583-194"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-195">JET_coltypUnsignedShort</span><span class="sxs-lookup"><span data-stu-id="b4583-195">JET_coltypUnsignedShort</span></span><br />
<span data-ttu-id="b4583-196">17</span><span class="sxs-lookup"><span data-stu-id="b4583-196">17</span></span></p></td>
<td><p><span data-ttu-id="b4583-197">Entero de 2 bytes sin signo que puede tomar valores entre 0 y 65535.</span><span class="sxs-lookup"><span data-stu-id="b4583-197">A 2-byte unsigned integer that can take on values between 0 and 65535.</span></span></p>
<p><span data-ttu-id="b4583-198"><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b4583-198"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-199">JET_coltypMax</span><span class="sxs-lookup"><span data-stu-id="b4583-199">JET_coltypMax</span></span><br />
<span data-ttu-id="b4583-200">18</span><span class="sxs-lookup"><span data-stu-id="b4583-200">18</span></span></p></td>
<td><p><span data-ttu-id="b4583-201">Constante que describe el tipo de columna máximo (es decir, uno más allá del mayor válido) admitido por el motor.</span><span class="sxs-lookup"><span data-stu-id="b4583-201">A constant describing the maximum (that is, one beyond the largest valid) column type supported by the engine.</span></span></p>
<p><span data-ttu-id="b4583-202">Este valor debe usarse con cuidado porque cambiará a medida que se admitan nuevos tipos de columna.</span><span class="sxs-lookup"><span data-stu-id="b4583-202">This value should be used with care because it will change as new column types are supported.</span></span> <span data-ttu-id="b4583-203">Por ejemplo, tiene un valor literal diferente en Windows 2000 que en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b4583-203">For example, it has a different literal value on Windows 2000 than it does on Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="b4583-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4583-204">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4583-205"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b4583-205"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b4583-206">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b4583-206">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4583-207"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b4583-207"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b4583-208">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b4583-208">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4583-209"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b4583-209"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b4583-210">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b4583-210">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b4583-211">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b4583-211">See Also</span></span>

[<span data-ttu-id="b4583-212">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="b4583-212">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="b4583-213">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="b4583-213">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)
