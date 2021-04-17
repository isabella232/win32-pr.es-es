---
description: 'Más información acerca de: JET_COMMIT_ID. desigualdad (operador)'
title: JET_COMMIT_ID. operador de desigualdad (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_inequality(v=EXCHG.10)
ms:contentKeyID: 55104411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b64be3b2c6438490d3e44076b1e553a7abb37d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716545"
---
# <a name="jet_commit_idinequality-operator"></a><span data-ttu-id="7aab5-103">JET_COMMIT_ID. desigualdad (operador)</span><span class="sxs-lookup"><span data-stu-id="7aab5-103">JET_COMMIT_ID.Inequality operator</span></span>

<span data-ttu-id="7aab5-104">Determine si un commitid no es igual a otro commitid.</span><span class="sxs-lookup"><span data-stu-id="7aab5-104">Determine whether one commitid is not equal to another commitid.</span></span>

<span data-ttu-id="7aab5-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7aab5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="7aab5-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7aab5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7aab5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7aab5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7aab5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7aab5-108">Parameters</span></span>

  - <span data-ttu-id="7aab5-109">LHS</span><span class="sxs-lookup"><span data-stu-id="7aab5-109">lhs</span></span>  
    <span data-ttu-id="7aab5-110">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="7aab5-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="7aab5-111">Primer commitid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7aab5-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7aab5-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7aab5-112">rhs</span></span>  
    <span data-ttu-id="7aab5-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="7aab5-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="7aab5-114">Segundo commitid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7aab5-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7aab5-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7aab5-115">Return value</span></span>

<span data-ttu-id="7aab5-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7aab5-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7aab5-117">True si LHS no es igual a RHS.</span><span class="sxs-lookup"><span data-stu-id="7aab5-117">True if lhs comes is not equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7aab5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7aab5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7aab5-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="7aab5-119">Reference</span></span>

[<span data-ttu-id="7aab5-120">JET_COMMIT_ID (clase)</span><span class="sxs-lookup"><span data-stu-id="7aab5-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="7aab5-121">Miembros de JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="7aab5-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="7aab5-122">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="7aab5-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
