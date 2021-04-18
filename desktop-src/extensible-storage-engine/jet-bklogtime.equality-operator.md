---
description: 'Más información acerca de: JET_BKLOGTIME. Operador de igualdad'
title: JET_BKLOGTIME. Operador de igualdad
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515956
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5a75a1fc55159fc5ea71dba09dc1ed54194b940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697882"
---
# <a name="jet_bklogtimeequality-operator"></a><span data-ttu-id="7f82c-103">JET_BKLOGTIME. Operador de igualdad</span><span class="sxs-lookup"><span data-stu-id="7f82c-103">JET_BKLOGTIME.Equality operator</span></span>

<span data-ttu-id="7f82c-104">Determina si dos instancias especificadas de JET_BKLOGTIME son iguales.</span><span class="sxs-lookup"><span data-stu-id="7f82c-104">Determines whether two specified instances of JET_BKLOGTIME are equal.</span></span>

<span data-ttu-id="7f82c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f82c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f82c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7f82c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f82c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f82c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7f82c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f82c-108">Parameters</span></span>

  - <span data-ttu-id="7f82c-109">LHS</span><span class="sxs-lookup"><span data-stu-id="7f82c-109">lhs</span></span>  
    <span data-ttu-id="7f82c-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7f82c-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="7f82c-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7f82c-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7f82c-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7f82c-112">rhs</span></span>  
    <span data-ttu-id="7f82c-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7f82c-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="7f82c-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7f82c-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7f82c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f82c-115">Return value</span></span>

<span data-ttu-id="7f82c-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7f82c-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7f82c-117">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="7f82c-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7f82c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f82c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f82c-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="7f82c-119">Reference</span></span>

[<span data-ttu-id="7f82c-120">Estructura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="7f82c-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="7f82c-121">Miembros de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="7f82c-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="7f82c-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7f82c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
