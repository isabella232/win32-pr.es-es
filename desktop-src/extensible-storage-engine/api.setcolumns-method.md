---
description: 'Más información acerca de: API. SetColumns (método)'
title: API. SetColumns (método)
TOCTitle: 'SetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumns(v=EXCHG.10)
ms:contentKeyID: 55100936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4ed75c668c0000c1d01d521a57ead46055bc8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808257"
---
# <a name="apisetcolumns-method"></a><span data-ttu-id="ef51e-103">API. SetColumns (método)</span><span class="sxs-lookup"><span data-stu-id="ef51e-103">Api.SetColumns method</span></span>

<span data-ttu-id="ef51e-104">Establece las columnas de los objetos ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="ef51e-104">Sets columns from ColumnValue objects.</span></span>

<span data-ttu-id="ef51e-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef51e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ef51e-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ef51e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ef51e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef51e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.SetColumns(sesid, tableid, values)
```

``` csharp
public static void SetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="ef51e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef51e-108">Parameters</span></span>

  - <span data-ttu-id="ef51e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ef51e-109">sesid</span></span>  
    <span data-ttu-id="ef51e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ef51e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ef51e-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ef51e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ef51e-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="ef51e-112">tableid</span></span>  
    <span data-ttu-id="ef51e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ef51e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ef51e-114">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="ef51e-114">The cursor to update.</span></span> <span data-ttu-id="ef51e-115">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="ef51e-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="ef51e-116">valores</span><span class="sxs-lookup"><span data-stu-id="ef51e-116">values</span></span>  
    <span data-ttu-id="ef51e-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="ef51e-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="ef51e-118">Valores que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="ef51e-118">The values to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef51e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef51e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef51e-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="ef51e-120">Reference</span></span>

[<span data-ttu-id="ef51e-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="ef51e-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ef51e-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="ef51e-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ef51e-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ef51e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
