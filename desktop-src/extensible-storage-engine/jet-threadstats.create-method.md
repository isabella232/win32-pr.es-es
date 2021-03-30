---
description: 'Más información acerca de: JET_THREADSTATS. Create (método)'
title: JET_THREADSTATS. Método Create (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816347"
---
# <a name="jet_threadstatscreate-method"></a><span data-ttu-id="910bd-103">JET_THREADSTATS. Create (método)</span><span class="sxs-lookup"><span data-stu-id="910bd-103">JET_THREADSTATS.Create method</span></span>

<span data-ttu-id="910bd-104">Cree un nuevo struct de [JET_THREADSTATS](./jet-threadstats-structure2.md) con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="910bd-104">Create a new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified valued.</span></span>

<span data-ttu-id="910bd-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="910bd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="910bd-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="910bd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="910bd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="910bd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a><span data-ttu-id="910bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="910bd-108">Parameters</span></span>

  - <span data-ttu-id="910bd-109">cPageReferenced</span><span class="sxs-lookup"><span data-stu-id="910bd-109">cPageReferenced</span></span>  
    <span data-ttu-id="910bd-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="910bd-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="910bd-111">Número de páginas visitadas.</span><span class="sxs-lookup"><span data-stu-id="910bd-111">Number of pages visited.</span></span>

<!-- end list -->

  - <span data-ttu-id="910bd-112">cPageRead</span><span class="sxs-lookup"><span data-stu-id="910bd-112">cPageRead</span></span>  
    <span data-ttu-id="910bd-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="910bd-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="910bd-114">Número de páginas leídas.</span><span class="sxs-lookup"><span data-stu-id="910bd-114">Number of pages read.</span></span>

<!-- end list -->

  - <span data-ttu-id="910bd-115">cPagePreread</span><span class="sxs-lookup"><span data-stu-id="910bd-115">cPagePreread</span></span>  
    <span data-ttu-id="910bd-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="910bd-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="910bd-117">Número de páginas preleídas.</span><span class="sxs-lookup"><span data-stu-id="910bd-117">Number of pages preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="910bd-118">cPageDirtied</span><span class="sxs-lookup"><span data-stu-id="910bd-118">cPageDirtied</span></span>  
    <span data-ttu-id="910bd-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="910bd-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="910bd-120">TNumber de páginas sucias.</span><span class="sxs-lookup"><span data-stu-id="910bd-120">TNumber of pages dirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="910bd-121">cPageRedirtied</span><span class="sxs-lookup"><span data-stu-id="910bd-121">cPageRedirtied</span></span>  
    <span data-ttu-id="910bd-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="910bd-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="910bd-123">Número de páginas resucias.</span><span class="sxs-lookup"><span data-stu-id="910bd-123">Number of pages redirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="910bd-124">cLogRecord</span><span class="sxs-lookup"><span data-stu-id="910bd-124">cLogRecord</span></span>  
    <span data-ttu-id="910bd-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="910bd-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="910bd-126">Número de entradas de registro generadas.</span><span class="sxs-lookup"><span data-stu-id="910bd-126">Number of log records generated.</span></span>

<!-- end list -->

  - <span data-ttu-id="910bd-127">cbLogRecord</span><span class="sxs-lookup"><span data-stu-id="910bd-127">cbLogRecord</span></span>  
    <span data-ttu-id="910bd-128">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="910bd-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="910bd-129">Bytes de entradas de registro escritas.</span><span class="sxs-lookup"><span data-stu-id="910bd-129">Bytes of log records written.</span></span>

#### <a name="return-value"></a><span data-ttu-id="910bd-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="910bd-130">Return value</span></span>

<span data-ttu-id="910bd-131">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="910bd-131">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="910bd-132">Nuevo struct de [JET_THREADSTATS](./jet-threadstats-structure2.md) con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="910bd-132">A new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified values.</span></span>  

## <a name="see-also"></a><span data-ttu-id="910bd-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="910bd-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="910bd-134">Referencia</span><span class="sxs-lookup"><span data-stu-id="910bd-134">Reference</span></span>

[<span data-ttu-id="910bd-135">Estructura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="910bd-135">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="910bd-136">Miembros de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="910bd-136">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="910bd-137">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="910bd-137">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
