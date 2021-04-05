---
description: 'Más información sobre: API. JetGetCursorInfo (método)'
title: Método API. JetGetCursorInfo
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7144283a062b0097d6866e74d1c263bb130c5e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082050"
---
# <a name="apijetgetcursorinfo-method"></a><span data-ttu-id="a6df1-103">Método API. JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="a6df1-103">Api.JetGetCursorInfo method</span></span>

<span data-ttu-id="a6df1-104">Determinar si una actualización del registro actual de un cursor producirá un conflicto de escritura, según el estado actual de actualización del registro.</span><span class="sxs-lookup"><span data-stu-id="a6df1-104">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="a6df1-105">Es posible que se devuelva un conflicto de escritura en última instancia, incluso si JetGetCursorInfo devuelve un valor correcto.</span><span class="sxs-lookup"><span data-stu-id="a6df1-105">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="a6df1-106">debido a que otra sesión puede actualizar el registro antes de que la sesión actual pueda actualizar el mismo registro.</span><span class="sxs-lookup"><span data-stu-id="a6df1-106">because another session may update the record before the current session is able to update the same record.</span></span>

<span data-ttu-id="a6df1-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6df1-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a6df1-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a6df1-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6df1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6df1-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="a6df1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6df1-110">Parameters</span></span>

  - <span data-ttu-id="a6df1-111">sesid</span><span class="sxs-lookup"><span data-stu-id="a6df1-111">sesid</span></span>  
    <span data-ttu-id="a6df1-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a6df1-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a6df1-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a6df1-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6df1-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="a6df1-114">tableid</span></span>  
    <span data-ttu-id="a6df1-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a6df1-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a6df1-116">Cursor que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="a6df1-116">The cursor to check.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6df1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6df1-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6df1-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="a6df1-118">Reference</span></span>

[<span data-ttu-id="a6df1-119">Clase de API</span><span class="sxs-lookup"><span data-stu-id="a6df1-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a6df1-120">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="a6df1-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a6df1-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a6df1-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
