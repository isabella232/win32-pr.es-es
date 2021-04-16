---
description: 'Más información sobre: Windows8Api. JetTryPrereadIndexRanges (método)'
title: Método Windows8Api. JetTryPrereadIndexRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9664e658254de057b0e3aa8ae86813eb996a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696664"
---
# <a name="windows8apijettryprereadindexranges-method"></a><span data-ttu-id="61c1a-103">Windows8Api. JetTryPrereadIndexRanges, método</span><span class="sxs-lookup"><span data-stu-id="61c1a-103">Windows8Api.JetTryPrereadIndexRanges method</span></span>

<span data-ttu-id="61c1a-104">Si los registros con los intervalos de claves especificados no están en la caché del búfer, inicie las lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="61c1a-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="61c1a-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61c1a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="61c1a-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61c1a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61c1a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61c1a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="61c1a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61c1a-108">Parameters</span></span>

  - <span data-ttu-id="61c1a-109">sesid</span><span class="sxs-lookup"><span data-stu-id="61c1a-109">sesid</span></span>  
    <span data-ttu-id="61c1a-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="61c1a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="61c1a-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="61c1a-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="61c1a-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="61c1a-112">tableid</span></span>  
    <span data-ttu-id="61c1a-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="61c1a-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="61c1a-114">Tabla en la que se van a emitir las lecturas preleídas.</span><span class="sxs-lookup"><span data-stu-id="61c1a-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="61c1a-115">indexRanges</span><span class="sxs-lookup"><span data-stu-id="61c1a-115">indexRanges</span></span>  
    <span data-ttu-id="61c1a-116">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="61c1a-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="61c1a-117">Intervalos de clave que se van a leer como preleídos.</span><span class="sxs-lookup"><span data-stu-id="61c1a-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="61c1a-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="61c1a-118">rangeIndex</span></span>  
    <span data-ttu-id="61c1a-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61c1a-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="61c1a-120">Índice del primer intervalo de claves de la matriz que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="61c1a-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="61c1a-121">rangeCount</span><span class="sxs-lookup"><span data-stu-id="61c1a-121">rangeCount</span></span>  
    <span data-ttu-id="61c1a-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61c1a-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="61c1a-123">Número máximo de intervalos de clave que se van a leer.</span><span class="sxs-lookup"><span data-stu-id="61c1a-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="61c1a-124">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="61c1a-124">rangesPreread</span></span>  
    <span data-ttu-id="61c1a-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61c1a-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="61c1a-126">Devuelve el número de claves que se han preleído realmente.</span><span class="sxs-lookup"><span data-stu-id="61c1a-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="61c1a-127">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="61c1a-127">columnsPreread</span></span>  
    <span data-ttu-id="61c1a-128">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="61c1a-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="61c1a-129">Lista de identificadores de columna para las columnas de valor largo que se van a leer como prelectura.</span><span class="sxs-lookup"><span data-stu-id="61c1a-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="61c1a-130">grbit</span><span class="sxs-lookup"><span data-stu-id="61c1a-130">grbit</span></span>  
    <span data-ttu-id="61c1a-131">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="61c1a-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="61c1a-132">Opciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="61c1a-132">Preread options.</span></span> <span data-ttu-id="61c1a-133">Se utiliza para especificar la dirección de la lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="61c1a-133">Used to specify the direction of the preread.</span></span>

#### <a name="return-value"></a><span data-ttu-id="61c1a-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61c1a-134">Return value</span></span>

<span data-ttu-id="61c1a-135">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="61c1a-135">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="61c1a-136">**\[ true \]** si se ha realizado una lectura preleída; de lo contrario, **\[ false \]** .</span><span class="sxs-lookup"><span data-stu-id="61c1a-136">**\[true\]** if some preread done, **\[false\]** otherwise.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61c1a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="61c1a-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61c1a-138">Referencia</span><span class="sxs-lookup"><span data-stu-id="61c1a-138">Reference</span></span>

[<span data-ttu-id="61c1a-139">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="61c1a-139">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="61c1a-140">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="61c1a-140">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="61c1a-141">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="61c1a-141">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
