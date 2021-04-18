---
description: 'Más información sobre: enumeración CommitTransactionGrbit'
title: Enumeración CommitTransactionGrbit
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720773"
---
# <a name="committransactiongrbit-enumeration"></a><span data-ttu-id="82fa5-103">Enumeración CommitTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="82fa5-103">CommitTransactionGrbit enumeration</span></span>

<span data-ttu-id="82fa5-104">Opciones de JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="82fa5-104">Options for JetCommitTransaction.</span></span>

<span data-ttu-id="82fa5-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="82fa5-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="82fa5-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82fa5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82fa5-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82fa5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82fa5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82fa5-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="82fa5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="82fa5-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="82fa5-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="82fa5-110">Member name</span></span></th>
<th><span data-ttu-id="82fa5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="82fa5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82fa5-112">None</span><span class="sxs-lookup"><span data-stu-id="82fa5-112">None</span></span></td>
<td><span data-ttu-id="82fa5-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="82fa5-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82fa5-114">LazyFlush</span><span class="sxs-lookup"><span data-stu-id="82fa5-114">LazyFlush</span></span></td>
<td><span data-ttu-id="82fa5-115">La transacción se confirma normalmente, pero esta API no espera a que la transacción se vacíe en el archivo de registro de transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="82fa5-115">The transaction is committed normally but this Api does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="82fa5-116">Esto reduce drásticamente la duración de una operación de confirmación a costa de la durabilidad.</span><span class="sxs-lookup"><span data-stu-id="82fa5-116">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="82fa5-117">Cualquier transacción que no se vacíe en el registro antes de un bloqueo se anulará automáticamente durante la recuperación tras el bloqueo durante la siguiente llamada a JetInit.</span><span class="sxs-lookup"><span data-stu-id="82fa5-117">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to JetInit.</span></span> <span data-ttu-id="82fa5-118">Si se especifican WaitLastLevel0Commit o WaitAllLevel0Commit, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="82fa5-118">If WaitLastLevel0Commit or WaitAllLevel0Commit are specified, this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82fa5-119">WaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="82fa5-119">WaitLastLevel0Commit</span></span></td>
<td><span data-ttu-id="82fa5-120">Si la sesión ha confirmado previamente alguna transacción y aún no se ha vaciado en el archivo de registro de transacciones, se deben vaciar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="82fa5-120">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="82fa5-121">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="82fa5-121">This Api will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="82fa5-122">Esto resulta útil si la aplicación ha confirmado previamente varias transacciones mediante JET_bitCommitLazyFlush y ahora desea vaciar todas ellas en el disco.</span><span class="sxs-lookup"><span data-stu-id="82fa5-122">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span>
<p><span data-ttu-id="82fa5-123">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="82fa5-123">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="82fa5-124">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="82fa5-124">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="82fa5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="82fa5-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82fa5-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="82fa5-126">Reference</span></span>

[<span data-ttu-id="82fa5-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="82fa5-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
