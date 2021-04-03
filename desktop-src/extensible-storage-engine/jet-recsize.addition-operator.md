---
description: 'Más información acerca de: JET_RECSIZE. Operador de suma'
title: JET_RECSIZE. Operador de suma (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c41fae92f6177bf0c39138ad33988a74c482e0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808521"
---
# <a name="jet_recsizeaddition-operator"></a><span data-ttu-id="64712-103">JET_RECSIZE. Operador de suma</span><span class="sxs-lookup"><span data-stu-id="64712-103">JET_RECSIZE.Addition operator</span></span>

<span data-ttu-id="64712-104">Agregue los tamaños en dos estructuras de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="64712-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="64712-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="64712-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="64712-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="64712-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="64712-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64712-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="64712-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64712-108">Parameters</span></span>

  - <span data-ttu-id="64712-109">izquierda</span><span class="sxs-lookup"><span data-stu-id="64712-109">left</span></span>  
    <span data-ttu-id="64712-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="64712-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="64712-111">Primer JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="64712-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="64712-112">right</span><span class="sxs-lookup"><span data-stu-id="64712-112">right</span></span>  
    <span data-ttu-id="64712-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="64712-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="64712-114">Segundo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="64712-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="64712-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64712-115">Return value</span></span>

<span data-ttu-id="64712-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="64712-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="64712-117">JET_RECSIZE que contiene el resultado de agregar los tamaños a la izquierda y a la derecha.</span><span class="sxs-lookup"><span data-stu-id="64712-117">A JET_RECSIZE containing the result of adding the sizes in left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="64712-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="64712-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="64712-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="64712-119">Reference</span></span>

[<span data-ttu-id="64712-120">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="64712-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="64712-121">Miembros de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="64712-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="64712-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="64712-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
