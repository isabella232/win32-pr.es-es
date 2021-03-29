---
description: 'Más información acerca de: JET_INDEXID. Operador de igualdad'
title: JET_INDEXID. Operador de igualdad
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality(Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39516722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
- Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9fa7574aeed52377b516f63549a6f690dc168d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003179"
---
# <a name="jet_indexidequality-operator"></a><span data-ttu-id="dc1c8-103">JET_INDEXID. Operador de igualdad</span><span class="sxs-lookup"><span data-stu-id="dc1c8-103">JET_INDEXID.Equality operator</span></span>

<span data-ttu-id="dc1c8-104">Determina si dos instancias especificadas de JET_INDEXID son iguales.</span><span class="sxs-lookup"><span data-stu-id="dc1c8-104">Determines whether two specified instances of JET_INDEXID are equal.</span></span>

<span data-ttu-id="dc1c8-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc1c8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dc1c8-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc1c8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1c8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc1c8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INDEXID, _
    rhs As JET_INDEXID _
) As Boolean
'Usage
Dim lhs As JET_INDEXID
Dim rhs As JET_INDEXID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INDEXID lhs,
    JET_INDEXID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="dc1c8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc1c8-108">Parameters</span></span>

  - <span data-ttu-id="dc1c8-109">LHS</span><span class="sxs-lookup"><span data-stu-id="dc1c8-109">lhs</span></span>  
    <span data-ttu-id="dc1c8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="dc1c8-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="dc1c8-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="dc1c8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc1c8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="dc1c8-112">rhs</span></span>  
    <span data-ttu-id="dc1c8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="dc1c8-113">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="dc1c8-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="dc1c8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="dc1c8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc1c8-115">Return value</span></span>

<span data-ttu-id="dc1c8-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="dc1c8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="dc1c8-117">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="dc1c8-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dc1c8-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc1c8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc1c8-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="dc1c8-119">Reference</span></span>

[<span data-ttu-id="dc1c8-120">Estructura de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="dc1c8-120">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="dc1c8-121">Miembros de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="dc1c8-121">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="dc1c8-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dc1c8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
