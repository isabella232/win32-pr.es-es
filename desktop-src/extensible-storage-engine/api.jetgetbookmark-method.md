---
description: 'Más información sobre: API. JetGetBookmark (método)'
title: Método API. JetGetBookmark
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eaac3c0c92fa9d6cfa1a5bca660791b81efe5ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720344"
---
# <a name="apijetgetbookmark-method"></a><span data-ttu-id="c4cf1-103">Método API. JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="c4cf1-103">Api.JetGetBookmark method</span></span>

<span data-ttu-id="c4cf1-104">Recupera el marcador del registro asociado a la entrada de índice en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="c4cf1-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="c4cf1-105">Este marcador se puede usar para volver a colocar el cursor en el mismo registro mediante [JetGotoBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetgotobookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="c4cf1-105">This bookmark can then be used to reposition that cursor back to the same record using [JetGotoBookmark(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetgotobookmark-method.md).</span></span> <span data-ttu-id="c4cf1-106">El marcador no tendrá más de [BookmarkMost](./systemparameters.bookmarkmost-property.md) bytes.</span><span class="sxs-lookup"><span data-stu-id="c4cf1-106">The bookmark will be no longer than [BookmarkMost](./systemparameters.bookmarkmost-property.md) bytes.</span></span> <span data-ttu-id="c4cf1-107">Vea también [GetBookmark (JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="c4cf1-107">Also see [GetBookmark(JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span></span>

<span data-ttu-id="c4cf1-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c4cf1-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c4cf1-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c4cf1-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cf1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4cf1-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="c4cf1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4cf1-111">Parameters</span></span>

  - <span data-ttu-id="c4cf1-112">sesid</span><span class="sxs-lookup"><span data-stu-id="c4cf1-112">sesid</span></span>  
    <span data-ttu-id="c4cf1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4cf1-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c4cf1-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c4cf1-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4cf1-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="c4cf1-115">tableid</span></span>  
    <span data-ttu-id="c4cf1-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4cf1-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c4cf1-117">Cursor del que se va a recuperar el marcador.</span><span class="sxs-lookup"><span data-stu-id="c4cf1-117">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4cf1-118">marcador</span><span class="sxs-lookup"><span data-stu-id="c4cf1-118">bookmark</span></span>  
    <span data-ttu-id="c4cf1-119">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="c4cf1-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="c4cf1-120">Búfer que va a contener el marcador.</span><span class="sxs-lookup"><span data-stu-id="c4cf1-120">Buffer to contain the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4cf1-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="c4cf1-121">bookmarkSize</span></span>  
    <span data-ttu-id="c4cf1-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c4cf1-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c4cf1-123">Tamaño del búfer del marcador.</span><span class="sxs-lookup"><span data-stu-id="c4cf1-123">Size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4cf1-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="c4cf1-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="c4cf1-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c4cf1-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c4cf1-126">Devuelve el tamaño real del marcador.</span><span class="sxs-lookup"><span data-stu-id="c4cf1-126">Returns the actual size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4cf1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4cf1-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4cf1-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="c4cf1-128">Reference</span></span>

[<span data-ttu-id="c4cf1-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="c4cf1-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c4cf1-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="c4cf1-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c4cf1-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c4cf1-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
