---
description: 'Más información sobre: enumeración GetLockGrbit'
title: Enumeración GetLockGrbit
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001461"
---
# <a name="getlockgrbit-enumeration"></a><span data-ttu-id="70bed-103">Enumeración GetLockGrbit</span><span class="sxs-lookup"><span data-stu-id="70bed-103">GetLockGrbit enumeration</span></span>

<span data-ttu-id="70bed-104">Opciones de JetGetLock.</span><span class="sxs-lookup"><span data-stu-id="70bed-104">Options for JetGetLock.</span></span>

<span data-ttu-id="70bed-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="70bed-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="70bed-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="70bed-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="70bed-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="70bed-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="70bed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70bed-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a><span data-ttu-id="70bed-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="70bed-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="70bed-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="70bed-110">Member name</span></span></th>
<th><span data-ttu-id="70bed-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="70bed-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="70bed-112">Lectura</span><span class="sxs-lookup"><span data-stu-id="70bed-112">Read</span></span></td>
<td><span data-ttu-id="70bed-113">Adquirir un bloqueo de lectura en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="70bed-113">Acquire a read lock on the current record.</span></span> <span data-ttu-id="70bed-114">Los bloqueos de lectura son incompatibles con los bloqueos de escritura que ya se encuentran en otras sesiones, pero son compatibles con los bloqueos de lectura retenidos por otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="70bed-114">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="70bed-115">Escritura</span><span class="sxs-lookup"><span data-stu-id="70bed-115">Write</span></span></td>
<td><span data-ttu-id="70bed-116">Adquiere un bloqueo de escritura en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="70bed-116">Acquire a write lock on the current record.</span></span> <span data-ttu-id="70bed-117">Los bloqueos de escritura no son compatibles con los bloqueos de lectura o escritura retenidos por otras sesiones, pero son compatibles con los bloqueos de lectura retenidos por la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="70bed-117">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="70bed-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="70bed-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="70bed-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="70bed-119">Reference</span></span>

[<span data-ttu-id="70bed-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="70bed-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
