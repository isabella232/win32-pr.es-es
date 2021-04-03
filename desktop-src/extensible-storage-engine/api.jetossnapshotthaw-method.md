---
description: 'Más información sobre: API. JetOSSnapshotThaw (método)'
title: Método API. JetOSSnapshotThaw
TOCTitle: 'JetOSSnapshotThaw method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.SnapshotThawGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotthaw(v=EXCHG.10)
ms:contentKeyID: 55100780
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f3fe0bc04586dddade7a9723720bbd3c994c516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913185"
---
# <a name="apijetossnapshotthaw-method"></a><span data-ttu-id="b104b-103">Método API. JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="b104b-103">Api.JetOSSnapshotThaw method</span></span>

<span data-ttu-id="b104b-104">Notifica al motor de que puede reanudar las operaciones de e/s normales después de un período de inmovilización y una instantánea correcta.</span><span class="sxs-lookup"><span data-stu-id="b104b-104">Notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="b104b-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b104b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b104b-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b104b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b104b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b104b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotThaw ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotThawGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotThawGrbitApi.JetOSSnapshotThaw(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotThaw(
    JET_OSSNAPID snapshot,
    SnapshotThawGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b104b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b104b-108">Parameters</span></span>

  - <span data-ttu-id="b104b-109">instantánea</span><span class="sxs-lookup"><span data-stu-id="b104b-109">snapshot</span></span>  
    <span data-ttu-id="b104b-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b104b-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="b104b-111">IDENTIFICADOR de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="b104b-111">The ID of the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="b104b-112">grbit</span><span class="sxs-lookup"><span data-stu-id="b104b-112">grbit</span></span>  
    <span data-ttu-id="b104b-113">Tipo: [Microsoft. ISAM. esent. Interop. SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b104b-113">Type: [Microsoft.Isam.Esent.Interop.SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b104b-114">Opciones de reanudación.</span><span class="sxs-lookup"><span data-stu-id="b104b-114">Thaw options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b104b-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b104b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b104b-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="b104b-116">Reference</span></span>

[<span data-ttu-id="b104b-117">Clase de API</span><span class="sxs-lookup"><span data-stu-id="b104b-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b104b-118">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="b104b-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b104b-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b104b-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
