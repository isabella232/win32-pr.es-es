---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100879
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
ms.openlocfilehash: bc3950db60b4d7fb52309e246555802f1624d6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697586"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-uint32"></a><span data-ttu-id="6ece9-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</span><span class="sxs-lookup"><span data-stu-id="6ece9-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</span></span>

<span data-ttu-id="6ece9-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="6ece9-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="6ece9-105">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="6ece9-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="6ece9-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6ece9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6ece9-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6ece9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6ece9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ece9-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As UIntegerApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    uint data
)
```

#### <a name="parameters"></a><span data-ttu-id="6ece9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ece9-109">Parameters</span></span>

  - <span data-ttu-id="6ece9-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6ece9-110">sesid</span></span>  
    <span data-ttu-id="6ece9-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6ece9-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6ece9-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6ece9-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6ece9-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="6ece9-113">tableid</span></span>  
    <span data-ttu-id="6ece9-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6ece9-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6ece9-115">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="6ece9-115">The cursor to update.</span></span> <span data-ttu-id="6ece9-116">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="6ece9-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="6ece9-117">columnid</span><span class="sxs-lookup"><span data-stu-id="6ece9-117">columnid</span></span>  
    <span data-ttu-id="6ece9-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6ece9-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6ece9-119">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="6ece9-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="6ece9-120">datos</span><span class="sxs-lookup"><span data-stu-id="6ece9-120">data</span></span>  
    <span data-ttu-id="6ece9-121">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="6ece9-121">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="6ece9-122">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="6ece9-122">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ece9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ece9-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6ece9-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="6ece9-124">Reference</span></span>

[<span data-ttu-id="6ece9-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="6ece9-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6ece9-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="6ece9-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6ece9-127">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="6ece9-127">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="6ece9-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6ece9-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
