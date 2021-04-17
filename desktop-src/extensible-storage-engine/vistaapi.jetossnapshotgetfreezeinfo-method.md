---
description: 'Más información sobre: VistaApi. JetOSSnapshotGetFreezeInfo (método)'
title: Método VistaApi. JetOSSnapshotGetFreezeInfo (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotGetFreezeInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotgetfreezeinfo(v=EXCHG.10)
ms:contentKeyID: 55104199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84b8f33f1fcac280e8fee65c1092c8fccdec3b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687230"
---
# <a name="vistaapijetossnapshotgetfreezeinfo-method"></a><span data-ttu-id="928d0-103">VistaApi. JetOSSnapshotGetFreezeInfo, método</span><span class="sxs-lookup"><span data-stu-id="928d0-103">VistaApi.JetOSSnapshotGetFreezeInfo method</span></span>

<span data-ttu-id="928d0-104">Recupera la lista de instancias y bases de datos que forman parte de la sesión de instantáneas en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="928d0-104">Retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="928d0-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="928d0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="928d0-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="928d0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="928d0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="928d0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotGetFreezeInfo ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotGetFreezeInfoGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotGetFreezeInfoGrbitVistaApi.JetOSSnapshotGetFreezeInfo(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotGetFreezeInfo(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotGetFreezeInfoGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="928d0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="928d0-108">Parameters</span></span>

  - <span data-ttu-id="928d0-109">instantánea</span><span class="sxs-lookup"><span data-stu-id="928d0-109">snapshot</span></span>  
    <span data-ttu-id="928d0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="928d0-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="928d0-111">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="928d0-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="928d0-112">numInstances</span><span class="sxs-lookup"><span data-stu-id="928d0-112">numInstances</span></span>  
    <span data-ttu-id="928d0-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="928d0-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="928d0-114">Devuelve el número de instancias de.</span><span class="sxs-lookup"><span data-stu-id="928d0-114">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="928d0-115">instances</span><span class="sxs-lookup"><span data-stu-id="928d0-115">instances</span></span>  
    <span data-ttu-id="928d0-116">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="928d0-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="928d0-117">Devuelve información sobre las instancias de.</span><span class="sxs-lookup"><span data-stu-id="928d0-117">Returns information about the instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="928d0-118">grbit</span><span class="sxs-lookup"><span data-stu-id="928d0-118">grbit</span></span>  
    <span data-ttu-id="928d0-119">Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="928d0-119">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="928d0-120">Opciones para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="928d0-120">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="928d0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="928d0-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="928d0-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="928d0-122">Reference</span></span>

[<span data-ttu-id="928d0-123">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="928d0-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="928d0-124">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="928d0-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="928d0-125">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="928d0-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
