---
description: 'Más información sobre: enumeración SnapshotTruncateLogGrbit'
title: Enumeración SnapshotTruncateLogGrbit (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: SnapshotTruncateLogGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.snapshottruncateloggrbit(v=EXCHG.10)
ms:contentKeyID: 39516474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8baf9f9ec15e91183d2b01a07da9aeda0c7fec18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705751"
---
# <a name="snapshottruncateloggrbit-enumeration"></a><span data-ttu-id="630b7-103">Enumeración SnapshotTruncateLogGrbit</span><span class="sxs-lookup"><span data-stu-id="630b7-103">SnapshotTruncateLogGrbit enumeration</span></span>

<span data-ttu-id="630b7-104">Opciones para [JetOSSnapshotTruncateLog (JET_OSSNAPID, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncatelog-method.md) y [JetOSSnapshotTruncateLogInstance (JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="630b7-104">Options for [JetOSSnapshotTruncateLog(JET_OSSNAPID, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncatelog-method.md) and [JetOSSnapshotTruncateLogInstance(JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).</span></span>

<span data-ttu-id="630b7-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="630b7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="630b7-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="630b7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="630b7-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="630b7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="630b7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="630b7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotTruncateLogGrbit
'Usage
Dim instance As SnapshotTruncateLogGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotTruncateLogGrbit
```

## <a name="members"></a><span data-ttu-id="630b7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="630b7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="630b7-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="630b7-110">Member name</span></span></th>
<th><span data-ttu-id="630b7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="630b7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="630b7-112">None</span><span class="sxs-lookup"><span data-stu-id="630b7-112">None</span></span></td>
<td><span data-ttu-id="630b7-113">No se producirá ningún truncamiento.</span><span class="sxs-lookup"><span data-stu-id="630b7-113">No truncation will occur.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="630b7-114">AllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="630b7-114">AllDatabasesSnapshot</span></span></td>
<td><span data-ttu-id="630b7-115">Todas las bases de datos están adjuntas para que el motor de almacenamiento pueda calcular y realizar el truncamiento del registro.</span><span class="sxs-lookup"><span data-stu-id="630b7-115">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="630b7-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="630b7-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="630b7-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="630b7-117">Reference</span></span>

[<span data-ttu-id="630b7-118">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="630b7-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
