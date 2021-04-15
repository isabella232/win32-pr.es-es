---
description: 'Más información sobre: enumeración SetColumnGrbit'
title: Enumeración SetColumnGrbit
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497674"
---
# <a name="setcolumngrbit-enumeration"></a><span data-ttu-id="85c73-103">Enumeración SetColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="85c73-103">SetColumnGrbit enumeration</span></span>

<span data-ttu-id="85c73-104">Opciones de JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="85c73-104">Options for JetSetColumn.</span></span>

<span data-ttu-id="85c73-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="85c73-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="85c73-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85c73-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85c73-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="85c73-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85c73-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85c73-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
```

## <a name="members"></a><span data-ttu-id="85c73-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="85c73-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="85c73-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="85c73-110">Member name</span></span></th>
<th><span data-ttu-id="85c73-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c73-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="85c73-112">None</span><span class="sxs-lookup"><span data-stu-id="85c73-112">None</span></span></td>
<td><span data-ttu-id="85c73-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="85c73-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="85c73-114">AppendLV</span><span class="sxs-lookup"><span data-stu-id="85c73-114">AppendLV</span></span></td>
<td><span data-ttu-id="85c73-115">Esta opción se utiliza para anexar datos a una columna de tipo JET_coltypLongText o JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="85c73-115">This option is used to append data to a column of type JET_coltypLongText or JET_coltypLongBinary.</span></span> <span data-ttu-id="85c73-116">Se puede lograr el mismo comportamiento determinando el tamaño del valor Long existente y especificando ibLongValue en psetinfo.</span><span class="sxs-lookup"><span data-stu-id="85c73-116">The same behavior can be achieved by determining the size of the existing long value and specifying ibLongValue in psetinfo.</span></span> <span data-ttu-id="85c73-117">Sin embargo, es más sencillo usar esta grbit, ya que no es necesario conocer el tamaño del valor de la columna existente.</span><span class="sxs-lookup"><span data-stu-id="85c73-117">However, its simpler to use this grbit since knowing the size of the existing column value is not necessary.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="85c73-118">OverwriteLV</span><span class="sxs-lookup"><span data-stu-id="85c73-118">OverwriteLV</span></span></td>
<td><span data-ttu-id="85c73-119">Esta opción se usa para reemplazar el valor Long existente con los datos proporcionados recientemente.</span><span class="sxs-lookup"><span data-stu-id="85c73-119">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="85c73-120">Cuando se usa esta opción, es como si el valor Long existente se hubiera establecido en la longitud 0 (cero) antes de establecer los datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="85c73-120">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="85c73-121">RevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="85c73-121">RevertToDefaultValue</span></span></td>
<td><span data-ttu-id="85c73-122">Esta opción solo es aplicable para columnas etiquetadas, dispersas o con varios valores.</span><span class="sxs-lookup"><span data-stu-id="85c73-122">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="85c73-123">Hace que la columna devuelva el valor de columna predeterminado en operaciones de recuperación de columna posteriores.</span><span class="sxs-lookup"><span data-stu-id="85c73-123">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="85c73-124">Se quitan todos los valores de columna existentes.</span><span class="sxs-lookup"><span data-stu-id="85c73-124">All existing column values are removed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="85c73-125">SeparateLV</span><span class="sxs-lookup"><span data-stu-id="85c73-125">SeparateLV</span></span></td>
<td><span data-ttu-id="85c73-126">Esta opción se usa para forzar un valor largo, las columnas de tipo JET_coltyp. LongText o JET_coltyp. LongBinary, que se almacenará de forma independiente del resto de datos de registro.</span><span class="sxs-lookup"><span data-stu-id="85c73-126">This option is used to force a long value, columns of type JET_coltyp.LongText or JET_coltyp.LongBinary, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="85c73-127">Esto ocurre normalmente cuando el tamaño del valor Long impide que se almacene con los datos de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="85c73-127">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="85c73-128">Sin embargo, esta opción se puede usar para forzar el almacenamiento del valor largo por separado.</span><span class="sxs-lookup"><span data-stu-id="85c73-128">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="85c73-129">Tenga en cuenta que no se puede forzar la separación de los valores Long de cuatro bytes de menor tamaño.</span><span class="sxs-lookup"><span data-stu-id="85c73-129">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="85c73-130">En estos casos, se omite la opción.</span><span class="sxs-lookup"><span data-stu-id="85c73-130">In such cases, the option is ignored.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="85c73-131">SizeLV</span><span class="sxs-lookup"><span data-stu-id="85c73-131">SizeLV</span></span></td>
<td><span data-ttu-id="85c73-132">Esta opción se usa para interpretar el búfer de entrada como un número entero de bytes que se establecerá como la longitud del valor largo descrito por el columnid determinado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="85c73-132">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="85c73-133">Si el tamaño dado es mayor que el valor de columna existente, la columna se extenderá con 0s.</span><span class="sxs-lookup"><span data-stu-id="85c73-133">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="85c73-134">Si el tamaño es menor que el valor de la columna existente, el valor se truncará.</span><span class="sxs-lookup"><span data-stu-id="85c73-134">If the size is smaller than the existing column value then the value will be truncated.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="85c73-135">UniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="85c73-135">UniqueMultiValues</span></span></td>
<td><span data-ttu-id="85c73-136">Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos.</span><span class="sxs-lookup"><span data-stu-id="85c73-136">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="85c73-137">Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado.</span><span class="sxs-lookup"><span data-stu-id="85c73-137">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="85c73-138">Si se proporciona esta opción, AppendLV, OverwriteLV y SizeLV también no se pueden proporcionar.</span><span class="sxs-lookup"><span data-stu-id="85c73-138">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="85c73-139">UniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="85c73-139">UniqueNormalizedMultiValues</span></span></td>
<td><span data-ttu-id="85c73-140">Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos.</span><span class="sxs-lookup"><span data-stu-id="85c73-140">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="85c73-141">Esta opción compara la transformación normalizada clave de datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado.</span><span class="sxs-lookup"><span data-stu-id="85c73-141">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="85c73-142">Si se proporciona esta opción, AppendLV, OverwriteLV y SizeLV también no se pueden proporcionar.</span><span class="sxs-lookup"><span data-stu-id="85c73-142">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="85c73-143">ZeroLength</span><span class="sxs-lookup"><span data-stu-id="85c73-143">ZeroLength</span></span></td>
<td><span data-ttu-id="85c73-144">Esta opción se usa para establecer un valor de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="85c73-144">This option is used to set a value to zero length.</span></span> <span data-ttu-id="85c73-145">Normalmente, un valor de columna se establece en NULL pasando un cbMax de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="85c73-145">Normally, a column value is set to NULL by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="85c73-146">Sin embargo, para algunos tipos, como JET_coltyp. Text, un valor de columna puede tener una longitud de 0 (cero) en lugar de NULL, y esta opción se utiliza para diferenciar entre la longitud NULL y 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="85c73-146">However, for some types, like JET_coltyp.Text, a column value can be 0 (zero) length instead of NULL, and this option is used to differentiate between NULL and 0 (zero) length.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="85c73-147">IntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="85c73-147">IntrinsicLV</span></span></td>
<td><span data-ttu-id="85c73-148">Intente almacenar columnas de valores largos en el registro, incluso si superan el tamaño de la separación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="85c73-148">Try to store long-value columns in the record, even if they exceed the default separation size.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="85c73-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="85c73-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85c73-150">Referencia</span><span class="sxs-lookup"><span data-stu-id="85c73-150">Reference</span></span>

[<span data-ttu-id="85c73-151">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="85c73-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="85c73-152">Compressed</span><span class="sxs-lookup"><span data-stu-id="85c73-152">Compressed</span></span>](./windows7grbits.compressed-field.md)

[<span data-ttu-id="85c73-153">Sin comprimir</span><span class="sxs-lookup"><span data-stu-id="85c73-153">Uncompressed</span></span>](./windows7grbits.uncompressed-field.md)
