---
description: 'Más información acerca de: JET_DBID. Operador de igualdad'
title: JET_DBID. Operador de igualdad
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality(Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
- Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f9e99de78665d07e1e5a800f5520a39eb05e74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543286"
---
# <a name="jet_dbidequality-operator"></a><span data-ttu-id="d8304-103">JET_DBID. Operador de igualdad</span><span class="sxs-lookup"><span data-stu-id="d8304-103">JET_DBID.Equality operator</span></span>

<span data-ttu-id="d8304-104">Determina si dos instancias especificadas de JET_DBID son iguales.</span><span class="sxs-lookup"><span data-stu-id="d8304-104">Determines whether two specified instances of JET_DBID are equal.</span></span>

<span data-ttu-id="d8304-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d8304-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d8304-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d8304-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d8304-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8304-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_DBID, _
    rhs As JET_DBID _
) As Boolean
'Usage
Dim lhs As JET_DBID
Dim rhs As JET_DBID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_DBID lhs,
    JET_DBID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="d8304-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8304-108">Parameters</span></span>

  - <span data-ttu-id="d8304-109">LHS</span><span class="sxs-lookup"><span data-stu-id="d8304-109">lhs</span></span>  
    <span data-ttu-id="d8304-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d8304-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d8304-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d8304-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="d8304-112">rhs</span><span class="sxs-lookup"><span data-stu-id="d8304-112">rhs</span></span>  
    <span data-ttu-id="d8304-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d8304-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d8304-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d8304-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d8304-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8304-115">Return value</span></span>

<span data-ttu-id="d8304-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d8304-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="d8304-117">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="d8304-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8304-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8304-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d8304-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="d8304-119">Reference</span></span>

[<span data-ttu-id="d8304-120">Estructura de JET_DBID</span><span class="sxs-lookup"><span data-stu-id="d8304-120">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="d8304-121">Miembros de JET_DBID</span><span class="sxs-lookup"><span data-stu-id="d8304-121">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="d8304-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d8304-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
