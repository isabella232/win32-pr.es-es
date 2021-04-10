---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, single)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, single)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Single)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100877
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e57a42a46b9247133c1427f3ae270645f6133523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153707"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-single"></a><span data-ttu-id="4d503-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, single)</span><span class="sxs-lookup"><span data-stu-id="4d503-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</span></span>

<span data-ttu-id="4d503-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="4d503-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="4d503-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d503-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d503-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d503-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d503-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d503-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Single _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As SingleApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    float data
)
```

#### <a name="parameters"></a><span data-ttu-id="4d503-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d503-108">Parameters</span></span>

  - <span data-ttu-id="4d503-109">sesid</span><span class="sxs-lookup"><span data-stu-id="4d503-109">sesid</span></span>  
    <span data-ttu-id="4d503-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d503-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4d503-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="4d503-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d503-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="4d503-112">tableid</span></span>  
    <span data-ttu-id="4d503-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d503-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4d503-114">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="4d503-114">The cursor to update.</span></span> <span data-ttu-id="4d503-115">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="4d503-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d503-116">columnid</span><span class="sxs-lookup"><span data-stu-id="4d503-116">columnid</span></span>  
    <span data-ttu-id="4d503-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d503-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4d503-118">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="4d503-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d503-119">datos</span><span class="sxs-lookup"><span data-stu-id="4d503-119">data</span></span>  
    <span data-ttu-id="4d503-120">Tipo: [System. Single](/dotnet/api/system.single)</span><span class="sxs-lookup"><span data-stu-id="4d503-120">Type: [System.Single](/dotnet/api/system.single)</span></span>  
    
    <span data-ttu-id="4d503-121">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="4d503-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d503-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d503-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d503-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="4d503-123">Reference</span></span>

[<span data-ttu-id="4d503-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="4d503-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4d503-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="4d503-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4d503-126">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="4d503-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="4d503-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4d503-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
