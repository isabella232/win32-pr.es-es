---
description: 'Más información acerca de: constructor de transacciones'
title: Constructor de transacción
TOCTitle: 'Transaction constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.transaction(v=EXCHG.10)
ms:contentKeyID: 55104069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.Transaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a8c3214ebe3d88ce8b50aff000d64270ec50a6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278038"
---
# <a name="transaction-constructor"></a><span data-ttu-id="7737a-103">Constructor de transacción</span><span class="sxs-lookup"><span data-stu-id="7737a-103">Transaction constructor</span></span>

<span data-ttu-id="7737a-104">Inicializa una nueva instancia de la clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="7737a-104">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="7737a-105">Esto inicia automáticamente una transacción.</span><span class="sxs-lookup"><span data-stu-id="7737a-105">This automatically begins a transaction.</span></span> <span data-ttu-id="7737a-106">La transacción se revertirá si no se confirma explícitamente.</span><span class="sxs-lookup"><span data-stu-id="7737a-106">The transaction will be rolled back if not explicitly committed.</span></span>

<span data-ttu-id="7737a-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7737a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7737a-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7737a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7737a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7737a-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID

Dim instance As New Transaction(sesid)
```

``` csharp
public Transaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="7737a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7737a-110">Parameters</span></span>

  - <span data-ttu-id="7737a-111">sesid</span><span class="sxs-lookup"><span data-stu-id="7737a-111">sesid</span></span>  
    <span data-ttu-id="7737a-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7737a-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7737a-113">Sesión para la que se va a iniciar la transacción.</span><span class="sxs-lookup"><span data-stu-id="7737a-113">The session to start the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="7737a-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="7737a-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7737a-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="7737a-115">Reference</span></span>

[<span data-ttu-id="7737a-116">Transaction, clase</span><span class="sxs-lookup"><span data-stu-id="7737a-116">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="7737a-117">Miembros de transacción</span><span class="sxs-lookup"><span data-stu-id="7737a-117">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="7737a-118">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7737a-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
