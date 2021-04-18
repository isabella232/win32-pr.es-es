---
description: 'Más información sobre: VistaApi. JetGetRecordSize (método)'
title: Método VistaApi. JetGetRecordSize (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetRecordSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE@,Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetrecordsize(v=EXCHG.10)
ms:contentKeyID: 55104285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37576e39d83270dcac3333e4d1f78fce32bb2669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696584"
---
# <a name="vistaapijetgetrecordsize-method"></a><span data-ttu-id="9cdf0-103">VistaApi. JetGetRecordSize, método</span><span class="sxs-lookup"><span data-stu-id="9cdf0-103">VistaApi.JetGetRecordSize method</span></span>

<span data-ttu-id="9cdf0-104">Recupera información de tamaño del registro de la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="9cdf0-104">Retrieves record size information from the desired location.</span></span>

<span data-ttu-id="9cdf0-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9cdf0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9cdf0-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9cdf0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9cdf0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cdf0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ByRef recsize As JET_RECSIZE, _
    grbit As GetRecordSizeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recsize As JET_RECSIZE
Dim grbit As GetRecordSizeGrbitVistaApi.JetGetRecordSize(sesid, tableid, _
    recsize, grbit)
```

``` csharp
public static void JetGetRecordSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ref JET_RECSIZE recsize,
    GetRecordSizeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9cdf0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cdf0-108">Parameters</span></span>

  - <span data-ttu-id="9cdf0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9cdf0-109">sesid</span></span>  
    <span data-ttu-id="9cdf0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9cdf0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9cdf0-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9cdf0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9cdf0-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="9cdf0-112">tableid</span></span>  
    <span data-ttu-id="9cdf0-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9cdf0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9cdf0-114">Cursor que se usará para la llamada de API.</span><span class="sxs-lookup"><span data-stu-id="9cdf0-114">The cursor that will be used for the API call.</span></span> <span data-ttu-id="9cdf0-115">El cursor debe estar colocado en un registro o tener una actualización preparada.</span><span class="sxs-lookup"><span data-stu-id="9cdf0-115">The cursor must be positioned on a record, or have an update prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="9cdf0-116">recsize</span><span class="sxs-lookup"><span data-stu-id="9cdf0-116">recsize</span></span>  
    <span data-ttu-id="9cdf0-117">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9cdf0-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="9cdf0-118">Devuelve el tamaño del registro.</span><span class="sxs-lookup"><span data-stu-id="9cdf0-118">Returns the size of the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="9cdf0-119">grbit</span><span class="sxs-lookup"><span data-stu-id="9cdf0-119">grbit</span></span>  
    <span data-ttu-id="9cdf0-120">Tipo: [Microsoft. ISAM. esent. Interop. GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9cdf0-120">Type: [Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9cdf0-121">Opciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="9cdf0-121">Call options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9cdf0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cdf0-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9cdf0-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="9cdf0-123">Reference</span></span>

[<span data-ttu-id="9cdf0-124">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="9cdf0-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="9cdf0-125">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="9cdf0-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="9cdf0-126">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="9cdf0-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
