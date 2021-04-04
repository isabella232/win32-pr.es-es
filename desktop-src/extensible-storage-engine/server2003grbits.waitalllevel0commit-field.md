---
description: 'Más información sobre: Server2003Grbits. WaitAllLevel0Commit, campo'
title: Campo Server2003Grbits. WaitAllLevel0Commit (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16390069adf81ead8e819bc5148a88e30900b508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910229"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a><span data-ttu-id="17536-103">Server2003Grbits. WaitAllLevel0Commit, campo</span><span class="sxs-lookup"><span data-stu-id="17536-103">Server2003Grbits.WaitAllLevel0Commit field</span></span>

<span data-ttu-id="17536-104">Todas las transacciones confirmadas previamente por cualquier sesión que todavía no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="17536-104">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="17536-105">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="17536-105">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="17536-106">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="17536-106">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="17536-107">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="17536-107">This option cannot be used in combination with any other option.</span></span>

<span data-ttu-id="17536-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="17536-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="17536-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="17536-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="17536-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17536-110">Syntax</span></span>

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a><span data-ttu-id="17536-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="17536-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="17536-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="17536-112">Reference</span></span>

[<span data-ttu-id="17536-113">Clase Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="17536-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="17536-114">Miembros de Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="17536-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="17536-115">Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="17536-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
