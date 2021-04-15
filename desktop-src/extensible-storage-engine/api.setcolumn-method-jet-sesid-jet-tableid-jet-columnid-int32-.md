---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100878
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf838a080ed1663264fb023c556eb5bc473b6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539682"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-int32"></a><span data-ttu-id="24c76-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</span><span class="sxs-lookup"><span data-stu-id="24c76-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</span></span>

<span data-ttu-id="24c76-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="24c76-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="24c76-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="24c76-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="24c76-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="24c76-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="24c76-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24c76-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As IntegerApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int data
)
```

#### <a name="parameters"></a><span data-ttu-id="24c76-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24c76-108">Parameters</span></span>

  - <span data-ttu-id="24c76-109">sesid</span><span class="sxs-lookup"><span data-stu-id="24c76-109">sesid</span></span>  
    <span data-ttu-id="24c76-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24c76-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="24c76-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="24c76-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="24c76-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="24c76-112">tableid</span></span>  
    <span data-ttu-id="24c76-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24c76-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="24c76-114">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="24c76-114">The cursor to update.</span></span> <span data-ttu-id="24c76-115">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="24c76-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="24c76-116">columnid</span><span class="sxs-lookup"><span data-stu-id="24c76-116">columnid</span></span>  
    <span data-ttu-id="24c76-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24c76-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="24c76-118">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="24c76-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="24c76-119">datos</span><span class="sxs-lookup"><span data-stu-id="24c76-119">data</span></span>  
    <span data-ttu-id="24c76-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="24c76-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="24c76-121">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="24c76-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="24c76-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="24c76-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="24c76-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="24c76-123">Reference</span></span>

[<span data-ttu-id="24c76-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="24c76-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="24c76-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="24c76-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="24c76-126">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="24c76-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="24c76-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="24c76-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
