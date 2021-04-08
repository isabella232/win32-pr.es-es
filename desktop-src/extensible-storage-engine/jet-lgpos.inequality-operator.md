---
description: 'Más información acerca de: JET_LGPOS. Operador de desigualdad'
title: JET_LGPOS. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511705
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e324131591f1d6bee3c00e6260f31f6580ec086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002512"
---
# <a name="jet_lgposinequality-operator"></a><span data-ttu-id="badb3-103">JET_LGPOS. Operador de desigualdad</span><span class="sxs-lookup"><span data-stu-id="badb3-103">JET_LGPOS.Inequality operator</span></span>

<span data-ttu-id="badb3-104">Determina si dos instancias especificadas de JET_LGPOS no son iguales.</span><span class="sxs-lookup"><span data-stu-id="badb3-104">Determines whether two specified instances of JET_LGPOS are not equal.</span></span>

<span data-ttu-id="badb3-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="badb3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="badb3-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="badb3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="badb3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="badb3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="badb3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="badb3-108">Parameters</span></span>

  - <span data-ttu-id="badb3-109">LHS</span><span class="sxs-lookup"><span data-stu-id="badb3-109">lhs</span></span>  
    <span data-ttu-id="badb3-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="badb3-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="badb3-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="badb3-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="badb3-112">rhs</span><span class="sxs-lookup"><span data-stu-id="badb3-112">rhs</span></span>  
    <span data-ttu-id="badb3-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="badb3-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="badb3-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="badb3-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="badb3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="badb3-115">Return value</span></span>

<span data-ttu-id="badb3-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="badb3-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="badb3-117">True si las dos instancias de no son iguales.</span><span class="sxs-lookup"><span data-stu-id="badb3-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="badb3-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="badb3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="badb3-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="badb3-119">Reference</span></span>

[<span data-ttu-id="badb3-120">Estructura de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="badb3-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="badb3-121">Miembros de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="badb3-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="badb3-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="badb3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
