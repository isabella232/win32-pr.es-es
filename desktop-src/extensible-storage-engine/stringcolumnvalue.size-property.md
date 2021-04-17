---
description: 'Más información sobre: StringColumnValue. Size (propiedad)'
title: StringColumnValue. Size (propiedad)
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104025
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.StringColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fdd9613061e049d45c4b9bce2772ff580ea1a0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716743"
---
# <a name="stringcolumnvaluesize-property"></a><span data-ttu-id="d2454-103">StringColumnValue. Size (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d2454-103">StringColumnValue.Size property</span></span>

<span data-ttu-id="d2454-104">Obtiene el tamaño del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="d2454-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="d2454-105">Esto devuelve 0 para las columnas de tamaño variable (es decir, binary y String).</span><span class="sxs-lookup"><span data-stu-id="d2454-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="d2454-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2454-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2454-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2454-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2454-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2454-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="d2454-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d2454-109">Property value</span></span>

<span data-ttu-id="d2454-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d2454-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2454-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2454-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2454-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="d2454-112">Reference</span></span>

[<span data-ttu-id="d2454-113">Clase StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="d2454-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="d2454-114">Miembros de StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="d2454-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="d2454-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d2454-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
