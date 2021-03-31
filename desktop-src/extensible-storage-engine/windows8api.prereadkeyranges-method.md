---
description: 'Más información sobre: Windows8Api. PrereadKeyRanges (método)'
title: Método Windows8Api. PrereadKeyRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001411"
---
# <a name="windows8apiprereadkeyranges-method"></a><span data-ttu-id="6e9a9-103">Windows8Api. PrereadKeyRanges, método</span><span class="sxs-lookup"><span data-stu-id="6e9a9-103">Windows8Api.PrereadKeyRanges method</span></span>

<span data-ttu-id="6e9a9-104">Si los registros con los intervalos de claves especificados no están en la caché del búfer, inicie las lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-104">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="6e9a9-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="6e9a9-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9a9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e9a9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6e9a9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e9a9-108">Parameters</span></span>

  - <span data-ttu-id="6e9a9-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6e9a9-109">sesid</span></span>  
    <span data-ttu-id="6e9a9-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6e9a9-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="6e9a9-112">tableid</span></span>  
    <span data-ttu-id="6e9a9-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6e9a9-114">Tabla en la que se van a emitir las lecturas preleídas.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-115">keysStart</span><span class="sxs-lookup"><span data-stu-id="6e9a9-115">keysStart</span></span>  
    <span data-ttu-id="6e9a9-116">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="6e9a9-117">Inicio de los intervalos de clave que se van a leer.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-117">The start of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-118">keyStartLengths</span><span class="sxs-lookup"><span data-stu-id="6e9a9-118">keyStartLengths</span></span>  
    <span data-ttu-id="6e9a9-119">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="6e9a9-120">Longitud de las claves de inicio que se van a leer como prelectura.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-120">The lengths of the start keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-121">keysEnd</span><span class="sxs-lookup"><span data-stu-id="6e9a9-121">keysEnd</span></span>  
    <span data-ttu-id="6e9a9-122">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="6e9a9-123">Final del intervalo de claves que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-123">The end of key rangess to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-124">keyEndLengths</span><span class="sxs-lookup"><span data-stu-id="6e9a9-124">keyEndLengths</span></span>  
    <span data-ttu-id="6e9a9-125">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-125">Type: \[\]</span></span>  
    
    <span data-ttu-id="6e9a9-126">Longitud de las teclas finales que se van a leer.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-126">The lengths of the end keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-127">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="6e9a9-127">rangeIndex</span></span>  
    <span data-ttu-id="6e9a9-128">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6e9a9-129">Índice del primer intervalo de claves de la matriz que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-129">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-130">rangeCount</span><span class="sxs-lookup"><span data-stu-id="6e9a9-130">rangeCount</span></span>  
    <span data-ttu-id="6e9a9-131">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-131">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6e9a9-132">Número máximo de intervalos de clave que se van a leer.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-132">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-133">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="6e9a9-133">rangesPreread</span></span>  
    <span data-ttu-id="6e9a9-134">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-134">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6e9a9-135">Devuelve el número de claves que se han preleído realmente.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-135">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-136">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="6e9a9-136">columnsPreread</span></span>  
    <span data-ttu-id="6e9a9-137">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-137">Type: \[\]</span></span>  
    
    <span data-ttu-id="6e9a9-138">Lista de identificadores de columna para las columnas de valor largo que se van a leer como prelectura.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-138">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e9a9-139">grbit</span><span class="sxs-lookup"><span data-stu-id="6e9a9-139">grbit</span></span>  
    <span data-ttu-id="6e9a9-140">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6e9a9-140">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6e9a9-141">Opciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-141">Preread options.</span></span> <span data-ttu-id="6e9a9-142">Se utiliza para especificar la dirección de la lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6e9a9-142">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e9a9-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e9a9-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e9a9-144">Referencia</span><span class="sxs-lookup"><span data-stu-id="6e9a9-144">Reference</span></span>

[<span data-ttu-id="6e9a9-145">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="6e9a9-145">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="6e9a9-146">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="6e9a9-146">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="6e9a9-147">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="6e9a9-147">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
