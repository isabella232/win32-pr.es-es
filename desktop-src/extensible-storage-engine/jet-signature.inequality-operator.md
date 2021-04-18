---
description: 'Más información acerca de: JET_SIGNATURE. Operador de desigualdad'
title: JET_SIGNATURE. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 646b97f37aea55ee3e9d1aa24e80b9d26ea82469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706789"
---
# <a name="jet_signatureinequality-operator"></a><span data-ttu-id="d2e81-103">JET_SIGNATURE. Operador de desigualdad</span><span class="sxs-lookup"><span data-stu-id="d2e81-103">JET_SIGNATURE.Inequality operator</span></span>

<span data-ttu-id="d2e81-104">Determina si dos instancias especificadas de JET_SIGNATURE no son iguales.</span><span class="sxs-lookup"><span data-stu-id="d2e81-104">Determines whether two specified instances of JET_SIGNATURE are not equal.</span></span>

<span data-ttu-id="d2e81-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2e81-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2e81-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2e81-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e81-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2e81-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="d2e81-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2e81-108">Parameters</span></span>

  - <span data-ttu-id="d2e81-109">LHS</span><span class="sxs-lookup"><span data-stu-id="d2e81-109">lhs</span></span>  
    <span data-ttu-id="d2e81-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d2e81-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="d2e81-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d2e81-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2e81-112">rhs</span><span class="sxs-lookup"><span data-stu-id="d2e81-112">rhs</span></span>  
    <span data-ttu-id="d2e81-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d2e81-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="d2e81-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d2e81-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d2e81-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2e81-115">Return value</span></span>

<span data-ttu-id="d2e81-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d2e81-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="d2e81-117">True si las dos instancias de no son iguales.</span><span class="sxs-lookup"><span data-stu-id="d2e81-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2e81-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2e81-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2e81-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="d2e81-119">Reference</span></span>

[<span data-ttu-id="d2e81-120">Estructura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="d2e81-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="d2e81-121">Miembros de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="d2e81-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="d2e81-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d2e81-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
