---
description: 'Más información sobre: API. MoveBeforeFirst (método)'
title: Método API. MoveBeforeFirst
TOCTitle: 'MoveBeforeFirst method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.movebeforefirst(v=EXCHG.10)
ms:contentKeyID: 55100849
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c3e49762c0d2be1f416181f5c07fb06b088d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714945"
---
# <a name="apimovebeforefirst-method"></a><span data-ttu-id="14826-103">Método API. MoveBeforeFirst</span><span class="sxs-lookup"><span data-stu-id="14826-103">Api.MoveBeforeFirst method</span></span>

<span data-ttu-id="14826-104">Coloca el cursor delante del primer registro de la tabla.</span><span class="sxs-lookup"><span data-stu-id="14826-104">Position the cursor before the first record in the table.</span></span> <span data-ttu-id="14826-105">El siguiente movimiento posterior colocará el cursor en el primer registro.</span><span class="sxs-lookup"><span data-stu-id="14826-105">A subsequent move next will position the cursor on the first record.</span></span>

<span data-ttu-id="14826-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14826-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14826-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14826-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14826-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14826-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MoveBeforeFirst ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.MoveBeforeFirst(sesid, tableid)
```

``` csharp
public static void MoveBeforeFirst(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="14826-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14826-109">Parameters</span></span>

  - <span data-ttu-id="14826-110">sesid</span><span class="sxs-lookup"><span data-stu-id="14826-110">sesid</span></span>  
    <span data-ttu-id="14826-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="14826-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="14826-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="14826-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="14826-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="14826-113">tableid</span></span>  
    <span data-ttu-id="14826-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="14826-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="14826-115">Tabla que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="14826-115">The table to position.</span></span>

## <a name="see-also"></a><span data-ttu-id="14826-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="14826-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14826-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="14826-117">Reference</span></span>

[<span data-ttu-id="14826-118">Clase de API</span><span class="sxs-lookup"><span data-stu-id="14826-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="14826-119">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="14826-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="14826-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="14826-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
