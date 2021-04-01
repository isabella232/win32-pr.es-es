---
description: 'Más información sobre: API. JetGetSecondaryIndexBookmark (método)'
title: Método API. JetGetSecondaryIndexBookmark
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082046"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a><span data-ttu-id="873cb-103">Método API. JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="873cb-103">Api.JetGetSecondaryIndexBookmark method</span></span>

<span data-ttu-id="873cb-104">Recupera un marcador especial para la entrada de índice secundario en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="873cb-104">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="873cb-105">Este marcador se puede usar para volver a colocar eficazmente ese cursor en la misma entrada de índice mediante JetGotoSecondaryIndexBookmark.</span><span class="sxs-lookup"><span data-stu-id="873cb-105">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="873cb-106">Esto es muy útil cuando se cambia la posición en un índice secundario que contiene claves duplicadas o que contiene varias entradas de índice para el mismo registro.</span><span class="sxs-lookup"><span data-stu-id="873cb-106">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="873cb-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="873cb-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="873cb-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="873cb-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="873cb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="873cb-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="873cb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="873cb-110">Parameters</span></span>

  - <span data-ttu-id="873cb-111">sesid</span><span class="sxs-lookup"><span data-stu-id="873cb-111">sesid</span></span>  
    <span data-ttu-id="873cb-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="873cb-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="873cb-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="873cb-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="873cb-114">tableid</span></span>  
    <span data-ttu-id="873cb-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="873cb-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="873cb-116">Cursor del que se va a recuperar el marcador.</span><span class="sxs-lookup"><span data-stu-id="873cb-116">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="873cb-117">secondaryKey</span></span>  
    <span data-ttu-id="873cb-118">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="873cb-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="873cb-119">Búfer de salida de la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="873cb-119">Output buffer for the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="873cb-120">secondaryKeySize</span></span>  
    <span data-ttu-id="873cb-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="873cb-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="873cb-122">Tamaño del búfer de clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="873cb-122">Size of the secondary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-123">actualSecondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="873cb-123">actualSecondaryKeySize</span></span>  
    <span data-ttu-id="873cb-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="873cb-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="873cb-125">Devuelve el tamaño de la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="873cb-125">Returns the size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-126">primaryKey</span><span class="sxs-lookup"><span data-stu-id="873cb-126">primaryKey</span></span>  
    <span data-ttu-id="873cb-127">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="873cb-127">Type: \[\]</span></span>  
    
    <span data-ttu-id="873cb-128">Búfer de salida de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="873cb-128">Output buffer for the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-129">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="873cb-129">primaryKeySize</span></span>  
    <span data-ttu-id="873cb-130">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="873cb-130">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="873cb-131">Tamaño del búfer de clave principal.</span><span class="sxs-lookup"><span data-stu-id="873cb-131">Size of the primary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-132">actualPrimaryKeySize</span><span class="sxs-lookup"><span data-stu-id="873cb-132">actualPrimaryKeySize</span></span>  
    <span data-ttu-id="873cb-133">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="873cb-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="873cb-134">Devuelve el tamaño de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="873cb-134">Returns the size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="873cb-135">grbit</span><span class="sxs-lookup"><span data-stu-id="873cb-135">grbit</span></span>  
    <span data-ttu-id="873cb-136">Tipo: [Microsoft. ISAM. esent. Interop. GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="873cb-136">Type: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="873cb-137">Opciones de la llamada.</span><span class="sxs-lookup"><span data-stu-id="873cb-137">Options for the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="873cb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="873cb-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="873cb-139">Referencia</span><span class="sxs-lookup"><span data-stu-id="873cb-139">Reference</span></span>

[<span data-ttu-id="873cb-140">Clase de API</span><span class="sxs-lookup"><span data-stu-id="873cb-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="873cb-141">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="873cb-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="873cb-142">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="873cb-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
