---
description: 'Más información acerca de: propiedad JET_SETCOLUMN. itagSequence'
title: Propiedad JET_SETCOLUMN. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103935
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7870f6e29cf8f6810c6aa41049868fbceb370dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715033"
---
# <a name="jet_setcolumnitagsequence-property"></a><span data-ttu-id="5041a-103">Propiedad JET_SETCOLUMN. itagSequence</span><span class="sxs-lookup"><span data-stu-id="5041a-103">JET_SETCOLUMN.itagSequence property</span></span>

<span data-ttu-id="5041a-104">Obtiene o establece el número de secuencia del valor de una columna con varios valores que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="5041a-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="5041a-105">La matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="5041a-105">The array of values is one-based.</span></span> <span data-ttu-id="5041a-106">El primer valor es Sequence 1, no 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5041a-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="5041a-107">Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence si ese valor se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="5041a-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="5041a-108">Un valor de 0 (cero) significa agregar una nueva instancia de valor de columna al final de la secuencia de valores de columna.</span><span class="sxs-lookup"><span data-stu-id="5041a-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="5041a-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5041a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5041a-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5041a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5041a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5041a-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5041a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5041a-112">Property value</span></span>

<span data-ttu-id="5041a-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5041a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5041a-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="5041a-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5041a-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="5041a-115">Reference</span></span>

[<span data-ttu-id="5041a-116">JET_SETCOLUMN (clase)</span><span class="sxs-lookup"><span data-stu-id="5041a-116">JET_SETCOLUMN class</span></span>](./jet-setcolumn-class.md)

[<span data-ttu-id="5041a-117">Miembros de JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="5041a-117">JET_SETCOLUMN members</span></span>](./jet-setcolumn-members.md)

[<span data-ttu-id="5041a-118">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5041a-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
