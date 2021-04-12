---
description: 'Más información acerca de: JET_THREADSTATS. Operador de resta'
title: JET_THREADSTATS. Operador de resta (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39512217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a41455f05b91a582a1d8aae824ca5b426628cf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275193"
---
# <a name="jet_threadstatssubtraction-operator"></a><span data-ttu-id="2030c-103">JET_THREADSTATS. Operador de resta</span><span class="sxs-lookup"><span data-stu-id="2030c-103">JET_THREADSTATS.Subtraction operator</span></span>

<span data-ttu-id="2030c-104">Calcular la diferencia en estadísticas entre dos estructuras de JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="2030c-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="2030c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2030c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2030c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2030c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2030c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2030c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 - t2)
```

``` csharp
public static JET_THREADSTATS operator -(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="2030c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2030c-108">Parameters</span></span>

  - <span data-ttu-id="2030c-109">t1</span><span class="sxs-lookup"><span data-stu-id="2030c-109">t1</span></span>  
    <span data-ttu-id="2030c-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2030c-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="2030c-111">Primer JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="2030c-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="2030c-112">T2</span><span class="sxs-lookup"><span data-stu-id="2030c-112">t2</span></span>  
    <span data-ttu-id="2030c-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2030c-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="2030c-114">Segundo JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="2030c-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2030c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2030c-115">Return value</span></span>

<span data-ttu-id="2030c-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2030c-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="2030c-117">JET_THREADSTATS que contiene la diferencia entre T1 y T2.</span><span class="sxs-lookup"><span data-stu-id="2030c-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2030c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2030c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2030c-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="2030c-119">Reference</span></span>

[<span data-ttu-id="2030c-120">Estructura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="2030c-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="2030c-121">Miembros de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="2030c-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="2030c-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="2030c-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
