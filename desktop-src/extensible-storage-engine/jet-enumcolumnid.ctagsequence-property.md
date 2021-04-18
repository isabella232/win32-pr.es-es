---
description: 'Más información acerca de: propiedad JET_ENUMCOLUMNID. ctagSequence'
title: Propiedad JET_ENUMCOLUMNID. ctagSequence
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e12c8c6a102cbb20862b3cc9859f7e632ade8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720360"
---
# <a name="jet_enumcolumnidctagsequence-property"></a><span data-ttu-id="2b7e7-103">Propiedad JET_ENUMCOLUMNID. ctagSequence</span><span class="sxs-lookup"><span data-stu-id="2b7e7-103">JET_ENUMCOLUMNID.ctagSequence property</span></span>

<span data-ttu-id="2b7e7-104">Obtiene o establece el recuento de valores de columna (por índice basado en uno) que se va a enumerar para el identificador de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="2b7e7-104">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="2b7e7-105">Si ctagSequence es 0 (cero), se omite rgtagSequence y se enumeran todos los valores de columna para el ID. de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="2b7e7-105">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="2b7e7-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2b7e7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2b7e7-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2b7e7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b7e7-108">Syntax</span></span>

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="2b7e7-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b7e7-109">Property value</span></span>

<span data-ttu-id="2b7e7-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2b7e7-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b7e7-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b7e7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2b7e7-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="2b7e7-112">Reference</span></span>

[<span data-ttu-id="2b7e7-113">JET_ENUMCOLUMNID (clase)</span><span class="sxs-lookup"><span data-stu-id="2b7e7-113">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="2b7e7-114">Miembros de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="2b7e7-114">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="2b7e7-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2b7e7-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
