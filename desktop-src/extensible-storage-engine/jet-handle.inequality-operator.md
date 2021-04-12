---
description: 'Más información acerca de: JET_HANDLE. Operador de desigualdad'
title: JET_HANDLE. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5feee9739ad57103b71786ae7d1cdbf5f7e858ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361362"
---
# <a name="jet_handleinequality-operator"></a><span data-ttu-id="77caf-103">JET_HANDLE. Operador de desigualdad</span><span class="sxs-lookup"><span data-stu-id="77caf-103">JET_HANDLE.Inequality operator</span></span>

<span data-ttu-id="77caf-104">Determina si dos instancias especificadas de JET_HANDLE no son iguales.</span><span class="sxs-lookup"><span data-stu-id="77caf-104">Determines whether two specified instances of JET_HANDLE are not equal.</span></span>

<span data-ttu-id="77caf-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="77caf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="77caf-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="77caf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="77caf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77caf-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="77caf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77caf-108">Parameters</span></span>

  - <span data-ttu-id="77caf-109">LHS</span><span class="sxs-lookup"><span data-stu-id="77caf-109">lhs</span></span>  
    <span data-ttu-id="77caf-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="77caf-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="77caf-111">Primera instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="77caf-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="77caf-112">rhs</span><span class="sxs-lookup"><span data-stu-id="77caf-112">rhs</span></span>  
    <span data-ttu-id="77caf-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="77caf-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="77caf-114">Segunda instancia que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="77caf-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="77caf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77caf-115">Return value</span></span>

<span data-ttu-id="77caf-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="77caf-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="77caf-117">True si las dos instancias de no son iguales.</span><span class="sxs-lookup"><span data-stu-id="77caf-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="77caf-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="77caf-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="77caf-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="77caf-119">Reference</span></span>

[<span data-ttu-id="77caf-120">Estructura de JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="77caf-120">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="77caf-121">Miembros de JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="77caf-121">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="77caf-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="77caf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
