---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.DateTime)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100875
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
ms.openlocfilehash: e43864a1b632adbc4ecf84d4963e7f87ea799283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686476"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-datetime"></a><span data-ttu-id="d6447-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</span><span class="sxs-lookup"><span data-stu-id="d6447-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</span></span>

<span data-ttu-id="d6447-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="d6447-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="d6447-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6447-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6447-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6447-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6447-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6447-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As DateTime _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As DateTimeApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    DateTime data
)
```

#### <a name="parameters"></a><span data-ttu-id="d6447-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6447-108">Parameters</span></span>

  - <span data-ttu-id="d6447-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d6447-109">sesid</span></span>  
    <span data-ttu-id="d6447-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6447-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d6447-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d6447-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6447-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="d6447-112">tableid</span></span>  
    <span data-ttu-id="d6447-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6447-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d6447-114">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="d6447-114">The cursor to update.</span></span> <span data-ttu-id="d6447-115">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="d6447-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6447-116">columnid</span><span class="sxs-lookup"><span data-stu-id="d6447-116">columnid</span></span>  
    <span data-ttu-id="d6447-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6447-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d6447-118">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="d6447-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6447-119">datos</span><span class="sxs-lookup"><span data-stu-id="d6447-119">data</span></span>  
    <span data-ttu-id="d6447-120">Tipo: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="d6447-120">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
    
    <span data-ttu-id="d6447-121">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="d6447-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6447-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6447-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6447-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="d6447-123">Reference</span></span>

[<span data-ttu-id="d6447-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d6447-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d6447-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d6447-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d6447-126">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="d6447-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="d6447-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d6447-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
