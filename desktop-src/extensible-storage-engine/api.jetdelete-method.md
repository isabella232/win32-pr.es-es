---
description: 'Más información sobre: API. JetDelete (método)'
title: Método API. JetDelete
TOCTitle: 'JetDelete method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDelete(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdelete(v=EXCHG.10)
ms:contentKeyID: 55100681
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc3decf125b8d3f3f1df7228852901cca90aae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907787"
---
# <a name="apijetdelete-method"></a><span data-ttu-id="e1f79-103">Método API. JetDelete</span><span class="sxs-lookup"><span data-stu-id="e1f79-103">Api.JetDelete method</span></span>

<span data-ttu-id="e1f79-104">Elimina el registro actual de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e1f79-104">Deletes the current record in a database table.</span></span>

<span data-ttu-id="e1f79-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e1f79-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e1f79-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e1f79-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f79-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1f79-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDelete ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetDelete(sesid, tableid)
```

``` csharp
public static void JetDelete(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="e1f79-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1f79-108">Parameters</span></span>

  - <span data-ttu-id="e1f79-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e1f79-109">sesid</span></span>  
    <span data-ttu-id="e1f79-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e1f79-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e1f79-111">La sesión que abrió el cursor.</span><span class="sxs-lookup"><span data-stu-id="e1f79-111">The session that opened the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="e1f79-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="e1f79-112">tableid</span></span>  
    <span data-ttu-id="e1f79-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e1f79-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e1f79-114">Cursor en una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e1f79-114">The cursor on a database table.</span></span> <span data-ttu-id="e1f79-115">Se eliminará la fila actual.</span><span class="sxs-lookup"><span data-stu-id="e1f79-115">The current row will be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1f79-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1f79-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e1f79-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="e1f79-117">Reference</span></span>

[<span data-ttu-id="e1f79-118">Clase de API</span><span class="sxs-lookup"><span data-stu-id="e1f79-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e1f79-119">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="e1f79-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e1f79-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e1f79-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
