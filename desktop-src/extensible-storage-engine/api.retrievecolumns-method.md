---
description: 'Más información sobre: API. RetrieveColumns (método)'
title: Método API. RetrieveColumns
TOCTitle: 'RetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100867
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c981ad8b8e90db10bb8735aa349315b769e6641f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539688"
---
# <a name="apiretrievecolumns-method"></a><span data-ttu-id="3c5b8-103">Método API. RetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="3c5b8-103">Api.RetrieveColumns method</span></span>

<span data-ttu-id="3c5b8-104">Recupera columnas en objetos ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="3c5b8-104">Retrieves columns into ColumnValue objects.</span></span>

<span data-ttu-id="3c5b8-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3c5b8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3c5b8-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3c5b8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3c5b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c5b8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub RetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.RetrieveColumns(sesid, tableid, _
    values)
```

``` csharp
public static void RetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="3c5b8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c5b8-108">Parameters</span></span>

  - <span data-ttu-id="3c5b8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="3c5b8-109">sesid</span></span>  
    <span data-ttu-id="3c5b8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3c5b8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3c5b8-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="3c5b8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3c5b8-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="3c5b8-112">tableid</span></span>  
    <span data-ttu-id="3c5b8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3c5b8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3c5b8-114">El cursor recupera los datos de.</span><span class="sxs-lookup"><span data-stu-id="3c5b8-114">The cursor retrieve the data from.</span></span> <span data-ttu-id="3c5b8-115">El cursor debe colocarse en un registro.</span><span class="sxs-lookup"><span data-stu-id="3c5b8-115">The cursor should be positioned on a record.</span></span>

<!-- end list -->

  - <span data-ttu-id="3c5b8-116">valores</span><span class="sxs-lookup"><span data-stu-id="3c5b8-116">values</span></span>  
    <span data-ttu-id="3c5b8-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="3c5b8-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="3c5b8-118">Valores que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3c5b8-118">The values to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c5b8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c5b8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3c5b8-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="3c5b8-120">Reference</span></span>

[<span data-ttu-id="3c5b8-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="3c5b8-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3c5b8-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="3c5b8-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3c5b8-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3c5b8-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
