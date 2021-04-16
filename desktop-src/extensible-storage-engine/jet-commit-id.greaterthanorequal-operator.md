---
description: 'Más información sobre: operador JET_COMMIT_ID. GreaterThanOrEqual'
title: Operador JET_COMMIT_ID. GreaterThanOrEqual (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 55104298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e531168d2c0656c465d8eace46d00181375bc4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705812"
---
# <a name="jet_commit_idgreaterthanorequal-operator"></a><span data-ttu-id="ac83c-103">JET_COMMIT_ID. GreaterThanOrEqual (operador)</span><span class="sxs-lookup"><span data-stu-id="ac83c-103">JET_COMMIT_ID.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="ac83c-104">Determinar si un commitid está antes que otro commitid.</span><span class="sxs-lookup"><span data-stu-id="ac83c-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="ac83c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac83c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="ac83c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac83c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac83c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac83c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="ac83c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac83c-108">Parameters</span></span>

  - <span data-ttu-id="ac83c-109">LHS</span><span class="sxs-lookup"><span data-stu-id="ac83c-109">lhs</span></span>  
    <span data-ttu-id="ac83c-110">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="ac83c-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="ac83c-111">Primer commitid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="ac83c-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="ac83c-112">rhs</span><span class="sxs-lookup"><span data-stu-id="ac83c-112">rhs</span></span>  
    <span data-ttu-id="ac83c-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="ac83c-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="ac83c-114">Segundo commitid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="ac83c-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ac83c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac83c-115">Return value</span></span>

<span data-ttu-id="ac83c-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ac83c-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ac83c-117">True si LHS va después o igual a RHS.</span><span class="sxs-lookup"><span data-stu-id="ac83c-117">True if lhs comes after or equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac83c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac83c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac83c-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="ac83c-119">Reference</span></span>

[<span data-ttu-id="ac83c-120">JET_COMMIT_ID (clase)</span><span class="sxs-lookup"><span data-stu-id="ac83c-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="ac83c-121">Miembros de JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="ac83c-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="ac83c-122">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="ac83c-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
