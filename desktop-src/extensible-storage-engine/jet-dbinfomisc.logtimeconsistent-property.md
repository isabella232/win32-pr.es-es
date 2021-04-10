---
description: 'Más información acerca de: propiedad JET_DBINFOMISC. logtimeConsistent'
title: Propiedad JET_DBINFOMISC. logtimeConsistent
TOCTitle: 'logtimeConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimeconsistent(v=EXCHG.10)
ms:contentKeyID: 39513228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeConsistent
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d46302373df17e147095c5ac5c37f02ffef1eb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153804"
---
# <a name="jet_dbinfomisclogtimeconsistent-property"></a><span data-ttu-id="5a5db-103">Propiedad JET_DBINFOMISC. logtimeConsistent</span><span class="sxs-lookup"><span data-stu-id="5a5db-103">JET_DBINFOMISC.logtimeConsistent property</span></span>

<span data-ttu-id="5a5db-104">Obtiene la hora a la que se realizó la coherencia de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5a5db-104">Gets the time when the database was made consistent.</span></span> <span data-ttu-id="5a5db-105">Este valor es NULL si la base de datos es incoherente.</span><span class="sxs-lookup"><span data-stu-id="5a5db-105">This value is null if the database is inconsistent.</span></span>

<span data-ttu-id="5a5db-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a5db-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a5db-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a5db-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a5db-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a5db-108">Syntax</span></span>

``` vb
'Declaration
Public Property logtimeConsistent As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeConsistent
```

``` csharp
public JET_LOGTIME logtimeConsistent { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="5a5db-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5a5db-109">Property value</span></span>

<span data-ttu-id="5a5db-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="5a5db-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a5db-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a5db-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a5db-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="5a5db-112">Reference</span></span>

[<span data-ttu-id="5a5db-113">JET_DBINFOMISC (clase)</span><span class="sxs-lookup"><span data-stu-id="5a5db-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="5a5db-114">Miembros de JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="5a5db-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="5a5db-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5a5db-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
