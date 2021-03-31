---
description: 'Más información acerca de: propiedad JET_RETRIEVECOLUMN. itagSequence'
title: Propiedad JET_RETRIEVECOLUMN. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103882
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f2885d5bf467d282ef97172323a8de44980ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911754"
---
# <a name="jet_retrievecolumnitagsequence-property"></a><span data-ttu-id="7eeb5-103">Propiedad JET_RETRIEVECOLUMN. itagSequence</span><span class="sxs-lookup"><span data-stu-id="7eeb5-103">JET_RETRIEVECOLUMN.itagSequence property</span></span>

<span data-ttu-id="7eeb5-104">Obtiene o establece el número de secuencia de los valores contenidos en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="7eeb5-104">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="7eeb5-105">Si el valor de itagSequence es 0, se devuelve el número de instancias de una columna con varios valores en lugar de datos de columna.</span><span class="sxs-lookup"><span data-stu-id="7eeb5-105">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span>

<span data-ttu-id="7eeb5-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7eeb5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7eeb5-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7eeb5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7eeb5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eeb5-108">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7eeb5-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7eeb5-109">Property value</span></span>

<span data-ttu-id="7eeb5-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7eeb5-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7eeb5-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eeb5-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7eeb5-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="7eeb5-112">Reference</span></span>

[<span data-ttu-id="7eeb5-113">JET_RETRIEVECOLUMN (clase)</span><span class="sxs-lookup"><span data-stu-id="7eeb5-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="7eeb5-114">Miembros de JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="7eeb5-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="7eeb5-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7eeb5-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
