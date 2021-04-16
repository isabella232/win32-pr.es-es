---
description: 'Más información acerca de: propiedad JET_RECSIZE. cbOverhead'
title: Propiedad JET_RECSIZE. cbOverhead (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbOverhead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cboverhead(v=EXCHG.10)
ms:contentKeyID: 39514763
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbOverhead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e7318428ef4b50a08a05f5021d293ad1d8d78cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696228"
---
# <a name="jet_recsizecboverhead-property"></a><span data-ttu-id="e6a45-103">Propiedad JET_RECSIZE. cbOverhead</span><span class="sxs-lookup"><span data-stu-id="e6a45-103">JET_RECSIZE.cbOverhead property</span></span>

<span data-ttu-id="e6a45-104">Obtiene la sobrecarga de la estructura de registro ESENT para este registro.</span><span class="sxs-lookup"><span data-stu-id="e6a45-104">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="e6a45-105">Esto incluye el tamaño de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="e6a45-105">This includes the record's key size.</span></span>

<span data-ttu-id="e6a45-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6a45-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e6a45-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6a45-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a45-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6a45-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbOverhead As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbOverhead
```

``` csharp
public long cbOverhead { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="e6a45-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6a45-109">Property value</span></span>

<span data-ttu-id="e6a45-110">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="e6a45-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6a45-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6a45-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6a45-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="e6a45-112">Reference</span></span>

[<span data-ttu-id="e6a45-113">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e6a45-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="e6a45-114">Miembros de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e6a45-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="e6a45-115">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="e6a45-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
