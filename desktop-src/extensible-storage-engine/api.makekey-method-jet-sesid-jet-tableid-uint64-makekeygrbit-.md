---
description: 'Más información sobre: método API. MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)'
title: Método API. MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt64,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100827
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
ms.openlocfilehash: 0cb4b26015e67e6801fe0e19ee0b0ca8d41ac4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716621"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint64-makekeygrbit"></a><span data-ttu-id="6be6e-103">Método API. MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="6be6e-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</span></span>

<span data-ttu-id="6be6e-104">Construye una clave de búsqueda que puede usar [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) y [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="6be6e-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="6be6e-105">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="6be6e-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="6be6e-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6be6e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6be6e-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6be6e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6be6e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6be6e-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As ULong, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As ULong
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ulong data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6be6e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6be6e-109">Parameters</span></span>

  - <span data-ttu-id="6be6e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6be6e-110">sesid</span></span>  
    <span data-ttu-id="6be6e-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6be6e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6be6e-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6be6e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be6e-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="6be6e-113">tableid</span></span>  
    <span data-ttu-id="6be6e-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6be6e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6be6e-115">Cursor en el que se va a crear la clave.</span><span class="sxs-lookup"><span data-stu-id="6be6e-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be6e-116">datos</span><span class="sxs-lookup"><span data-stu-id="6be6e-116">data</span></span>  
    <span data-ttu-id="6be6e-117">Tipo: [System. UInt64](/dotnet/api/system.uint64)</span><span class="sxs-lookup"><span data-stu-id="6be6e-117">Type: [System.UInt64](/dotnet/api/system.uint64)</span></span>  
    
    <span data-ttu-id="6be6e-118">Datos de columna para la columna de clave actual del índice actual.</span><span class="sxs-lookup"><span data-stu-id="6be6e-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be6e-119">grbit</span><span class="sxs-lookup"><span data-stu-id="6be6e-119">grbit</span></span>  
    <span data-ttu-id="6be6e-120">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6be6e-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6be6e-121">Opciones de clave.</span><span class="sxs-lookup"><span data-stu-id="6be6e-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="6be6e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6be6e-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6be6e-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="6be6e-123">Reference</span></span>

[<span data-ttu-id="6be6e-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="6be6e-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6be6e-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="6be6e-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6be6e-126">Sobrecarga MakeKey</span><span class="sxs-lookup"><span data-stu-id="6be6e-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="6be6e-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6be6e-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
