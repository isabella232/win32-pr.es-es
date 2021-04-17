---
description: 'Más información sobre: enumeración GotoSecondaryIndexBookmarkGrbit'
title: Enumeración GotoSecondaryIndexBookmarkGrbit
TOCTitle: GotoSecondaryIndexBookmarkGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.gotosecondaryindexbookmarkgrbit(v=EXCHG.10)
ms:contentKeyID: 39515224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f38b5f26abc4dfafb95d5560b3ff1def4267527c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666788"
---
# <a name="gotosecondaryindexbookmarkgrbit-enumeration"></a><span data-ttu-id="90c01-103">Enumeración GotoSecondaryIndexBookmarkGrbit</span><span class="sxs-lookup"><span data-stu-id="90c01-103">GotoSecondaryIndexBookmarkGrbit enumeration</span></span>

<span data-ttu-id="90c01-104">Opciones para [JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="90c01-104">Options for [JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span></span>

<span data-ttu-id="90c01-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="90c01-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="90c01-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90c01-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="90c01-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90c01-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90c01-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90c01-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GotoSecondaryIndexBookmarkGrbit
'Usage
Dim instance As GotoSecondaryIndexBookmarkGrbit
```

``` csharp
[FlagsAttribute]
public enum GotoSecondaryIndexBookmarkGrbit
```

## <a name="members"></a><span data-ttu-id="90c01-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="90c01-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="90c01-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="90c01-110">Member name</span></span></th>
<th><span data-ttu-id="90c01-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="90c01-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="90c01-112">None</span><span class="sxs-lookup"><span data-stu-id="90c01-112">None</span></span></td>
<td><span data-ttu-id="90c01-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="90c01-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="90c01-114">BookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="90c01-114">BookmarkPermitVirtualCurrency</span></span></td>
<td><span data-ttu-id="90c01-115">En caso de que ya no se pueda encontrar la entrada de índice, el cursor se dejará situado donde esa entrada de índice se haya encontrado previamente.</span><span class="sxs-lookup"><span data-stu-id="90c01-115">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="90c01-116">La operación todavía producirá un error con JET_errRecordDeleted; sin embargo, será posible moverse a la entrada de índice siguiente o anterior en relación con la entrada de índice que ahora falta.</span><span class="sxs-lookup"><span data-stu-id="90c01-116">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="90c01-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="90c01-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90c01-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="90c01-118">Reference</span></span>

[<span data-ttu-id="90c01-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="90c01-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
