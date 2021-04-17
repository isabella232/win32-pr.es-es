---
description: 'Más información sobre: API. JetGotoSecondaryIndexBookmark (método)'
title: Método API. JetGotoSecondaryIndexBookmark
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697774"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a><span data-ttu-id="edd9f-103">Método API. JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="edd9f-103">Api.JetGotoSecondaryIndexBookmark method</span></span>

<span data-ttu-id="edd9f-104">Coloca un cursor en una entrada de índice que está asociada al marcador de índice secundario especificado.</span><span class="sxs-lookup"><span data-stu-id="edd9f-104">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="edd9f-105">El marcador de índice secundario debe usarse con el mismo índice en la misma tabla desde la que se recuperó originalmente.</span><span class="sxs-lookup"><span data-stu-id="edd9f-105">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="edd9f-106">El marcador de índice secundario de una entrada de índice se puede recuperar mediante JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GotoSecondaryIndexBookmarkGrbit).</span><span class="sxs-lookup"><span data-stu-id="edd9f-106">The secondary index bookmark for an index entry can be retrieved using JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit).</span></span>

<span data-ttu-id="edd9f-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="edd9f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="edd9f-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="edd9f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="edd9f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edd9f-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="edd9f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edd9f-110">Parameters</span></span>

  - <span data-ttu-id="edd9f-111">sesid</span><span class="sxs-lookup"><span data-stu-id="edd9f-111">sesid</span></span>  
    <span data-ttu-id="edd9f-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="edd9f-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="edd9f-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="edd9f-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="edd9f-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="edd9f-114">tableid</span></span>  
    <span data-ttu-id="edd9f-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="edd9f-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="edd9f-116">Cursor de la tabla que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="edd9f-116">The table cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="edd9f-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="edd9f-117">secondaryKey</span></span>  
    <span data-ttu-id="edd9f-118">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="edd9f-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="edd9f-119">Búfer que contiene la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="edd9f-119">The buffer that contains the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="edd9f-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="edd9f-120">secondaryKeySize</span></span>  
    <span data-ttu-id="edd9f-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="edd9f-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="edd9f-122">Tamaño de la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="edd9f-122">The size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="edd9f-123">primaryKey</span><span class="sxs-lookup"><span data-stu-id="edd9f-123">primaryKey</span></span>  
    <span data-ttu-id="edd9f-124">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="edd9f-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="edd9f-125">Búfer que contiene la clave principal.</span><span class="sxs-lookup"><span data-stu-id="edd9f-125">The buffer that contains the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="edd9f-126">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="edd9f-126">primaryKeySize</span></span>  
    <span data-ttu-id="edd9f-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="edd9f-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="edd9f-128">Tamaño de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="edd9f-128">The size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="edd9f-129">grbit</span><span class="sxs-lookup"><span data-stu-id="edd9f-129">grbit</span></span>  
    <span data-ttu-id="edd9f-130">Tipo: [Microsoft. ISAM. esent. Interop. GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="edd9f-130">Type: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="edd9f-131">Opciones para colocar el marcador.</span><span class="sxs-lookup"><span data-stu-id="edd9f-131">Options for positioning the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="edd9f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="edd9f-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="edd9f-133">Referencia</span><span class="sxs-lookup"><span data-stu-id="edd9f-133">Reference</span></span>

[<span data-ttu-id="edd9f-134">Clase de API</span><span class="sxs-lookup"><span data-stu-id="edd9f-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="edd9f-135">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="edd9f-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="edd9f-136">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="edd9f-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
