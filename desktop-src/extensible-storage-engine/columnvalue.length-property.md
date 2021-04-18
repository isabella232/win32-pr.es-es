---
description: 'Más información sobre: ColumnValue. length (propiedad)'
title: ColumnValue. length (propiedad)
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707483"
---
# <a name="columnvaluelength-property"></a><span data-ttu-id="246d6-103">ColumnValue. length (propiedad)</span><span class="sxs-lookup"><span data-stu-id="246d6-103">ColumnValue.Length property</span></span>

<span data-ttu-id="246d6-104">Obtiene la longitud de bytes de un valor de columna, que es cero si la columna es null; de lo contrario, coincide con el tamaño de las columnas de tamaño fijo y representa el valor real de longitud de bytes para las columnas de tamaño variable (es decir, binario y cadena).</span><span class="sxs-lookup"><span data-stu-id="246d6-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for fixed-size columns and represent the actual value byte length for variable sized columns (i.e. binary and string).</span></span> <span data-ttu-id="246d6-105">En el caso de las cadenas, la longitud se determina en dos bytes por carácter.</span><span class="sxs-lookup"><span data-stu-id="246d6-105">For strings the length is determined in assumption two bytes per character.</span></span>

<span data-ttu-id="246d6-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="246d6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="246d6-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="246d6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="246d6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="246d6-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="246d6-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="246d6-109">Property value</span></span>

<span data-ttu-id="246d6-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="246d6-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="246d6-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="246d6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="246d6-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="246d6-112">Reference</span></span>

[<span data-ttu-id="246d6-113">Clase ColumnValue</span><span class="sxs-lookup"><span data-stu-id="246d6-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="246d6-114">Miembros de ColumnValue</span><span class="sxs-lookup"><span data-stu-id="246d6-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="246d6-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="246d6-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
