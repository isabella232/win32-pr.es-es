---
description: 'Más información sobre: método Transaction. Commit (CommitTransactionGrbit)'
title: Método Transaction. Commit (CommitTransactionGrbit)
TOCTitle: Commit method (CommitTransactionGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104071
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 048071a08d1211d6091fb6c2c23f9cfe302f8872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278032"
---
# <a name="transactioncommit-method-committransactiongrbit"></a><span data-ttu-id="71ca4-103">Método Transaction. Commit (CommitTransactionGrbit)</span><span class="sxs-lookup"><span data-stu-id="71ca4-103">Transaction.Commit method (CommitTransactionGrbit)</span></span>

<span data-ttu-id="71ca4-104">Confirme una transacción.</span><span class="sxs-lookup"><span data-stu-id="71ca4-104">Commit a transaction.</span></span> <span data-ttu-id="71ca4-105">Este objeto debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="71ca4-105">This object should be in a transaction.</span></span>

<span data-ttu-id="71ca4-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71ca4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71ca4-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71ca4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71ca4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71ca4-108">Syntax</span></span>

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit

instance.Commit(grbit)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="71ca4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71ca4-109">Parameters</span></span>

  - <span data-ttu-id="71ca4-110">grbit</span><span class="sxs-lookup"><span data-stu-id="71ca4-110">grbit</span></span>  
    <span data-ttu-id="71ca4-111">Tipo: [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="71ca4-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="71ca4-112">Opciones de JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="71ca4-112">JetCommitTransaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="71ca4-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="71ca4-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71ca4-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="71ca4-114">Reference</span></span>

[<span data-ttu-id="71ca4-115">Transaction, clase</span><span class="sxs-lookup"><span data-stu-id="71ca4-115">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="71ca4-116">Miembros de transacción</span><span class="sxs-lookup"><span data-stu-id="71ca4-116">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="71ca4-117">Sobrecarga de confirmación</span><span class="sxs-lookup"><span data-stu-id="71ca4-117">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="71ca4-118">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="71ca4-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
