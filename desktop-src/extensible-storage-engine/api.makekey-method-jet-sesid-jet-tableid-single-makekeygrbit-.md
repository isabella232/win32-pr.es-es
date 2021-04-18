---
description: 'Más información sobre: método API. MakeKey (JET_SESID, JET_TABLEID, single, MakeKeyGrbit)'
title: Método API. MakeKey (JET_SESID, JET_TABLEID, single, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Single,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100826
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17ba9b655c805142f31b0b603bf8a0cfdf81a217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707337"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-single-makekeygrbit"></a><span data-ttu-id="926b7-103">Método API. MakeKey (JET_SESID, JET_TABLEID, single, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="926b7-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)</span></span>

<span data-ttu-id="926b7-104">Construye una clave de búsqueda que puede usar [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) y [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="926b7-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="926b7-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="926b7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="926b7-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="926b7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="926b7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="926b7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Single, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Single
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    float data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="926b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="926b7-108">Parameters</span></span>

  - <span data-ttu-id="926b7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="926b7-109">sesid</span></span>  
    <span data-ttu-id="926b7-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="926b7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="926b7-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="926b7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="926b7-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="926b7-112">tableid</span></span>  
    <span data-ttu-id="926b7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="926b7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="926b7-114">Cursor en el que se va a crear la clave.</span><span class="sxs-lookup"><span data-stu-id="926b7-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="926b7-115">datos</span><span class="sxs-lookup"><span data-stu-id="926b7-115">data</span></span>  
    <span data-ttu-id="926b7-116">Tipo: [System. Single](/dotnet/api/system.single)</span><span class="sxs-lookup"><span data-stu-id="926b7-116">Type: [System.Single](/dotnet/api/system.single)</span></span>  
    
    <span data-ttu-id="926b7-117">Datos de columna para la columna de clave actual del índice actual.</span><span class="sxs-lookup"><span data-stu-id="926b7-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="926b7-118">grbit</span><span class="sxs-lookup"><span data-stu-id="926b7-118">grbit</span></span>  
    <span data-ttu-id="926b7-119">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="926b7-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="926b7-120">Opciones de clave.</span><span class="sxs-lookup"><span data-stu-id="926b7-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="926b7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="926b7-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="926b7-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="926b7-122">Reference</span></span>

[<span data-ttu-id="926b7-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="926b7-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="926b7-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="926b7-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="926b7-125">Sobrecarga MakeKey</span><span class="sxs-lookup"><span data-stu-id="926b7-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="926b7-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="926b7-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
