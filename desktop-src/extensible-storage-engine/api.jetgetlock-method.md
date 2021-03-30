---
description: 'Más información sobre: API. JetGetLock (método)'
title: Método API. JetGetLock
TOCTitle: 'JetGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetlock(v=EXCHG.10)
ms:contentKeyID: 55100732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8480b6ac2eab84a0299e0bb3d480908e4f646fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907783"
---
# <a name="apijetgetlock-method"></a><span data-ttu-id="04009-103">Método API. JetGetLock</span><span class="sxs-lookup"><span data-stu-id="04009-103">Api.JetGetLock method</span></span>

<span data-ttu-id="04009-104">Reserve explícitamente la capacidad de actualizar una fila, un bloqueo de escritura o impedir explícitamente que una fila se actualice en cualquier otra sesión, bloqueo de lectura.</span><span class="sxs-lookup"><span data-stu-id="04009-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="04009-105">Normalmente, los bloqueos de escritura de filas se adquieren implícitamente como resultado de la actualización de filas.</span><span class="sxs-lookup"><span data-stu-id="04009-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="04009-106">Normalmente, los bloqueos de lectura no son necesarios debido a las versiones de registros.</span><span class="sxs-lookup"><span data-stu-id="04009-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="04009-107">Sin embargo, en algunos casos, una transacción puede desear bloquear explícitamente una fila para aplicar la serialización o asegurarse de que una operación posterior se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="04009-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="04009-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04009-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04009-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="04009-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04009-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04009-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbitApi.JetGetLock(sesid, tableid, grbit)
```

``` csharp
public static void JetGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="04009-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04009-111">Parameters</span></span>

  - <span data-ttu-id="04009-112">sesid</span><span class="sxs-lookup"><span data-stu-id="04009-112">sesid</span></span>  
    <span data-ttu-id="04009-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="04009-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="04009-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="04009-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="04009-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="04009-115">tableid</span></span>  
    <span data-ttu-id="04009-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="04009-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="04009-117">Cursor que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="04009-117">The cursor to use.</span></span> <span data-ttu-id="04009-118">Se adquirirá un bloqueo en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="04009-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="04009-119">grbit</span><span class="sxs-lookup"><span data-stu-id="04009-119">grbit</span></span>  
    <span data-ttu-id="04009-120">Tipo: [Microsoft. ISAM. esent. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="04009-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="04009-121">Opciones de bloqueo, use esta opción para especificar el tipo de bloqueo que se debe obtener.</span><span class="sxs-lookup"><span data-stu-id="04009-121">Lock options, use this to specify which type of lock to obtain.</span></span>

## <a name="see-also"></a><span data-ttu-id="04009-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="04009-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04009-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="04009-123">Reference</span></span>

[<span data-ttu-id="04009-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="04009-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="04009-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="04009-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="04009-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="04009-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
