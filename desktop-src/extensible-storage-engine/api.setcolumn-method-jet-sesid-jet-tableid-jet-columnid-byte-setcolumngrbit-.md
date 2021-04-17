---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, SetColumnGrbit)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, SetColumnGrbit)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100881
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
ms.openlocfilehash: e345db028422733d37d50f51cfd0c940823f9f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697634"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--setcolumngrbit"></a><span data-ttu-id="f4fb7-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, SetColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="f4fb7-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)</span></span>

<span data-ttu-id="f4fb7-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="f4fb7-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="f4fb7-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f4fb7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f4fb7-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f4fb7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fb7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4fb7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    SetColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f4fb7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4fb7-108">Parameters</span></span>

  - <span data-ttu-id="f4fb7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f4fb7-109">sesid</span></span>  
    <span data-ttu-id="f4fb7-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f4fb7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f4fb7-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f4fb7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4fb7-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="f4fb7-112">tableid</span></span>  
    <span data-ttu-id="f4fb7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f4fb7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f4fb7-114">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="f4fb7-114">The cursor to update.</span></span> <span data-ttu-id="f4fb7-115">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="f4fb7-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4fb7-116">columnid</span><span class="sxs-lookup"><span data-stu-id="f4fb7-116">columnid</span></span>  
    <span data-ttu-id="f4fb7-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f4fb7-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f4fb7-118">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f4fb7-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4fb7-119">datos</span><span class="sxs-lookup"><span data-stu-id="f4fb7-119">data</span></span>  
    <span data-ttu-id="f4fb7-120">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="f4fb7-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="f4fb7-121">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="f4fb7-121">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4fb7-122">grbit</span><span class="sxs-lookup"><span data-stu-id="f4fb7-122">grbit</span></span>  
    <span data-ttu-id="f4fb7-123">Tipo: [Microsoft. ISAM. esent. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f4fb7-123">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f4fb7-124">Opciones de SetColumn.</span><span class="sxs-lookup"><span data-stu-id="f4fb7-124">SetColumn options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4fb7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4fb7-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4fb7-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="f4fb7-126">Reference</span></span>

[<span data-ttu-id="f4fb7-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f4fb7-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f4fb7-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f4fb7-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f4fb7-129">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="f4fb7-129">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="f4fb7-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f4fb7-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
