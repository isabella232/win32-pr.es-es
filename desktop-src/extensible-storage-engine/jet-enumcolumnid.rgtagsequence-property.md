---
description: 'Más información acerca de: propiedad JET_ENUMCOLUMNID. rgtagSequence'
title: Propiedad JET_ENUMCOLUMNID. rgtagSequence
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808545"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a><span data-ttu-id="5ade7-103">Propiedad JET_ENUMCOLUMNID. rgtagSequence</span><span class="sxs-lookup"><span data-stu-id="5ade7-103">JET_ENUMCOLUMNID.rgtagSequence property</span></span>

<span data-ttu-id="5ade7-104">Obtiene o establece la matriz de índices basados en uno en la matriz de valores de columna de una columna determinada.</span><span class="sxs-lookup"><span data-stu-id="5ade7-104">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="5ade7-105">Un único elemento es un itagSequence que se define en JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="5ade7-105">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="5ade7-106">Un valor de itagSequence de 0 (cero) significa "SKIP".</span><span class="sxs-lookup"><span data-stu-id="5ade7-106">An itagSequence of 0 (zero) means "skip".</span></span> <span data-ttu-id="5ade7-107">Un itagSequence de 1 significa devolver el valor de la primera columna de la columna, 2 significa el segundo, etc.</span><span class="sxs-lookup"><span data-stu-id="5ade7-107">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

<span data-ttu-id="5ade7-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5ade7-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5ade7-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5ade7-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ade7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ade7-110">Syntax</span></span>

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5ade7-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5ade7-111">Property value</span></span>

<span data-ttu-id="5ade7-112">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="5ade7-112">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="5ade7-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ade7-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ade7-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="5ade7-114">Reference</span></span>

[<span data-ttu-id="5ade7-115">JET_ENUMCOLUMNID (clase)</span><span class="sxs-lookup"><span data-stu-id="5ade7-115">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="5ade7-116">Miembros de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="5ade7-116">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="5ade7-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5ade7-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
