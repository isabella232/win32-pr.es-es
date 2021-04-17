---
description: 'Más información acerca de: JET_THREADSTATS. Operador de igualdad'
title: JET_THREADSTATS. Operador de igualdad (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 076ae2cfa25f446d8d6200fbee7f53ecf0edea5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706893"
---
# <a name="jet_threadstatsequality-operator"></a><span data-ttu-id="4bda8-103">JET_THREADSTATS. Operador de igualdad</span><span class="sxs-lookup"><span data-stu-id="4bda8-103">JET_THREADSTATS.Equality operator</span></span>

<span data-ttu-id="4bda8-104">Determina si dos instancias especificadas de JET_THREADSTATS son iguales.</span><span class="sxs-lookup"><span data-stu-id="4bda8-104">Determines whether two specified instances of JET_THREADSTATS are equal.</span></span>

<span data-ttu-id="4bda8-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4bda8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4bda8-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4bda8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4bda8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bda8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4bda8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bda8-108">Parameters</span></span>

  - <span data-ttu-id="4bda8-109">LHS</span><span class="sxs-lookup"><span data-stu-id="4bda8-109">lhs</span></span>  
    <span data-ttu-id="4bda8-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4bda8-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="4bda8-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4bda8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bda8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4bda8-112">rhs</span></span>  
    <span data-ttu-id="4bda8-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4bda8-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="4bda8-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4bda8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4bda8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bda8-115">Return value</span></span>

<span data-ttu-id="4bda8-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4bda8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4bda8-117">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="4bda8-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4bda8-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bda8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4bda8-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="4bda8-119">Reference</span></span>

[<span data-ttu-id="4bda8-120">Estructura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="4bda8-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="4bda8-121">Miembros de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="4bda8-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="4bda8-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="4bda8-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
