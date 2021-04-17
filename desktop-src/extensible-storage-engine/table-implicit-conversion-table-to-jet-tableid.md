---
description: Más información acerca de la conversión implícita de tabla (tabla a JET_TABLEID)
title: Conversión implícita de tabla (tabla a JET_TABLEID)
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720628"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a><span data-ttu-id="15f96-103">Conversión implícita de tabla (tabla a JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="15f96-103">Table Implicit conversion (Table to JET_TABLEID)</span></span>

<span data-ttu-id="15f96-104">Operador de conversión implícita de una tabla a una JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="15f96-104">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="15f96-105">Esto permite usar una tabla con las API que esperan un JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="15f96-105">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span>

<span data-ttu-id="15f96-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="15f96-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="15f96-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="15f96-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="15f96-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15f96-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a><span data-ttu-id="15f96-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15f96-109">Parameters</span></span>

  - <span data-ttu-id="15f96-110">table</span><span class="sxs-lookup"><span data-stu-id="15f96-110">table</span></span>  
    <span data-ttu-id="15f96-111">Tipo: [Microsoft. ISAM. esent. Interop. Table](./table-class.md)</span><span class="sxs-lookup"><span data-stu-id="15f96-111">Type: [Microsoft.Isam.Esent.Interop.Table](./table-class.md)</span></span>  
    
    <span data-ttu-id="15f96-112">Tabla que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="15f96-112">The table to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="15f96-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15f96-113">Return value</span></span>

<span data-ttu-id="15f96-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="15f96-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
<span data-ttu-id="15f96-115">JET_TABLEID de la tabla.</span><span class="sxs-lookup"><span data-stu-id="15f96-115">The JET_TABLEID of the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="15f96-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="15f96-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="15f96-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="15f96-117">Reference</span></span>

[<span data-ttu-id="15f96-118">Table (clase)</span><span class="sxs-lookup"><span data-stu-id="15f96-118">Table class</span></span>](./table-class.md)

[<span data-ttu-id="15f96-119">Miembros de tabla</span><span class="sxs-lookup"><span data-stu-id="15f96-119">Table members</span></span>](./table-members.md)

[<span data-ttu-id="15f96-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="15f96-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
