---
description: 'Más información sobre: API. JetOSSnapshotPrepare (método)'
title: Método API. JetOSSnapshotPrepare
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ac304cf522e7c99a2495925da8571b2139c0a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279084"
---
# <a name="apijetossnapshotprepare-method"></a><span data-ttu-id="db301-103">Método API. JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="db301-103">Api.JetOSSnapshotPrepare method</span></span>

<span data-ttu-id="db301-104">Comienza los preparativos para una sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="db301-104">Begins the preparations for a snapshot session.</span></span> <span data-ttu-id="db301-105">Una sesión de instantáneas es un breve intervalo de tiempo en el que el motor no emite ninguna e/s de escritura en el disco, de modo que el motor puede participar en una sesión de instantáneas de volumen (cuando está controlada por un escritor de instantáneas).</span><span class="sxs-lookup"><span data-stu-id="db301-105">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="db301-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db301-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db301-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db301-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db301-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db301-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="db301-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db301-109">Parameters</span></span>

  - <span data-ttu-id="db301-110">instantánea</span><span class="sxs-lookup"><span data-stu-id="db301-110">snapshot</span></span>  
    <span data-ttu-id="db301-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db301-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="db301-112">Devuelve el identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="db301-112">Returns the ID of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="db301-113">grbit</span><span class="sxs-lookup"><span data-stu-id="db301-113">grbit</span></span>  
    <span data-ttu-id="db301-114">Tipo: [Microsoft. ISAM. esent. Interop. SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="db301-114">Type: [Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="db301-115">Opciones de instantánea.</span><span class="sxs-lookup"><span data-stu-id="db301-115">Snapshot options.</span></span>

## <a name="see-also"></a><span data-ttu-id="db301-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="db301-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db301-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="db301-117">Reference</span></span>

[<span data-ttu-id="db301-118">Clase de API</span><span class="sxs-lookup"><span data-stu-id="db301-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="db301-119">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="db301-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="db301-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="db301-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
