---
description: 'Más información sobre: API. JetMakeKey (método)'
title: Método API. JetMakeKey
TOCTitle: 'JetMakeKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmakekey(v=EXCHG.10)
ms:contentKeyID: 55100764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13db6e7106f5312e03ffa5acfbd86c72d38c6edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002823"
---
# <a name="apijetmakekey-method"></a><span data-ttu-id="90c44-103">Método API. JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="90c44-103">Api.JetMakeKey method</span></span>

<span data-ttu-id="90c44-104">Construye claves de búsqueda que puede usar [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) y [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="90c44-104">Constructs search keys that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="90c44-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90c44-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="90c44-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90c44-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90c44-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90c44-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As MakeKeyGrbitApi.JetMakeKey(sesid, tableid, data, _
    dataSize, grbit)
```

``` csharp
public static void JetMakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="90c44-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90c44-108">Parameters</span></span>

  - <span data-ttu-id="90c44-109">sesid</span><span class="sxs-lookup"><span data-stu-id="90c44-109">sesid</span></span>  
    <span data-ttu-id="90c44-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="90c44-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="90c44-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="90c44-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="90c44-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="90c44-112">tableid</span></span>  
    <span data-ttu-id="90c44-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="90c44-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="90c44-114">Cursor en el que se va a crear la clave.</span><span class="sxs-lookup"><span data-stu-id="90c44-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="90c44-115">datos</span><span class="sxs-lookup"><span data-stu-id="90c44-115">data</span></span>  
    <span data-ttu-id="90c44-116">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="90c44-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="90c44-117">Datos de columna para la columna de clave actual del índice actual.</span><span class="sxs-lookup"><span data-stu-id="90c44-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="90c44-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="90c44-118">dataSize</span></span>  
    <span data-ttu-id="90c44-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="90c44-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="90c44-120">Tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="90c44-120">Size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="90c44-121">grbit</span><span class="sxs-lookup"><span data-stu-id="90c44-121">grbit</span></span>  
    <span data-ttu-id="90c44-122">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="90c44-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="90c44-123">Opciones de clave.</span><span class="sxs-lookup"><span data-stu-id="90c44-123">Key options.</span></span>

## <a name="remarks"></a><span data-ttu-id="90c44-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90c44-124">Remarks</span></span>

<span data-ttu-id="90c44-125">Las funciones MakeKey proporcionan funcionalidad de creación de claves específica del tipo de información.</span><span class="sxs-lookup"><span data-stu-id="90c44-125">The MakeKey functions provide datatype-specific make key functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="90c44-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="90c44-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90c44-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="90c44-127">Reference</span></span>

[<span data-ttu-id="90c44-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="90c44-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="90c44-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="90c44-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="90c44-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="90c44-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
