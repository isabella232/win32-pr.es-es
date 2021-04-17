---
description: 'Más información sobre: enumeración GetRecordSizeGrbit'
title: Enumeración GetRecordSizeGrbit
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666789"
---
# <a name="getrecordsizegrbit-enumeration"></a><span data-ttu-id="23d45-103">Enumeración GetRecordSizeGrbit</span><span class="sxs-lookup"><span data-stu-id="23d45-103">GetRecordSizeGrbit enumeration</span></span>

<span data-ttu-id="23d45-104">Opciones para [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span><span class="sxs-lookup"><span data-stu-id="23d45-104">Options for [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span></span>

<span data-ttu-id="23d45-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="23d45-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="23d45-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23d45-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="23d45-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="23d45-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23d45-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23d45-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
```

## <a name="members"></a><span data-ttu-id="23d45-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="23d45-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="23d45-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="23d45-110">Member name</span></span></th>
<th><span data-ttu-id="23d45-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="23d45-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23d45-112">None</span><span class="sxs-lookup"><span data-stu-id="23d45-112">None</span></span></td>
<td><span data-ttu-id="23d45-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="23d45-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="23d45-114">InCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="23d45-114">InCopyBuffer</span></span></td>
<td><span data-ttu-id="23d45-115">Recupere el tamaño del registro que se encuentra en el búfer de copia preparado o actualizado.</span><span class="sxs-lookup"><span data-stu-id="23d45-115">Retrieve the size of the record that is in the copy buffer prepared or update.</span></span> <span data-ttu-id="23d45-116">De lo contrario, el ID. de la ubicación debe estar colocado en un registro y se utilizará ese registro.</span><span class="sxs-lookup"><span data-stu-id="23d45-116">Otherwise, the tableid must be positioned on a record, and that record will be used.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23d45-117">RunningTotal</span><span class="sxs-lookup"><span data-stu-id="23d45-117">RunningTotal</span></span></td>
<td><span data-ttu-id="23d45-118">El JET_RECSIZE no es cero antes de rellenar el contenido, lo que actúa de forma eficaz como acumulación de las estadísticas de varios registros visitados o actualizados.</span><span class="sxs-lookup"><span data-stu-id="23d45-118">The JET_RECSIZE is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="23d45-119">Local</span><span class="sxs-lookup"><span data-stu-id="23d45-119">Local</span></span></td>
<td><span data-ttu-id="23d45-120">Omitir los valores largos no intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="23d45-120">Ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="23d45-121">Solo se utilizará el registro local de la página.</span><span class="sxs-lookup"><span data-stu-id="23d45-121">Only the local record on the page will be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="23d45-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="23d45-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23d45-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="23d45-123">Reference</span></span>

[<span data-ttu-id="23d45-124">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="23d45-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
