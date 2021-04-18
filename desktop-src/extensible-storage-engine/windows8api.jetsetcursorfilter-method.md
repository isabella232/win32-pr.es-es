---
description: 'Más información sobre: Windows8Api. JetSetCursorFilter (método)'
title: Método Windows8Api. JetSetCursorFilter (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetSetCursorFilter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN[],Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetcursorfilter(v=EXCHG.10)
ms:contentKeyID: 55104447
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0137c25ee6ab548537d797af0a00a7ffcd1f6d5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705858"
---
# <a name="windows8apijetsetcursorfilter-method"></a><span data-ttu-id="f2b08-103">Windows8Api. JetSetCursorFilter, método</span><span class="sxs-lookup"><span data-stu-id="f2b08-103">Windows8Api.JetSetCursorFilter method</span></span>

<span data-ttu-id="f2b08-104">Establezca una matriz de filtros simples para [JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span><span class="sxs-lookup"><span data-stu-id="f2b08-104">Set an array of simple filters for [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span></span>

<span data-ttu-id="f2b08-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2b08-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="f2b08-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f2b08-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b08-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2b08-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCursorFilter ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    filters As JET_INDEX_COLUMN(), _
    grbit As CursorFilterGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim filters As JET_INDEX_COLUMN()
Dim grbit As CursorFilterGrbitWindows8Api.JetSetCursorFilter(sesid, tableid, _
    filters, grbit)
```

``` csharp
public static void JetSetCursorFilter(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_COLUMN[] filters,
    CursorFilterGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f2b08-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2b08-108">Parameters</span></span>

  - <span data-ttu-id="f2b08-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f2b08-109">sesid</span></span>  
    <span data-ttu-id="f2b08-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2b08-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f2b08-111">La sesión que se va a usar para la llamada.</span><span class="sxs-lookup"><span data-stu-id="f2b08-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2b08-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2b08-112">tableid</span></span>  
    <span data-ttu-id="f2b08-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2b08-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f2b08-114">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="f2b08-114">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2b08-115">filters</span><span class="sxs-lookup"><span data-stu-id="f2b08-115">filters</span></span>  
    <span data-ttu-id="f2b08-116">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="f2b08-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2b08-117">Filtros de registro simples.</span><span class="sxs-lookup"><span data-stu-id="f2b08-117">Simple record filters.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2b08-118">grbit</span><span class="sxs-lookup"><span data-stu-id="f2b08-118">grbit</span></span>  
    <span data-ttu-id="f2b08-119">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f2b08-119">Type: [Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f2b08-120">Opciones de movimiento.</span><span class="sxs-lookup"><span data-stu-id="f2b08-120">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2b08-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2b08-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2b08-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="f2b08-122">Reference</span></span>

[<span data-ttu-id="f2b08-123">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="f2b08-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="f2b08-124">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="f2b08-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="f2b08-125">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="f2b08-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
