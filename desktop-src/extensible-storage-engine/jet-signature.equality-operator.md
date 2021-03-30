---
description: 'Más información acerca de: JET_SIGNATURE. Operador de igualdad'
title: JET_SIGNATURE. Operador de igualdad
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011510343f79724c2c529c2b6b18537b43facbef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810501"
---
# <a name="jet_signatureequality-operator"></a><span data-ttu-id="bd649-103">JET_SIGNATURE. Operador de igualdad</span><span class="sxs-lookup"><span data-stu-id="bd649-103">JET_SIGNATURE.Equality operator</span></span>

<span data-ttu-id="bd649-104">Determina si dos instancias especificadas de JET_SIGNATURE son iguales.</span><span class="sxs-lookup"><span data-stu-id="bd649-104">Determines whether two specified instances of JET_SIGNATURE are equal.</span></span>

<span data-ttu-id="bd649-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bd649-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bd649-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bd649-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bd649-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd649-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="bd649-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd649-108">Parameters</span></span>

  - <span data-ttu-id="bd649-109">LHS</span><span class="sxs-lookup"><span data-stu-id="bd649-109">lhs</span></span>  
    <span data-ttu-id="bd649-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="bd649-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="bd649-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="bd649-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="bd649-112">rhs</span><span class="sxs-lookup"><span data-stu-id="bd649-112">rhs</span></span>  
    <span data-ttu-id="bd649-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="bd649-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="bd649-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="bd649-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="bd649-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd649-115">Return value</span></span>

<span data-ttu-id="bd649-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="bd649-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="bd649-117">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="bd649-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd649-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd649-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bd649-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="bd649-119">Reference</span></span>

[<span data-ttu-id="bd649-120">Estructura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="bd649-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="bd649-121">Miembros de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="bd649-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="bd649-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bd649-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
