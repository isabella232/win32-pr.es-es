---
description: 'Más información sobre: JET_ENUMCOLUMNVALUE (clase)'
title: JET_ENUMCOLUMNVALUE (clase)
TOCTitle: JET_ENUMCOLUMNVALUE class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103622
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2066e6b4b3039ba150f17630afaef967c215823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720312"
---
# <a name="jet_enumcolumnvalue-class"></a><span data-ttu-id="cbf3b-103">JET_ENUMCOLUMNVALUE (clase)</span><span class="sxs-lookup"><span data-stu-id="cbf3b-103">JET_ENUMCOLUMNVALUE class</span></span>

<span data-ttu-id="cbf3b-104">Enumera los valores de columna de un registro mediante la función JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="cbf3b-104">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="cbf3b-105">[JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) devuelve una matriz de estructuras de JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="cbf3b-105">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="cbf3b-106">La matriz se devuelve en memoria que se asignó mediante la devolución de llamada que se proporcionó a esa función.</span><span class="sxs-lookup"><span data-stu-id="cbf3b-106">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cbf3b-107">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="cbf3b-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="cbf3b-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="cbf3b-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="cbf3b-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="cbf3b-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span></span>  

<span data-ttu-id="cbf3b-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cbf3b-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cbf3b-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cbf3b-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf3b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbf3b-112">Syntax</span></span>

``` vb
'Declaration
Public Class JET_ENUMCOLUMNVALUE
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
```

``` csharp
public class JET_ENUMCOLUMNVALUE
```

## <a name="thread-safety"></a><span data-ttu-id="cbf3b-113">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="cbf3b-113">Thread safety</span></span>

<span data-ttu-id="cbf3b-114">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="cbf3b-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cbf3b-115">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="cbf3b-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbf3b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbf3b-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cbf3b-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="cbf3b-117">Reference</span></span>

[<span data-ttu-id="cbf3b-118">Miembros de JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="cbf3b-118">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="cbf3b-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cbf3b-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
