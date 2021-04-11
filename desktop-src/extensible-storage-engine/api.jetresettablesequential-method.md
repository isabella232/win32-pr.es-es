---
description: 'Más información sobre: API. JetResetTableSequential (método)'
title: Método API. JetResetTableSequential
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279080"
---
# <a name="apijetresettablesequential-method"></a><span data-ttu-id="d033d-103">Método API. JetResetTableSequential</span><span class="sxs-lookup"><span data-stu-id="d033d-103">Api.JetResetTableSequential method</span></span>

<span data-ttu-id="d033d-104">Notifica al motor de base de datos que la aplicación ya no está examinando el índice completo en el que está situado el cursor.</span><span class="sxs-lookup"><span data-stu-id="d033d-104">Notifies the database engine that the application is no longer scanning the entire index the cursor is positioned on.</span></span> <span data-ttu-id="d033d-105">Esta llamada invierte una notificación enviada por [JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="d033d-105">This call reverses a notification sent by [JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span></span>

<span data-ttu-id="d033d-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d033d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d033d-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d033d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d033d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d033d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d033d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d033d-109">Parameters</span></span>

  - <span data-ttu-id="d033d-110">sesid</span><span class="sxs-lookup"><span data-stu-id="d033d-110">sesid</span></span>  
    <span data-ttu-id="d033d-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d033d-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d033d-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d033d-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d033d-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="d033d-113">tableid</span></span>  
    <span data-ttu-id="d033d-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d033d-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d033d-115">Cursor que ha tenido acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="d033d-115">The cursor that was accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="d033d-116">grbit</span><span class="sxs-lookup"><span data-stu-id="d033d-116">grbit</span></span>  
    <span data-ttu-id="d033d-117">Tipo: [Microsoft. ISAM. esent. Interop. ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d033d-117">Type: [Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d033d-118">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d033d-118">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="d033d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d033d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d033d-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d033d-120">Reference</span></span>

[<span data-ttu-id="d033d-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d033d-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d033d-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d033d-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d033d-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d033d-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
