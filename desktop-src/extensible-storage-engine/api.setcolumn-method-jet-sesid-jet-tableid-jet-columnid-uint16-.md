---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.UInt16)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100929
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
ms.openlocfilehash: b1f7b1f385b3629cd08ed043bf3d34366bd2af58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082254"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-uint16"></a><span data-ttu-id="3edc0-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</span><span class="sxs-lookup"><span data-stu-id="3edc0-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</span></span>

<span data-ttu-id="3edc0-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="3edc0-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="3edc0-105">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="3edc0-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="3edc0-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3edc0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3edc0-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3edc0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3edc0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3edc0-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As UShort _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As UShortApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    ushort data
)
```

#### <a name="parameters"></a><span data-ttu-id="3edc0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3edc0-109">Parameters</span></span>

  - <span data-ttu-id="3edc0-110">sesid</span><span class="sxs-lookup"><span data-stu-id="3edc0-110">sesid</span></span>  
    <span data-ttu-id="3edc0-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3edc0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3edc0-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="3edc0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3edc0-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="3edc0-113">tableid</span></span>  
    <span data-ttu-id="3edc0-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3edc0-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3edc0-115">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="3edc0-115">The cursor to update.</span></span> <span data-ttu-id="3edc0-116">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="3edc0-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="3edc0-117">columnid</span><span class="sxs-lookup"><span data-stu-id="3edc0-117">columnid</span></span>  
    <span data-ttu-id="3edc0-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3edc0-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="3edc0-119">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="3edc0-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3edc0-120">datos</span><span class="sxs-lookup"><span data-stu-id="3edc0-120">data</span></span>  
    <span data-ttu-id="3edc0-121">Tipo: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="3edc0-121">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="3edc0-122">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="3edc0-122">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="3edc0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3edc0-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3edc0-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="3edc0-124">Reference</span></span>

[<span data-ttu-id="3edc0-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="3edc0-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3edc0-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="3edc0-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3edc0-127">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="3edc0-127">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="3edc0-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3edc0-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
