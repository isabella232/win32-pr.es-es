---
description: 'Más información acerca de: JET_COLUMNID. Operador LessThanOrEqual'
title: JET_COLUMNID. Operador LessThanOrEqual
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39513688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d6f98c5861a57fa4916ebca1b421c538d752d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811096"
---
# <a name="jet_columnidlessthanorequal-operator"></a><span data-ttu-id="2a750-103">JET_COLUMNID. Operador LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2a750-103">JET_COLUMNID.LessThanOrEqual operator</span></span>

<span data-ttu-id="2a750-104">Determine si un columnid es anterior o igual a otro columnid.</span><span class="sxs-lookup"><span data-stu-id="2a750-104">Determine whether one columnid is before or equal to another columnid.</span></span>

<span data-ttu-id="2a750-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2a750-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2a750-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2a750-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2a750-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a750-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="2a750-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a750-108">Parameters</span></span>

  - <span data-ttu-id="2a750-109">LHS</span><span class="sxs-lookup"><span data-stu-id="2a750-109">lhs</span></span>  
    <span data-ttu-id="2a750-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2a750-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="2a750-111">Primer columnid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="2a750-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="2a750-112">rhs</span><span class="sxs-lookup"><span data-stu-id="2a750-112">rhs</span></span>  
    <span data-ttu-id="2a750-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2a750-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="2a750-114">Segundo columnid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="2a750-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2a750-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a750-115">Return value</span></span>

<span data-ttu-id="2a750-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="2a750-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="2a750-117">True si LHS viene antes o es igual a RHS.</span><span class="sxs-lookup"><span data-stu-id="2a750-117">True if lhs comes before or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2a750-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a750-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a750-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="2a750-119">Reference</span></span>

[<span data-ttu-id="2a750-120">Estructura de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2a750-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="2a750-121">Miembros de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2a750-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="2a750-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2a750-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
