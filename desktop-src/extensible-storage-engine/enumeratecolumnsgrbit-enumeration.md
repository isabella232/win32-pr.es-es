---
description: 'Más información sobre: enumeración EnumerateColumnsGrbit'
title: Enumeración EnumerateColumnsGrbit
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717097"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a><span data-ttu-id="08b28-103">Enumeración EnumerateColumnsGrbit</span><span class="sxs-lookup"><span data-stu-id="08b28-103">EnumerateColumnsGrbit enumeration</span></span>

<span data-ttu-id="08b28-104">Opciones de JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="08b28-104">Options for JetEnumerateColumns.</span></span>

<span data-ttu-id="08b28-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="08b28-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="08b28-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08b28-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08b28-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08b28-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08b28-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08b28-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a><span data-ttu-id="08b28-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="08b28-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="08b28-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="08b28-110">Member name</span></span></th>
<th><span data-ttu-id="08b28-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="08b28-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="08b28-112">None</span><span class="sxs-lookup"><span data-stu-id="08b28-112">None</span></span></td>
<td><span data-ttu-id="08b28-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="08b28-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="08b28-114">EnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="08b28-114">EnumerateCompressOutput</span></span></td>
<td><span data-ttu-id="08b28-115">Al enumerar los valores de columna, todas las columnas para las que se recuperan todos los valores y que solo tienen un valor de columna que no es NULL pueden devolverse en un formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="08b28-115">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="08b28-116">El estado de estas columnas se establecerá en <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> y el tamaño del valor de la columna y la memoria que contiene el valor de la columna se devolverán directamente en la estructura <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="08b28-116">The status for such columns will be set to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> and the size of the column value and the memory containing the column value will be returned directly in the <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="08b28-117">No se garantiza que todas las columnas coincidentes se compriman de esta manera.</span><span class="sxs-lookup"><span data-stu-id="08b28-117">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="08b28-118">Consulte <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="08b28-118">See <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="08b28-119">EnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="08b28-119">EnumerateCopy</span></span></td>
<td><span data-ttu-id="08b28-120">Esta opción indica que los valores de columna modificados del registro se deben enumerar en lugar de los valores de columna originales.</span><span class="sxs-lookup"><span data-stu-id="08b28-120">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="08b28-121">Si un valor de columna no se ha modificado, se enumera el valor de la columna original.</span><span class="sxs-lookup"><span data-stu-id="08b28-121">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="08b28-122">De esta manera, se puede enumerar un valor de columna que todavía no se ha insertado o actualizado al insertar o actualizar un registro.</span><span class="sxs-lookup"><span data-stu-id="08b28-122">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span>
<p><span data-ttu-id="08b28-123">Esta opción es idéntica a <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span><span class="sxs-lookup"><span data-stu-id="08b28-123">This option is identical to <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="08b28-124">EnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="08b28-124">EnumerateIgnoreDefault</span></span></td>
<td><span data-ttu-id="08b28-125">Si una columna determinada no está presente en el registro, no se devolverá ningún valor de columna.</span><span class="sxs-lookup"><span data-stu-id="08b28-125">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="08b28-126">Normalmente, el valor predeterminado de la columna, si existe, se devolvería en este caso.</span><span class="sxs-lookup"><span data-stu-id="08b28-126">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="08b28-127">Se garantiza que, si la columna se establece en un valor distinto del valor predeterminado, se devolverá un valor diferente (es decir, si una columna con un valor predeterminado se establece explícitamente en NULL, se devolverá un valor NULL como valor para esa columna).</span><span class="sxs-lookup"><span data-stu-id="08b28-127">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to NULL then a NULL will be returned as the value for that column).</span></span> <span data-ttu-id="08b28-128">Aunque se solicite esta opción, sigue siendo posible ver un valor de columna que sea igual al valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="08b28-128">Even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="08b28-129">No se realiza ningún esfuerzo para quitar los valores de columna que coincidan con sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="08b28-129">No effort is made to remove column values that match their default values.</span></span> <span data-ttu-id="08b28-130">Es importante recordar que esta opción afecta a la salida de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> cuando se usa con EnumeratePresenceOnly o EnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="08b28-130">It is important to remember that this option affects the output of <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> when used with EnumeratePresenceOnly or EnumerateTaggedOnly.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="08b28-131">EnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="08b28-131">EnumeratePresenceOnly</span></span></td>
<td><span data-ttu-id="08b28-132">Si existe un valor no NULL para el valor de columna o columna solicitado, no se devuelven los datos asociados.</span><span class="sxs-lookup"><span data-stu-id="08b28-132">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="08b28-133">En su lugar, el estado asociado para ese valor de columna o columna se establecerá en <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span><span class="sxs-lookup"><span data-stu-id="08b28-133">Instead, the associated status for that column or column value will be set to <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span></span> <span data-ttu-id="08b28-134">Si el valor de la columna o columna es NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> se devolverá como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="08b28-134">If the column or column value is NULL then <a href="hh557250(v=exchg.10).md">ColumnNull</a> will be returned as usual.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="08b28-135">EnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="08b28-135">EnumerateTaggedOnly</span></span></td>
<td><span data-ttu-id="08b28-136">Al enumerar todos los valores de columna del registro (por ejemplo, es cuando numColumnids es cero), solo se devolverán los valores de columna etiquetada.</span><span class="sxs-lookup"><span data-stu-id="08b28-136">When enumerating all column values in the record (for example,that is when numColumnids is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="08b28-137">Esta opción no está permitida cuando se enumera una matriz de identificadores de columna específica.</span><span class="sxs-lookup"><span data-stu-id="08b28-137">This option is not allowed when enumerating a specific array of column IDs.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="08b28-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="08b28-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08b28-139">Referencia</span><span class="sxs-lookup"><span data-stu-id="08b28-139">Reference</span></span>

[<span data-ttu-id="08b28-140">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="08b28-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="08b28-141">EnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="08b28-141">EnumerateIgnoreUserDefinedDefault</span></span>](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[<span data-ttu-id="08b28-142">EnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="08b28-142">EnumerateInRecordOnly</span></span>](./windows7grbits.enumerateinrecordonly-field.md)
