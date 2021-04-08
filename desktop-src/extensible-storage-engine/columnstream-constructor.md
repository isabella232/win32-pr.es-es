---
description: 'Más información acerca de: constructor ColumnStream'
title: Constructor de ColumnStream
TOCTitle: 'ColumnStream constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 498fed2daf2cad5903d9597689a80eadca7bd569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001370"
---
# <a name="columnstream-constructor"></a><span data-ttu-id="18c86-103">Constructor de ColumnStream</span><span class="sxs-lookup"><span data-stu-id="18c86-103">ColumnStream constructor</span></span>

<span data-ttu-id="18c86-104">Inicializa una nueva instancia de la clase ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="18c86-104">Initializes a new instance of the ColumnStream class.</span></span>

<span data-ttu-id="18c86-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="18c86-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="18c86-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="18c86-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="18c86-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18c86-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID

Dim instance As New ColumnStream(sesid, tableid, _
    columnid)
```

``` csharp
public ColumnStream(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="18c86-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18c86-108">Parameters</span></span>

  - <span data-ttu-id="18c86-109">sesid</span><span class="sxs-lookup"><span data-stu-id="18c86-109">sesid</span></span>  
    <span data-ttu-id="18c86-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="18c86-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="18c86-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="18c86-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="18c86-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="18c86-112">tableid</span></span>  
    <span data-ttu-id="18c86-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="18c86-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="18c86-114">Cursor que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="18c86-114">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="18c86-115">columnid</span><span class="sxs-lookup"><span data-stu-id="18c86-115">columnid</span></span>  
    <span data-ttu-id="18c86-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="18c86-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="18c86-117">Columnid de la columna de la que se van a establecer o recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="18c86-117">The columnid of the column to set/retrieve data from.</span></span>

## <a name="see-also"></a><span data-ttu-id="18c86-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="18c86-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="18c86-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="18c86-119">Reference</span></span>

[<span data-ttu-id="18c86-120">Clase ColumnStream</span><span class="sxs-lookup"><span data-stu-id="18c86-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="18c86-121">Miembros de ColumnStream</span><span class="sxs-lookup"><span data-stu-id="18c86-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="18c86-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="18c86-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
