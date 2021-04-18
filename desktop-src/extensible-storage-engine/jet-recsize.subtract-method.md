---
description: 'Más información acerca de: JET_RECSIZE. Resta (método)'
title: JET_RECSIZE. Método resta (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.subtract(v=EXCHG.10)
ms:contentKeyID: 39514591
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9789dac524e57ea762243ed47d513d262d7ebb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706793"
---
# <a name="jet_recsizesubtract-method"></a><span data-ttu-id="981dc-103">JET_RECSIZE. Resta (método)</span><span class="sxs-lookup"><span data-stu-id="981dc-103">JET_RECSIZE.Subtract method</span></span>

<span data-ttu-id="981dc-104">Calcular la diferencia en tamaños entre dos estructuras JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="981dc-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="981dc-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="981dc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="981dc-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="981dc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="981dc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="981dc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Subtract(s1, s2)
```

``` csharp
public static JET_RECSIZE Subtract(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="981dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="981dc-108">Parameters</span></span>

  - <span data-ttu-id="981dc-109">s1</span><span class="sxs-lookup"><span data-stu-id="981dc-109">s1</span></span>  
    <span data-ttu-id="981dc-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="981dc-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="981dc-111">Primer JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="981dc-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="981dc-112">s2</span><span class="sxs-lookup"><span data-stu-id="981dc-112">s2</span></span>  
    <span data-ttu-id="981dc-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="981dc-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="981dc-114">Segundo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="981dc-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="981dc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="981dc-115">Return value</span></span>

<span data-ttu-id="981dc-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="981dc-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="981dc-117">JET_RECSIZE que contiene la diferencia en los tamaños entre S1 y S2.</span><span class="sxs-lookup"><span data-stu-id="981dc-117">A JET_RECSIZE containing the difference in sizes between s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="981dc-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="981dc-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="981dc-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="981dc-119">Reference</span></span>

[<span data-ttu-id="981dc-120">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="981dc-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="981dc-121">Miembros de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="981dc-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="981dc-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="981dc-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
