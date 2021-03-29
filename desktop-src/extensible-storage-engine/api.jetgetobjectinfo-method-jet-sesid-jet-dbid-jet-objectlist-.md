---
description: 'Más información sobre: método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)'
title: Método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_OBJECTLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_OBJECTLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100728
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9564b0eb2dc8a5bee2e65b729164f39a19d349fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809223"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objectlist"></a><span data-ttu-id="e5f37-103">Método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)</span><span class="sxs-lookup"><span data-stu-id="e5f37-103">Api.JetGetObjectInfo method (JET_SESID, JET_DBID, JET_OBJECTLIST)</span></span>

<span data-ttu-id="e5f37-104">Recupera información acerca de los objetos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e5f37-104">Retrieves information about database objects.</span></span>

<span data-ttu-id="e5f37-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5f37-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5f37-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5f37-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f37-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5f37-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef objectlist As JET_OBJECTLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objectlist As JET_OBJECTLISTApi.JetGetObjectInfo(sesid, dbid, _
    objectlist)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out JET_OBJECTLIST objectlist
)
```

#### <a name="parameters"></a><span data-ttu-id="e5f37-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5f37-108">Parameters</span></span>

  - <span data-ttu-id="e5f37-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e5f37-109">sesid</span></span>  
    <span data-ttu-id="e5f37-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e5f37-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e5f37-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e5f37-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5f37-112">dbid</span><span class="sxs-lookup"><span data-stu-id="e5f37-112">dbid</span></span>  
    <span data-ttu-id="e5f37-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e5f37-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="e5f37-114">Base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e5f37-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5f37-115">objectlist</span><span class="sxs-lookup"><span data-stu-id="e5f37-115">objectlist</span></span>  
    <span data-ttu-id="e5f37-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_OBJECTLIST](./jet-objectlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="e5f37-116">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTLIST](./jet-objectlist-class.md)</span></span>  
    
    <span data-ttu-id="e5f37-117">Se rellena con información acerca de los objetos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e5f37-117">Filled in with information about the objects in the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5f37-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5f37-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5f37-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="e5f37-119">Reference</span></span>

[<span data-ttu-id="e5f37-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="e5f37-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e5f37-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="e5f37-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e5f37-122">Sobrecarga JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="e5f37-122">JetGetObjectInfo overload</span></span>](./api.jetgetobjectinfo-method.md)

[<span data-ttu-id="e5f37-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e5f37-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
