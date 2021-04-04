---
description: 'Más información acerca de: JET_TABLEID. Operador de igualdad'
title: JET_TABLEID. Operador de igualdad
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Equality(Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515925
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equality
- Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b653fcd4576a1069a2c2d896d4e2cb58b9864ece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278054"
---
# <a name="jet_tableidequality-operator"></a><span data-ttu-id="4f178-103">JET_TABLEID. Operador de igualdad</span><span class="sxs-lookup"><span data-stu-id="4f178-103">JET_TABLEID.Equality operator</span></span>

<span data-ttu-id="4f178-104">Determina si dos instancias especificadas de JET_TABLEID son iguales.</span><span class="sxs-lookup"><span data-stu-id="4f178-104">Determines whether two specified instances of JET_TABLEID are equal.</span></span>

<span data-ttu-id="4f178-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4f178-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4f178-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4f178-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f178-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f178-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_TABLEID, _
    rhs As JET_TABLEID _
) As Boolean
'Usage
Dim lhs As JET_TABLEID
Dim rhs As JET_TABLEID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_TABLEID lhs,
    JET_TABLEID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4f178-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f178-108">Parameters</span></span>

  - <span data-ttu-id="4f178-109">LHS</span><span class="sxs-lookup"><span data-stu-id="4f178-109">lhs</span></span>  
    <span data-ttu-id="4f178-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4f178-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4f178-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4f178-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f178-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4f178-112">rhs</span></span>  
    <span data-ttu-id="4f178-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4f178-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4f178-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4f178-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4f178-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f178-115">Return value</span></span>

<span data-ttu-id="4f178-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4f178-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4f178-117">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="4f178-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4f178-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f178-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4f178-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="4f178-119">Reference</span></span>

[<span data-ttu-id="4f178-120">Estructura de JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4f178-120">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="4f178-121">Miembros de JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4f178-121">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="4f178-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4f178-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
