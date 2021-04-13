---
description: 'Más información sobre: API. JetGotoBookmark (método)'
title: Método API. JetGotoBookmark
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 362a174e3da4dad864fd504e1678b4a3a1477e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546963"
---
# <a name="apijetgotobookmark-method"></a><span data-ttu-id="330d7-103">Método API. JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="330d7-103">Api.JetGotoBookmark method</span></span>

<span data-ttu-id="330d7-104">Coloca un cursor en una entrada de índice para el registro asociado al marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="330d7-104">Positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="330d7-105">El marcador se puede usar con cualquier índice definido en una tabla.</span><span class="sxs-lookup"><span data-stu-id="330d7-105">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="330d7-106">El marcador de un registro se puede recuperar mediante [JetGetBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetgetbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="330d7-106">The bookmark for a record can be retrieved using [JetGetBookmark(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetgetbookmark-method.md).</span></span>

<span data-ttu-id="330d7-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="330d7-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="330d7-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="330d7-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="330d7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="330d7-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="330d7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="330d7-110">Parameters</span></span>

  - <span data-ttu-id="330d7-111">sesid</span><span class="sxs-lookup"><span data-stu-id="330d7-111">sesid</span></span>  
    <span data-ttu-id="330d7-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="330d7-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="330d7-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="330d7-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="330d7-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="330d7-114">tableid</span></span>  
    <span data-ttu-id="330d7-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="330d7-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="330d7-116">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="330d7-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="330d7-117">marcador</span><span class="sxs-lookup"><span data-stu-id="330d7-117">bookmark</span></span>  
    <span data-ttu-id="330d7-118">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="330d7-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="330d7-119">Marcador utilizado para colocar el cursor.</span><span class="sxs-lookup"><span data-stu-id="330d7-119">The bookmark used to position the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="330d7-120">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="330d7-120">bookmarkSize</span></span>  
    <span data-ttu-id="330d7-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="330d7-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="330d7-122">Tamaño del marcador.</span><span class="sxs-lookup"><span data-stu-id="330d7-122">The size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="330d7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="330d7-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="330d7-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="330d7-124">Reference</span></span>

[<span data-ttu-id="330d7-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="330d7-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="330d7-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="330d7-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="330d7-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="330d7-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
