---
description: 'Más información acerca de: propiedad JET_RETINFO. itagSequence'
title: Propiedad JET_RETINFO. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278942"
---
# <a name="jet_retinfoitagsequence-property"></a><span data-ttu-id="9ea71-103">Propiedad JET_RETINFO. itagSequence</span><span class="sxs-lookup"><span data-stu-id="9ea71-103">JET_RETINFO.itagSequence property</span></span>

<span data-ttu-id="9ea71-104">Obtiene o establece el número de secuencia de un valor en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="9ea71-104">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="9ea71-105">La matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="9ea71-105">The array of values is one-based.</span></span> <span data-ttu-id="9ea71-106">El primer valor es Sequence 1, no 0.</span><span class="sxs-lookup"><span data-stu-id="9ea71-106">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="9ea71-107">Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence.</span><span class="sxs-lookup"><span data-stu-id="9ea71-107">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<span data-ttu-id="9ea71-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9ea71-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9ea71-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9ea71-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea71-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ea71-110">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="9ea71-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9ea71-111">Property value</span></span>

<span data-ttu-id="9ea71-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9ea71-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ea71-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ea71-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ea71-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="9ea71-114">Reference</span></span>

[<span data-ttu-id="9ea71-115">JET_RETINFO (clase)</span><span class="sxs-lookup"><span data-stu-id="9ea71-115">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="9ea71-116">Miembros de JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="9ea71-116">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="9ea71-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9ea71-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
