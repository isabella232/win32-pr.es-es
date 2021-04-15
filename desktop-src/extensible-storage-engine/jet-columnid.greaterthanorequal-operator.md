---
description: 'Más información acerca de: JET_COLUMNID. Operador GreaterThanOrEqual'
title: JET_COLUMNID. Operador GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39509674
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 344d1ed95ebc6a4a79d17f8b664f3f8a76740367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696234"
---
# <a name="jet_columnidgreaterthanorequal-operator"></a><span data-ttu-id="75e22-103">JET_COLUMNID. Operador GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="75e22-103">JET_COLUMNID.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="75e22-104">Determine si un columnid es posterior o igual a otro columnid.</span><span class="sxs-lookup"><span data-stu-id="75e22-104">Determine whether one columnid is after or equal to another columnid.</span></span>

<span data-ttu-id="75e22-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75e22-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75e22-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75e22-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75e22-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75e22-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="75e22-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75e22-108">Parameters</span></span>

  - <span data-ttu-id="75e22-109">LHS</span><span class="sxs-lookup"><span data-stu-id="75e22-109">lhs</span></span>  
    <span data-ttu-id="75e22-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="75e22-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="75e22-111">Primer columnid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="75e22-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="75e22-112">rhs</span><span class="sxs-lookup"><span data-stu-id="75e22-112">rhs</span></span>  
    <span data-ttu-id="75e22-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="75e22-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="75e22-114">Segundo columnid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="75e22-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="75e22-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75e22-115">Return value</span></span>

<span data-ttu-id="75e22-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="75e22-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="75e22-117">True si LHS viene después de o es igual a RHS.</span><span class="sxs-lookup"><span data-stu-id="75e22-117">True if lhs comes after or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="75e22-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="75e22-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75e22-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="75e22-119">Reference</span></span>

[<span data-ttu-id="75e22-120">Estructura de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="75e22-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="75e22-121">Miembros de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="75e22-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="75e22-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="75e22-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
