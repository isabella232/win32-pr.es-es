---
description: 'Más información sobre: API. MoveAfterLast (método)'
title: Método API. MoveAfterLast
TOCTitle: 'MoveAfterLast method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MoveAfterLast(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.moveafterlast(v=EXCHG.10)
ms:contentKeyID: 55100851
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37d3e4eae32c9540f3ee469e4b782c893aa15c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707401"
---
# <a name="apimoveafterlast-method"></a><span data-ttu-id="71397-103">Método API. MoveAfterLast</span><span class="sxs-lookup"><span data-stu-id="71397-103">Api.MoveAfterLast method</span></span>

<span data-ttu-id="71397-104">Coloca el cursor después del último registro de la tabla.</span><span class="sxs-lookup"><span data-stu-id="71397-104">Position the cursor after the last record in the table.</span></span> <span data-ttu-id="71397-105">Un movimiento anterior posterior colocará el cursor en el último registro.</span><span class="sxs-lookup"><span data-stu-id="71397-105">A subsequent move previous will position the cursor on the last record.</span></span>

<span data-ttu-id="71397-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71397-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71397-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71397-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71397-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71397-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MoveAfterLast ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.MoveAfterLast(sesid, tableid)
```

``` csharp
public static void MoveAfterLast(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="71397-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71397-109">Parameters</span></span>

  - <span data-ttu-id="71397-110">sesid</span><span class="sxs-lookup"><span data-stu-id="71397-110">sesid</span></span>  
    <span data-ttu-id="71397-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="71397-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="71397-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="71397-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="71397-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="71397-113">tableid</span></span>  
    <span data-ttu-id="71397-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="71397-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="71397-115">Tabla que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="71397-115">The table to position.</span></span>

## <a name="see-also"></a><span data-ttu-id="71397-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="71397-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71397-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="71397-117">Reference</span></span>

[<span data-ttu-id="71397-118">Clase de API</span><span class="sxs-lookup"><span data-stu-id="71397-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="71397-119">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="71397-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="71397-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="71397-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
