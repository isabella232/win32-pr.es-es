---
description: 'Más información sobre: constantes de configuración máxima'
title: Constantes de configuración máxima
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908111"
---
# <a name="maximum-settings-constants"></a><span data-ttu-id="59c8e-103">Constantes de configuración máxima</span><span class="sxs-lookup"><span data-stu-id="59c8e-103">Maximum Settings Constants</span></span>


<span data-ttu-id="59c8e-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="59c8e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="maximum-settings-constants"></a><span data-ttu-id="59c8e-105">Constantes de configuración máxima</span><span class="sxs-lookup"><span data-stu-id="59c8e-105">Maximum Settings Constants</span></span>

<span data-ttu-id="59c8e-106">Estas constantes proporcionan la configuración máxima que se permite en los elementos de una base de datos ESE.</span><span class="sxs-lookup"><span data-stu-id="59c8e-106">These constants provide the maximum settings that are allowed on items in an ESE database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59c8e-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="59c8e-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="59c8e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="59c8e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-109">JET_BASE_NAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="59c8e-109">JET_BASE_NAME_LENGTH</span></span><br />
<span data-ttu-id="59c8e-110">3</span><span class="sxs-lookup"><span data-stu-id="59c8e-110">3</span></span></p></td>
<td><p><span data-ttu-id="59c8e-111">Establece la longitud del prefijo utilizado para asignar nombre a los archivos utilizados por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="59c8e-111">Sets the length for the prefix used to name files that are used by the database engine.</span></span> <span data-ttu-id="59c8e-112">Esta longitud es aplicable al nombre establecido para el parámetro del sistema <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</span><span class="sxs-lookup"><span data-stu-id="59c8e-112">This length is applicable to the name set for the <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> system parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-113">JET_MAX_COMPUTERNAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="59c8e-113">JET_MAX_COMPUTERNAME_LENGTH</span></span><br />
<span data-ttu-id="59c8e-114">15</span><span class="sxs-lookup"><span data-stu-id="59c8e-114">15</span></span></p></td>
<td><p><span data-ttu-id="59c8e-115">Establece la longitud máxima de <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span><span class="sxs-lookup"><span data-stu-id="59c8e-115">Sets the maximum length for <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-116">JET_cbBookmarkMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-116">JET_cbBookmarkMost</span></span><br />
<span data-ttu-id="59c8e-117">256</span><span class="sxs-lookup"><span data-stu-id="59c8e-117">256</span></span></p></td>
<td><p><span data-ttu-id="59c8e-118">Tamaño máximo predeterminado de un marcador.</span><span class="sxs-lookup"><span data-stu-id="59c8e-118">The default maximum size of a bookmark.</span></span> <span data-ttu-id="59c8e-119">Es válido cuando el tamaño de la clave se deja en su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="59c8e-119">This is valid when the key size is left at its default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-120">JET_cbBookmarkMostMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-120">JET_cbBookmarkMostMost</span></span><br />
<span data-ttu-id="59c8e-121">2000</span><span class="sxs-lookup"><span data-stu-id="59c8e-121">2000</span></span></p></td>
<td><p><span data-ttu-id="59c8e-122">El tamaño máximo de un marcador cuando esent está configurado para tener las claves más grandes posibles.</span><span class="sxs-lookup"><span data-stu-id="59c8e-122">The maximum size of a bookmark when esent is configured to have the largest keys possible.</span></span></p>
<p><span data-ttu-id="59c8e-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59c8e-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-124">JET_cbNameMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-124">JET_cbNameMost</span></span><br />
<span data-ttu-id="59c8e-125">64</span><span class="sxs-lookup"><span data-stu-id="59c8e-125">64</span></span></p></td>
<td><p><span data-ttu-id="59c8e-126">La longitud máxima de un objeto, una columna, un índice o un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="59c8e-126">The maximum length of a object, column, index, or property name.</span></span></p>
<p><span data-ttu-id="59c8e-127"><strong>Nota:</strong>  Si es Unicode, el valor es 128.</span><span class="sxs-lookup"><span data-stu-id="59c8e-127"><strong>Note</strong>  If Unicode, the value is 128.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-128">JET_cbFullNameMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-128">JET_cbFullNameMost</span></span><br />
<span data-ttu-id="59c8e-129">255</span><span class="sxs-lookup"><span data-stu-id="59c8e-129">255</span></span></p></td>
<td><p><span data-ttu-id="59c8e-130">La longitud máxima de una &quot; construcción Name.Name.Name... &quot;</span><span class="sxs-lookup"><span data-stu-id="59c8e-130">The maximum length of a &quot;name.name.name...&quot; construct.</span></span></p>
<p><span data-ttu-id="59c8e-131"><strong>Nota:</strong>  Si es Unicode, el valor es 510.</span><span class="sxs-lookup"><span data-stu-id="59c8e-131"><strong>Note</strong>  If Unicode, the value is 510.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-132">JET_cbColumnLVPageOverhead</span><span class="sxs-lookup"><span data-stu-id="59c8e-132">JET_cbColumnLVPageOverhead</span></span><br />
<span data-ttu-id="59c8e-133">82</span><span class="sxs-lookup"><span data-stu-id="59c8e-133">82</span></span></p></td>
<td><p><span data-ttu-id="59c8e-134">Este número se puede usar para calcular la cantidad máxima de un BLOB que el motor de base de datos puede almacenar en una sola página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="59c8e-134">This number can be used to compute the maximum amount of a BLOB that can be stored by the database engine on a single database page.</span></span> <span data-ttu-id="59c8e-135">La fórmula es el tamaño máximo = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</span><span class="sxs-lookup"><span data-stu-id="59c8e-135">The formula is max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</span></span></p>
<p><span data-ttu-id="59c8e-136">Este valor está ahora obsoleto.</span><span class="sxs-lookup"><span data-stu-id="59c8e-136">This value is now obsolete.</span></span> <span data-ttu-id="59c8e-137">El tamaño del fragmento de valor largo debe recuperarse con el parámetro JET_paramLVChunkSizeMost.</span><span class="sxs-lookup"><span data-stu-id="59c8e-137">The long-value chunk size should be retrieved with the JET_paramLVChunkSizeMost parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-138">JET_cbColumnMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-138">JET_cbColumnMost</span></span><br />
<span data-ttu-id="59c8e-139">255</span><span class="sxs-lookup"><span data-stu-id="59c8e-139">255</span></span></p></td>
<td><p><span data-ttu-id="59c8e-140">Tamaño máximo de los datos de columna que no son de valor largo.</span><span class="sxs-lookup"><span data-stu-id="59c8e-140">The maximum size of non-long-value column data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-141">JET_cbLVDefaultValueMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-141">JET_cbLVDefaultValueMost</span></span><br />
<span data-ttu-id="59c8e-142">255</span><span class="sxs-lookup"><span data-stu-id="59c8e-142">255</span></span></p></td>
<td><p><span data-ttu-id="59c8e-143">Tamaño máximo de un valor predeterminado de la columna de valor largo (LongBinary o LongText).</span><span class="sxs-lookup"><span data-stu-id="59c8e-143">The maximum size of a long-value (LongBinary or LongText) column default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-144">JET_cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-144">JET_cbKeyMost</span></span><br />
<span data-ttu-id="59c8e-145">255</span><span class="sxs-lookup"><span data-stu-id="59c8e-145">255</span></span></p></td>
<td><p><span data-ttu-id="59c8e-146">El tamaño máximo predeterminado de una clave de ordenación o de índice.</span><span class="sxs-lookup"><span data-stu-id="59c8e-146">The default maximum size of a sort or index key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-147">JET_cbKeyMostMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-147">JET_cbKeyMostMost</span></span><br />
<span data-ttu-id="59c8e-148">2000</span><span class="sxs-lookup"><span data-stu-id="59c8e-148">2000</span></span></p></td>
<td><p><span data-ttu-id="59c8e-149">Tamaño máximo configurable de una clave de ordenación o de índice para cualquier tamaño de página.</span><span class="sxs-lookup"><span data-stu-id="59c8e-149">The maximum configurable size of a sort or index key for any page size.</span></span> <span data-ttu-id="59c8e-150">(Consulte JET_INDEXCREATE2. cbKeyMost)</span><span class="sxs-lookup"><span data-stu-id="59c8e-150">(See JET_INDEXCREATE2.cbKeyMost)</span></span></p>
<p><span data-ttu-id="59c8e-151"><strong>Windows 7:</strong> JET_cbKeyMostMost se introduce en el sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59c8e-151"><strong>Windows 7:</strong> JET_cbKeyMostMost is introduced in the Windows 7 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-152">JET_cbKeyMost2KBytePage</span><span class="sxs-lookup"><span data-stu-id="59c8e-152">JET_cbKeyMost2KBytePage</span></span><br />
<span data-ttu-id="59c8e-153">500</span><span class="sxs-lookup"><span data-stu-id="59c8e-153">500</span></span></p></td>
<td><p><span data-ttu-id="59c8e-154">El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos con páginas de 2048 bytes.</span><span class="sxs-lookup"><span data-stu-id="59c8e-154">The maximum allowable maximum configurable size for an index key in a database using 2048 byte pages.</span></span> <span data-ttu-id="59c8e-155">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="59c8e-155">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="59c8e-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage se introduce en el sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59c8e-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage is introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-157">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="59c8e-157">JET_cbKeyMost4KBytePage</span></span><br />
<span data-ttu-id="59c8e-158">1000</span><span class="sxs-lookup"><span data-stu-id="59c8e-158">1000</span></span></p></td>
<td><p><span data-ttu-id="59c8e-159">El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos con páginas de 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="59c8e-159">The maximum allowable maximum configurable size for an index key in a database using 4096 byte pages.</span></span> <span data-ttu-id="59c8e-160">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="59c8e-160">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="59c8e-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59c8e-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-162">JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="59c8e-162">JET_cbKeyMost8KBytePage</span></span><br />
<span data-ttu-id="59c8e-163">2000</span><span class="sxs-lookup"><span data-stu-id="59c8e-163">2000</span></span></p></td>
<td><p><span data-ttu-id="59c8e-164">El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos con páginas de 8192 bytes.</span><span class="sxs-lookup"><span data-stu-id="59c8e-164">The maximum allowable maximum configurable size for an index key in a database using 8192 byte pages.</span></span> <span data-ttu-id="59c8e-165">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="59c8e-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="59c8e-166"><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage se introduce en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59c8e-166"><strong>Windows Vista:  </strong>JET_cbKeyMost8KBytePage is introduced in Windows Vista</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-167">JET_cbKeyMostMin</span><span class="sxs-lookup"><span data-stu-id="59c8e-167">JET_cbKeyMostMin</span></span><br />
<span data-ttu-id="59c8e-168">255</span><span class="sxs-lookup"><span data-stu-id="59c8e-168">255</span></span></p></td>
<td><p><span data-ttu-id="59c8e-169">El tamaño máximo permitido mínimo para una clave de índice.</span><span class="sxs-lookup"><span data-stu-id="59c8e-169">The minimum allowable maximum size for an index key.</span></span> <span data-ttu-id="59c8e-170">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="59c8e-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="59c8e-171"><strong>Windows Vista:  </strong> JET_cbKeyMostMin se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59c8e-171"><strong>Windows Vista:  </strong>JET_cbKeyMostMin is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-172">JET_cbLimitKeyMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-172">JET_cbLimitKeyMost</span></span><br />
<span data-ttu-id="59c8e-173">256</span><span class="sxs-lookup"><span data-stu-id="59c8e-173">256</span></span></p></td>
<td><p><span data-ttu-id="59c8e-174">El tamaño máximo de la clave cuando se forma la clave mediante un límite <em>grbit</em>, como JET_bitStrLimit, que se usa en la función <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="59c8e-174">The maximum key size when the key is formed by using a limit <em>grbit</em>, such as JET_bitStrLimit, which is used in the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-175">JET_cbPrimaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-175">JET_cbPrimaryKeyMost</span></span><br />
<span data-ttu-id="59c8e-176">255</span><span class="sxs-lookup"><span data-stu-id="59c8e-176">255</span></span></p></td>
<td><p><span data-ttu-id="59c8e-177">Tamaño máximo del índice principal.</span><span class="sxs-lookup"><span data-stu-id="59c8e-177">The maximum size of the primary index.</span></span> <span data-ttu-id="59c8e-178">Esto está ahora obsoleto.</span><span class="sxs-lookup"><span data-stu-id="59c8e-178">This is now obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-179">JET_cbSecondaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-179">JET_cbSecondaryKeyMost</span></span><br />
<span data-ttu-id="59c8e-180">255</span><span class="sxs-lookup"><span data-stu-id="59c8e-180">255</span></span></p></td>
<td><p><span data-ttu-id="59c8e-181">Tamaño máximo del índice secundario.</span><span class="sxs-lookup"><span data-stu-id="59c8e-181">The maximum size of the secondary index.</span></span> <span data-ttu-id="59c8e-182">Esto está ahora obsoleto.</span><span class="sxs-lookup"><span data-stu-id="59c8e-182">This is now obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-183">JET_ccolKeyMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-183">JET_ccolKeyMost</span></span><br />
<span data-ttu-id="59c8e-184">12</span><span class="sxs-lookup"><span data-stu-id="59c8e-184">12</span></span></p></td>
<td><p><span data-ttu-id="59c8e-185">Número máximo de componentes en una clave de ordenación o de índice.</span><span class="sxs-lookup"><span data-stu-id="59c8e-185">The maximum number of components in a sort or index key.</span></span></p>
<p><span data-ttu-id="59c8e-186"><strong>Windows Vista:  </strong> En Windows Vista y versiones posteriores de Windows, el valor es 16.</span><span class="sxs-lookup"><span data-stu-id="59c8e-186"><strong>Windows Vista:  </strong>In Windows Vista and later versions of Windows the value is 16.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-187">JET_ccolMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-187">JET_ccolMost</span></span><br />
<span data-ttu-id="59c8e-188">0x0000fee0</span><span class="sxs-lookup"><span data-stu-id="59c8e-188">0x0000fee0</span></span></p></td>
<td><p><span data-ttu-id="59c8e-189">Número máximo de columnas permitidas en una tabla.</span><span class="sxs-lookup"><span data-stu-id="59c8e-189">The maximum number of columns allowed in a table.</span></span></p>
<p><span data-ttu-id="59c8e-190"><strong>Windows XP:  </strong> El valor 0x0000fee0 se utiliza en Windows XP y versiones posteriores y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="59c8e-190"><strong>Windows XP:  </strong>The value 0x0000fee0 is used in Windows XP and later and later versions of Windows</span></span></p>
<p><span data-ttu-id="59c8e-191"><strong>Windows 2000:  </strong> El valor 0x00007ffe se utiliza en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="59c8e-191"><strong>Windows 2000:  </strong>The value 0x00007ffe is used in Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-192">JET_ccolFixedMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-192">JET_ccolFixedMost</span></span><br />
<span data-ttu-id="59c8e-193">detención</span><span class="sxs-lookup"><span data-stu-id="59c8e-193">0x0000007f</span></span></p></td>
<td><p><span data-ttu-id="59c8e-194">Número máximo de columnas fijas permitidas en una tabla; actualmente, 127.</span><span class="sxs-lookup"><span data-stu-id="59c8e-194">The maximum number of fixed columns allowed in a table, currently 127.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-195">JET_ccolVarMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-195">JET_ccolVarMost</span></span><br />
<span data-ttu-id="59c8e-196">0x00000080</span><span class="sxs-lookup"><span data-stu-id="59c8e-196">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="59c8e-197">Número máximo de columnas de longitud variable que se pueden incluir en una tabla, actualmente 128.</span><span class="sxs-lookup"><span data-stu-id="59c8e-197">The maximum number of variable-length columns that can be contained in a table, currently 128.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-198">JET_ccolTaggedMost</span><span class="sxs-lookup"><span data-stu-id="59c8e-198">JET_ccolTaggedMost</span></span><br />
<span data-ttu-id="59c8e-199">(JET_ccolMost-0x000000ff)</span><span class="sxs-lookup"><span data-stu-id="59c8e-199">( JET_ccolMost - 0x000000ff )</span></span></p></td>
<td><p><span data-ttu-id="59c8e-200">Número máximo de columnas etiquetadas que se pueden incluir en una tabla, actualmente 64993.</span><span class="sxs-lookup"><span data-stu-id="59c8e-200">The maximum number of tagged columns that can be contained in a table, currently 64993.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="59c8e-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c8e-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="59c8e-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="59c8e-203">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="59c8e-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c8e-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="59c8e-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="59c8e-205">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="59c8e-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c8e-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="59c8e-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="59c8e-207">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="59c8e-207">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

