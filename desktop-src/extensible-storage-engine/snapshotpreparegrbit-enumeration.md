---
description: 'Más información sobre: enumeración SnapshotPrepareGrbit'
title: Enumeración SnapshotPrepareGrbit
TOCTitle: SnapshotPrepareGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.snapshotpreparegrbit(v=EXCHG.10)
ms:contentKeyID: 39515688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32c11c609f78cc96862f9c2f15d93266f40ae941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360390"
---
# <a name="snapshotpreparegrbit-enumeration"></a><span data-ttu-id="8b598-103">Enumeración SnapshotPrepareGrbit</span><span class="sxs-lookup"><span data-stu-id="8b598-103">SnapshotPrepareGrbit enumeration</span></span>

<span data-ttu-id="8b598-104">Opciones de [JetOSSnapshotPrepare (JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b598-104">Options for [JetOSSnapshotPrepare(JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span></span>

<span data-ttu-id="8b598-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="8b598-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8b598-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8b598-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8b598-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8b598-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8b598-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b598-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotPrepareGrbit
'Usage
Dim instance As SnapshotPrepareGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotPrepareGrbit
```

## <a name="members"></a><span data-ttu-id="8b598-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b598-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8b598-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="8b598-110">Member name</span></span></th>
<th><span data-ttu-id="8b598-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b598-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8b598-112">None</span><span class="sxs-lookup"><span data-stu-id="8b598-112">None</span></span></td>
<td><span data-ttu-id="8b598-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="8b598-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8b598-114">IncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="8b598-114">IncrementalSnapshot</span></span></td>
<td><span data-ttu-id="8b598-115">Solo se tomarán los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="8b598-115">Only logfiles will be taken.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8b598-116">CopySnapshot</span><span class="sxs-lookup"><span data-stu-id="8b598-116">CopySnapshot</span></span></td>
<td><span data-ttu-id="8b598-117">Una instantánea de copia (normal o incremental) sin truncamiento del registro.</span><span class="sxs-lookup"><span data-stu-id="8b598-117">A copy snapshot (normal or incremental) with no log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8b598-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b598-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8b598-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="8b598-119">Reference</span></span>

[<span data-ttu-id="8b598-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8b598-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
