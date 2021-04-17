---
description: 'Más información acerca de: JET_LGPOS. GreaterThan (operador)'
title: JET_LGPOS. GreaterThan (operador)
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThan(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 39510131
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThan
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f3e0c060311205d1f5d47bc4678c6ff9458b589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678541"
---
# <a name="jet_lgposgreaterthan-operator"></a><span data-ttu-id="2083a-103">JET_LGPOS. GreaterThan (operador)</span><span class="sxs-lookup"><span data-stu-id="2083a-103">JET_LGPOS.GreaterThan operator</span></span>

<span data-ttu-id="2083a-104">Determinar si una posición del registro está después de otra posición del registro.</span><span class="sxs-lookup"><span data-stu-id="2083a-104">Determine whether one log position is after another log position.</span></span>

<span data-ttu-id="2083a-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2083a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2083a-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2083a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2083a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2083a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="2083a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2083a-108">Parameters</span></span>

  - <span data-ttu-id="2083a-109">LHS</span><span class="sxs-lookup"><span data-stu-id="2083a-109">lhs</span></span>  
    <span data-ttu-id="2083a-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2083a-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="2083a-111">Primera posición del registro que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="2083a-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="2083a-112">rhs</span><span class="sxs-lookup"><span data-stu-id="2083a-112">rhs</span></span>  
    <span data-ttu-id="2083a-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2083a-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="2083a-114">Segunda posición del registro que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="2083a-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2083a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2083a-115">Return value</span></span>

<span data-ttu-id="2083a-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="2083a-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="2083a-117">True si LHS viene después de RHS.</span><span class="sxs-lookup"><span data-stu-id="2083a-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2083a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2083a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2083a-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="2083a-119">Reference</span></span>

[<span data-ttu-id="2083a-120">Estructura de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="2083a-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="2083a-121">Miembros de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="2083a-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="2083a-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2083a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
