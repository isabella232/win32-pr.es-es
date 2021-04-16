---
description: 'Más información sobre: API. TryMove (método)'
title: Método API. TryMove
TOCTitle: 'TryMove method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymove(v=EXCHG.10)
ms:contentKeyID: 55100883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMove
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d4b3aa596bb5e813d87dcc6f278112fe1e4cbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696201"
---
# <a name="apitrymove-method"></a><span data-ttu-id="619aa-103">Método API. TryMove</span><span class="sxs-lookup"><span data-stu-id="619aa-103">Api.TryMove method</span></span>

<span data-ttu-id="619aa-104">Intente desplazarse por un índice.</span><span class="sxs-lookup"><span data-stu-id="619aa-104">Try to navigate through an index.</span></span> <span data-ttu-id="619aa-105">Si la navegación se realiza correctamente, este método devuelve true.</span><span class="sxs-lookup"><span data-stu-id="619aa-105">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="619aa-106">Si no hay ningún registro para navegar a este método, devuelve false; se producirá una excepción para otros errores.</span><span class="sxs-lookup"><span data-stu-id="619aa-106">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span>

<span data-ttu-id="619aa-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="619aa-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="619aa-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="619aa-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="619aa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="619aa-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    move As JET_Move, _
    grbit As MoveGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim move As JET_Move
Dim grbit As MoveGrbit
Dim returnValue As Boolean

returnValue = Api.TryMove(sesid, _
    tableid, move, grbit)
```

``` csharp
public static bool TryMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move move,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="619aa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="619aa-110">Parameters</span></span>

  - <span data-ttu-id="619aa-111">sesid</span><span class="sxs-lookup"><span data-stu-id="619aa-111">sesid</span></span>  
    <span data-ttu-id="619aa-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="619aa-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="619aa-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="619aa-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="619aa-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="619aa-114">tableid</span></span>  
    <span data-ttu-id="619aa-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="619aa-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="619aa-116">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="619aa-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="619aa-117">mover</span><span class="sxs-lookup"><span data-stu-id="619aa-117">move</span></span>  
    <span data-ttu-id="619aa-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="619aa-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="619aa-119">Dirección en la que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="619aa-119">The direction to move in.</span></span>

<!-- end list -->

  - <span data-ttu-id="619aa-120">grbit</span><span class="sxs-lookup"><span data-stu-id="619aa-120">grbit</span></span>  
    <span data-ttu-id="619aa-121">Tipo: [Microsoft. ISAM. esent. Interop. MoveGrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="619aa-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="619aa-122">Opciones de movimiento.</span><span class="sxs-lookup"><span data-stu-id="619aa-122">Move options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="619aa-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="619aa-123">Return value</span></span>

<span data-ttu-id="619aa-124">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="619aa-124">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="619aa-125">True si el movimiento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="619aa-125">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="619aa-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="619aa-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="619aa-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="619aa-127">Reference</span></span>

[<span data-ttu-id="619aa-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="619aa-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="619aa-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="619aa-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="619aa-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="619aa-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
