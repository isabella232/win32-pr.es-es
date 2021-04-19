---
description: 'Más información acerca de: JET_BKLOGTIME. Operador de desigualdad'
title: JET_BKLOGTIME. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42f13a1068543caaa590015151b523c1a441c806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707045"
---
# <a name="jet_bklogtimeinequality-operator"></a><span data-ttu-id="4ddc8-103">JET_BKLOGTIME. Operador de desigualdad</span><span class="sxs-lookup"><span data-stu-id="4ddc8-103">JET_BKLOGTIME.Inequality operator</span></span>

<span data-ttu-id="4ddc8-104">Determina si dos instancias especificadas de JET_BKLOGTIME no son iguales.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-104">Determines whether two specified instances of JET_BKLOGTIME are not equal.</span></span>

<span data-ttu-id="4ddc8-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ddc8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ddc8-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ddc8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddc8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ddc8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4ddc8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ddc8-108">Parameters</span></span>

  - <span data-ttu-id="4ddc8-109">LHS</span><span class="sxs-lookup"><span data-stu-id="4ddc8-109">lhs</span></span>  
    <span data-ttu-id="4ddc8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4ddc8-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="4ddc8-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ddc8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4ddc8-112">rhs</span></span>  
    <span data-ttu-id="4ddc8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4ddc8-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="4ddc8-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4ddc8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ddc8-115">Return value</span></span>

<span data-ttu-id="4ddc8-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4ddc8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4ddc8-117">True si las dos instancias de no son iguales.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ddc8-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ddc8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ddc8-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="4ddc8-119">Reference</span></span>

[<span data-ttu-id="4ddc8-120">Estructura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="4ddc8-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="4ddc8-121">Miembros de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="4ddc8-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="4ddc8-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4ddc8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
