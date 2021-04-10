---
description: 'Más información sobre: VistaApi. JetOSSnapshotPrepareInstance (método)'
title: Método VistaApi. JetOSSnapshotPrepareInstance (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotPrepareInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotprepareinstance(v=EXCHG.10)
ms:contentKeyID: 55104304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46151e2b11c669ac9635ce5974757999a8636b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156601"
---
# <a name="vistaapijetossnapshotprepareinstance-method"></a><span data-ttu-id="18ff0-103">VistaApi. JetOSSnapshotPrepareInstance, método</span><span class="sxs-lookup"><span data-stu-id="18ff0-103">VistaApi.JetOSSnapshotPrepareInstance method</span></span>

<span data-ttu-id="18ff0-104">Selecciona una instancia específica para que forme parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="18ff0-104">Selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="18ff0-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="18ff0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="18ff0-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="18ff0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="18ff0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18ff0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepareInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotPrepareInstanceGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotPrepareInstanceGrbitVistaApi.JetOSSnapshotPrepareInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotPrepareInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotPrepareInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="18ff0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18ff0-108">Parameters</span></span>

  - <span data-ttu-id="18ff0-109">instantánea</span><span class="sxs-lookup"><span data-stu-id="18ff0-109">snapshot</span></span>  
    <span data-ttu-id="18ff0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="18ff0-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="18ff0-111">Identificador de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="18ff0-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="18ff0-112">instance</span><span class="sxs-lookup"><span data-stu-id="18ff0-112">instance</span></span>  
    <span data-ttu-id="18ff0-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="18ff0-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="18ff0-114">Instancia de que se va a agregar a la instantánea.</span><span class="sxs-lookup"><span data-stu-id="18ff0-114">The instance to add to the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="18ff0-115">grbit</span><span class="sxs-lookup"><span data-stu-id="18ff0-115">grbit</span></span>  
    <span data-ttu-id="18ff0-116">Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="18ff0-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="18ff0-117">Opciones para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="18ff0-117">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="18ff0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="18ff0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="18ff0-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="18ff0-119">Reference</span></span>

[<span data-ttu-id="18ff0-120">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="18ff0-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="18ff0-121">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="18ff0-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="18ff0-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="18ff0-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
