---
description: 'Más información acerca de: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907770"
---
# <a name="jet_sesid"></a><span data-ttu-id="0d229-103">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0d229-103">JET_SESID</span></span>


<span data-ttu-id="0d229-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0d229-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_sesid"></a><span data-ttu-id="0d229-105">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0d229-105">JET_SESID</span></span>

<span data-ttu-id="0d229-106">El tipo de datos **JET_SESID** contiene un identificador de la sesión que se va a usar para una llamada a la API de jet.</span><span class="sxs-lookup"><span data-stu-id="0d229-106">The **JET_SESID** data type contains a handle to the session to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a><span data-ttu-id="0d229-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0d229-107">Data Types</span></span>

<span data-ttu-id="0d229-108">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0d229-108">JET_SESID</span></span>

<span data-ttu-id="0d229-109">Se puede utilizar **null** o [JET_sesidNil](./invalid-handle-constants.md) para indicar un identificador de sesión no válido.</span><span class="sxs-lookup"><span data-stu-id="0d229-109">Either **NULL** or [JET_sesidNil](./invalid-handle-constants.md) can be used to indicate an invalid session handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="0d229-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d229-110">Remarks</span></span>

<span data-ttu-id="0d229-111">Una sesión es el contexto de transacción del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0d229-111">A session is the transaction context of the database engine.</span></span> <span data-ttu-id="0d229-112">Se puede usar para iniciar, confirmar o anular transacciones que afectan a la visibilidad y la durabilidad de los cambios realizados por esta u otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="0d229-112">It can be used to begin, commit, or abort transactions that affect the visibility and durability of changes that are made by this or other sessions.</span></span>

<span data-ttu-id="0d229-113">Una transacción se puede iniciar mediante [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d229-113">A transaction can be started using [JetBeginTransaction](./jetbegintransaction-function.md).</span></span> <span data-ttu-id="0d229-114">Se puede crear una sesión mediante [JetBeginSession](./jetbeginsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d229-114">A session may be created using [JetBeginSession](./jetbeginsession-function.md).</span></span> <span data-ttu-id="0d229-115">El número máximo de sesiones que se pueden crear en un momento determinado se controla mediante [JET_paramMaxSessions](./resource-parameters.md), que se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d229-115">The maximum number of sessions that can be created at any one time is controlled by [JET_paramMaxSessions](./resource-parameters.md), which can be configured by means of [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="0d229-116">Una sesión finaliza explícitamente mediante una llamada a [JetEndSession](./jetendsession-function.md) o termina implícitamente mediante una llamada a [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d229-116">A session is explicitly ended by a call to [JetEndSession](./jetendsession-function.md) or implicitly ended by a call to [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="0d229-117">Cada sesión solo puede ser utilizada por un subproceso a la vez.</span><span class="sxs-lookup"><span data-stu-id="0d229-117">Each session can only be used by one thread at a time.</span></span> <span data-ttu-id="0d229-118">Además, el comportamiento predeterminado del motor es restringir el uso de una sesión al mismo subproceso desde el momento en que se realiza la primera llamada a [JetBeginTransaction](./jetbegintransaction-function.md) hasta el momento en que se realiza la llamada coincidente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0d229-118">In addition, the default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to [JetBeginTransaction](./jetbegintransaction-function.md) is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="0d229-119">Este comportamiento se puede cambiar para quitar esta segunda restricción mediante la configuración de un contexto de sesión personalizado mediante [JetSetSessionContext](./jetsetsessioncontext-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="0d229-119">This behavior can be changed to remove this second restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="0d229-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d229-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d229-121"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0d229-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0d229-122">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0d229-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d229-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0d229-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0d229-124">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0d229-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d229-125"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0d229-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0d229-126">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="0d229-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0d229-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d229-127">See Also</span></span>

[<span data-ttu-id="0d229-128">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="0d229-128">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="0d229-129">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="0d229-129">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="0d229-130">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="0d229-130">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="0d229-131">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="0d229-131">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="0d229-132">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="0d229-132">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="0d229-133">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="0d229-133">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="0d229-134">JetRollback</span><span class="sxs-lookup"><span data-stu-id="0d229-134">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="0d229-135">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="0d229-135">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="0d229-136">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0d229-136">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="0d229-137">JetTerm</span><span class="sxs-lookup"><span data-stu-id="0d229-137">JetTerm</span></span>](./jetterm-function.md)
