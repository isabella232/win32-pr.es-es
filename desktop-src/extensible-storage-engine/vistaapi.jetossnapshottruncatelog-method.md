---
description: 'Más información sobre: VistaApi. JetOSSnapshotTruncateLog (método)'
title: Método VistaApi. JetOSSnapshotTruncateLog (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686474"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a><span data-ttu-id="36c66-103">VistaApi. JetOSSnapshotTruncateLog, método</span><span class="sxs-lookup"><span data-stu-id="36c66-103">VistaApi.JetOSSnapshotTruncateLog method</span></span>

<span data-ttu-id="36c66-104">Habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="36c66-104">Enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="36c66-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36c66-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="36c66-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36c66-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36c66-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36c66-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="36c66-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36c66-108">Parameters</span></span>

  - <span data-ttu-id="36c66-109">instantánea</span><span class="sxs-lookup"><span data-stu-id="36c66-109">snapshot</span></span>  
    <span data-ttu-id="36c66-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36c66-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="36c66-111">Identificador de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="36c66-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="36c66-112">grbit</span><span class="sxs-lookup"><span data-stu-id="36c66-112">grbit</span></span>  
    <span data-ttu-id="36c66-113">Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="36c66-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="36c66-114">Opciones para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="36c66-114">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c66-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36c66-115">Remarks</span></span>

<span data-ttu-id="36c66-116">Solo se debe llamar a esta función si la instantánea se creó con la opción [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) .</span><span class="sxs-lookup"><span data-stu-id="36c66-116">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="36c66-117">De lo contrario, la sesión de instantánea finaliza después de la llamada a [JetOSSnapshotThaw (JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span><span class="sxs-lookup"><span data-stu-id="36c66-117">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="36c66-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="36c66-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36c66-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="36c66-119">Reference</span></span>

[<span data-ttu-id="36c66-120">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="36c66-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="36c66-121">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="36c66-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="36c66-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="36c66-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
