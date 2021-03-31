---
description: 'Más información acerca de: JET_THREADSTATS. Operador de desigualdad'
title: JET_THREADSTATS. Operador de desigualdad (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510396
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dd3bc0f56b5fbbc47928387f999664df7bcc7a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912174"
---
# <a name="jet_threadstatsinequality-operator"></a><span data-ttu-id="a7492-103">JET_THREADSTATS. Operador de desigualdad</span><span class="sxs-lookup"><span data-stu-id="a7492-103">JET_THREADSTATS.Inequality operator</span></span>

<span data-ttu-id="a7492-104">Determina si dos instancias especificadas de JET_THREADSTATS no son iguales.</span><span class="sxs-lookup"><span data-stu-id="a7492-104">Determines whether two specified instances of JET_THREADSTATS are not equal.</span></span>

<span data-ttu-id="a7492-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7492-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="a7492-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7492-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7492-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7492-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a7492-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7492-108">Parameters</span></span>

  - <span data-ttu-id="a7492-109">LHS</span><span class="sxs-lookup"><span data-stu-id="a7492-109">lhs</span></span>  
    <span data-ttu-id="a7492-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a7492-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="a7492-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="a7492-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7492-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a7492-112">rhs</span></span>  
    <span data-ttu-id="a7492-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a7492-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="a7492-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="a7492-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a7492-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7492-115">Return value</span></span>

<span data-ttu-id="a7492-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a7492-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a7492-117">True si las dos instancias de no son iguales.</span><span class="sxs-lookup"><span data-stu-id="a7492-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a7492-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7492-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7492-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="a7492-119">Reference</span></span>

[<span data-ttu-id="a7492-120">Estructura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="a7492-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="a7492-121">Miembros de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="a7492-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="a7492-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="a7492-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
