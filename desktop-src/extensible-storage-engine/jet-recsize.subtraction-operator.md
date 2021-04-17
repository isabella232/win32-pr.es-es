---
description: 'Más información acerca de: JET_RECSIZE. Operador de resta'
title: JET_RECSIZE. Operador de resta (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39516016
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be60da4aeeab78794f087e9c7095a16dd39eb378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706792"
---
# <a name="jet_recsizesubtraction-operator"></a><span data-ttu-id="bb0ee-103">JET_RECSIZE. Operador de resta</span><span class="sxs-lookup"><span data-stu-id="bb0ee-103">JET_RECSIZE.Subtraction operator</span></span>

<span data-ttu-id="bb0ee-104">Calcular la diferencia en tamaños entre dos estructuras JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="bb0ee-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="bb0ee-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bb0ee-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="bb0ee-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bb0ee-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0ee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb0ee-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left - right)
```

``` csharp
public static JET_RECSIZE operator -(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="bb0ee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb0ee-108">Parameters</span></span>

  - <span data-ttu-id="bb0ee-109">izquierda</span><span class="sxs-lookup"><span data-stu-id="bb0ee-109">left</span></span>  
    <span data-ttu-id="bb0ee-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="bb0ee-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="bb0ee-111">Primer JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="bb0ee-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="bb0ee-112">right</span><span class="sxs-lookup"><span data-stu-id="bb0ee-112">right</span></span>  
    <span data-ttu-id="bb0ee-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="bb0ee-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="bb0ee-114">Segundo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="bb0ee-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="bb0ee-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb0ee-115">Return value</span></span>

<span data-ttu-id="bb0ee-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="bb0ee-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="bb0ee-117">JET_RECSIZE que contiene la diferencia en tamaños entre la izquierda y la derecha.</span><span class="sxs-lookup"><span data-stu-id="bb0ee-117">A JET_RECSIZE containing the difference in sizes between left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb0ee-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb0ee-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bb0ee-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="bb0ee-119">Reference</span></span>

[<span data-ttu-id="bb0ee-120">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="bb0ee-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="bb0ee-121">Miembros de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="bb0ee-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="bb0ee-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="bb0ee-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
