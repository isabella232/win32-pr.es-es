---
description: 'Más información sobre: enumeración MakeKeyGrbit'
title: Enumeración MakeKeyGrbit
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154000"
---
# <a name="makekeygrbit-enumeration"></a><span data-ttu-id="25006-103">Enumeración MakeKeyGrbit</span><span class="sxs-lookup"><span data-stu-id="25006-103">MakeKeyGrbit enumeration</span></span>

<span data-ttu-id="25006-104">Opciones de JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="25006-104">Options for JetMakeKey.</span></span>

<span data-ttu-id="25006-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="25006-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="25006-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25006-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25006-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25006-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25006-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25006-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
```

## <a name="members"></a><span data-ttu-id="25006-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="25006-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="25006-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="25006-110">Member name</span></span></th>
<th><span data-ttu-id="25006-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="25006-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25006-112">None</span><span class="sxs-lookup"><span data-stu-id="25006-112">None</span></span></td>
<td><span data-ttu-id="25006-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="25006-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25006-114">Nuevaclave</span><span class="sxs-lookup"><span data-stu-id="25006-114">NewKey</span></span></td>
<td><span data-ttu-id="25006-115">Se debe crear una nueva clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="25006-115">A new search key should be constructed.</span></span> <span data-ttu-id="25006-116">Se descarta cualquier clave de búsqueda existente previamente.</span><span class="sxs-lookup"><span data-stu-id="25006-116">Any previously existing search key is discarded.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25006-117">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="25006-117">NormalizedKey</span></span></td>
<td><span data-ttu-id="25006-118">Cuando se especifica esta opción, se omiten todas las demás opciones, se descarta cualquier clave de búsqueda existente y el contenido del búfer de entrada se carga como la nueva clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="25006-118">When this option is specified, all other options are ignored, any previously existing search key is discarded, and the contents of the input buffer are loaded as the new search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25006-119">KeyDataZeroLength</span><span class="sxs-lookup"><span data-stu-id="25006-119">KeyDataZeroLength</span></span></td>
<td><span data-ttu-id="25006-120">Si el tamaño del búfer de entrada es cero y la columna de clave actual es una columna de longitud variable, esta opción indica que el búfer de entrada contiene un valor de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="25006-120">If the size of the input buffer is zero and the current key column is a variable length column, this option indicates that the input buffer contains a zero length value.</span></span> <span data-ttu-id="25006-121">De lo contrario, el tamaño del búfer de entrada cero indicaría un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="25006-121">Otherwise, an input buffer size of zero would indicate a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25006-122">StrLimit</span><span class="sxs-lookup"><span data-stu-id="25006-122">StrLimit</span></span></td>
<td><span data-ttu-id="25006-123">Esta opción indica que la clave de búsqueda debe construirse de tal forma que las columnas de clave que aparecen después de la columna de clave actual se consideren como caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="25006-123">This option indicates that the search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25006-124">SubStrLimit</span><span class="sxs-lookup"><span data-stu-id="25006-124">SubStrLimit</span></span></td>
<td><span data-ttu-id="25006-125">Esta opción indica que la clave de búsqueda debe construirse de tal forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que se encuentran después de la columna de clave actual se consideren como caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="25006-125">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25006-126">FullColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="25006-126">FullColumnStartLimit</span></span></td>
<td><span data-ttu-id="25006-127">La clave de búsqueda se debe construir de modo que las columnas de clave que se encuentran después de la columna de clave actual se consideren como caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="25006-127">The search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25006-128">FullColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="25006-128">FullColumnEndLimit</span></span></td>
<td><span data-ttu-id="25006-129">La clave de búsqueda debe construirse de tal forma que las columnas de clave que aparecen después de la columna de clave actual se consideren como caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="25006-129">The search key should be constructed in such a way that any key columns that come after the current key column are considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25006-130">PartialColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="25006-130">PartialColumnStartLimit</span></span></td>
<td><span data-ttu-id="25006-131">La clave de búsqueda debe construirse de tal forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que aparecen después de la columna de clave actual se consideren como caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="25006-131">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25006-132">PartialColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="25006-132">PartialColumnEndLimit</span></span></td>
<td><span data-ttu-id="25006-133">La clave de búsqueda debe construirse de tal forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que aparecen después de la columna de clave actual se consideren como caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="25006-133">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="25006-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="25006-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25006-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="25006-135">Reference</span></span>

[<span data-ttu-id="25006-136">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="25006-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
