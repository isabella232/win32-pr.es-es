---
description: 'Más información sobre: API. JetOSSnapshotFreeze (método)'
title: Método API. JetOSSnapshotFreeze
TOCTitle: 'JetOSSnapshotFreeze method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotfreeze(v=EXCHG.10)
ms:contentKeyID: 55100793
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7434cb79e90f99ab946c86a97559079352956fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279085"
---
# <a name="apijetossnapshotfreeze-method"></a><span data-ttu-id="432dd-103">Método API. JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="432dd-103">Api.JetOSSnapshotFreeze method</span></span>

<span data-ttu-id="432dd-104">Inicia una instantánea.</span><span class="sxs-lookup"><span data-stu-id="432dd-104">Starts a snapshot.</span></span> <span data-ttu-id="432dd-105">Mientras la instantánea está en curso, no se puede llevar a cabo ninguna actividad de escritura en disco por parte del motor.</span><span class="sxs-lookup"><span data-stu-id="432dd-105">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="432dd-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="432dd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="432dd-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="432dd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="432dd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="432dd-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotFreeze ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotFreezeGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotFreezeGrbitApi.JetOSSnapshotFreeze(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotFreeze(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotFreezeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="432dd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="432dd-109">Parameters</span></span>

  - <span data-ttu-id="432dd-110">instantánea</span><span class="sxs-lookup"><span data-stu-id="432dd-110">snapshot</span></span>  
    <span data-ttu-id="432dd-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="432dd-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="432dd-112">Sesión de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="432dd-112">The snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="432dd-113">numInstances</span><span class="sxs-lookup"><span data-stu-id="432dd-113">numInstances</span></span>  
    <span data-ttu-id="432dd-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="432dd-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="432dd-115">Devuelve el número de instancias que forman parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="432dd-115">Returns the number of instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="432dd-116">instances</span><span class="sxs-lookup"><span data-stu-id="432dd-116">instances</span></span>  
    <span data-ttu-id="432dd-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="432dd-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="432dd-118">Devuelve información sobre las instancias de que forman parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="432dd-118">Returns information about the instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="432dd-119">grbit</span><span class="sxs-lookup"><span data-stu-id="432dd-119">grbit</span></span>  
    <span data-ttu-id="432dd-120">Tipo: [Microsoft. ISAM. esent. Interop. SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="432dd-120">Type: [Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="432dd-121">Opciones de inmovilización de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="432dd-121">Snapshot freeze options.</span></span>

## <a name="see-also"></a><span data-ttu-id="432dd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="432dd-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="432dd-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="432dd-123">Reference</span></span>

[<span data-ttu-id="432dd-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="432dd-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="432dd-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="432dd-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="432dd-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="432dd-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
