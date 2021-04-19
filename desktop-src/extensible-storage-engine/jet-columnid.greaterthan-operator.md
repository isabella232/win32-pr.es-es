---
description: 'Más información acerca de: JET_COLUMNID. GreaterThan (operador)'
title: JET_COLUMNID. GreaterThan (operador)
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 39513070
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16105651443aad050a1bbaf4a9dee1e68a5042fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707201"
---
# <a name="jet_columnidgreaterthan-operator"></a><span data-ttu-id="4d915-103">JET_COLUMNID. GreaterThan (operador)</span><span class="sxs-lookup"><span data-stu-id="4d915-103">JET_COLUMNID.GreaterThan operator</span></span>

<span data-ttu-id="4d915-104">Determine si un columnid es posterior a otro columnid.</span><span class="sxs-lookup"><span data-stu-id="4d915-104">Determine whether one columnid is after another columnid.</span></span>

<span data-ttu-id="4d915-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d915-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d915-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d915-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d915-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d915-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4d915-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d915-108">Parameters</span></span>

  - <span data-ttu-id="4d915-109">LHS</span><span class="sxs-lookup"><span data-stu-id="4d915-109">lhs</span></span>  
    <span data-ttu-id="4d915-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d915-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4d915-111">Primer columnid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4d915-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d915-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4d915-112">rhs</span></span>  
    <span data-ttu-id="4d915-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d915-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4d915-114">Segundo columnid que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4d915-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4d915-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d915-115">Return value</span></span>

<span data-ttu-id="4d915-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4d915-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4d915-117">True si LHS viene después de RHS.</span><span class="sxs-lookup"><span data-stu-id="4d915-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4d915-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d915-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d915-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="4d915-119">Reference</span></span>

[<span data-ttu-id="4d915-120">Estructura de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4d915-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="4d915-121">Miembros de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4d915-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="4d915-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4d915-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
