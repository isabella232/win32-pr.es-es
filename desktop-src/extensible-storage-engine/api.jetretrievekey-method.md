---
description: 'Más información sobre: API. JetRetrieveKey (método)'
title: Método API. JetRetrieveKey
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebf130b4542992e18de49d58801f789d40106fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707340"
---
# <a name="apijetretrievekey-method"></a><span data-ttu-id="29c69-103">Método API. JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="29c69-103">Api.JetRetrieveKey method</span></span>

<span data-ttu-id="29c69-104">Recupera la clave de la entrada de índice en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="29c69-104">Retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="29c69-105">Vea también [RetrieveKey (JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="29c69-105">Also see [RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span></span>

<span data-ttu-id="29c69-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="29c69-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="29c69-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="29c69-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="29c69-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29c69-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="29c69-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29c69-109">Parameters</span></span>

  - <span data-ttu-id="29c69-110">sesid</span><span class="sxs-lookup"><span data-stu-id="29c69-110">sesid</span></span>  
    <span data-ttu-id="29c69-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="29c69-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="29c69-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="29c69-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c69-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="29c69-113">tableid</span></span>  
    <span data-ttu-id="29c69-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="29c69-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="29c69-115">Cursor del que se va a recuperar la clave.</span><span class="sxs-lookup"><span data-stu-id="29c69-115">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c69-116">datos</span><span class="sxs-lookup"><span data-stu-id="29c69-116">data</span></span>  
    <span data-ttu-id="29c69-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="29c69-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="29c69-118">Búfer en el que se va a recuperar la clave.</span><span class="sxs-lookup"><span data-stu-id="29c69-118">The buffer to retrieve the key into.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c69-119">dataSize</span><span class="sxs-lookup"><span data-stu-id="29c69-119">dataSize</span></span>  
    <span data-ttu-id="29c69-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="29c69-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="29c69-121">Tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="29c69-121">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c69-122">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="29c69-122">actualDataSize</span></span>  
    <span data-ttu-id="29c69-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="29c69-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="29c69-124">Devuelve el tamaño real de los datos.</span><span class="sxs-lookup"><span data-stu-id="29c69-124">Returns the actual size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="29c69-125">grbit</span><span class="sxs-lookup"><span data-stu-id="29c69-125">grbit</span></span>  
    <span data-ttu-id="29c69-126">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="29c69-126">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="29c69-127">Recupera las opciones de clave.</span><span class="sxs-lookup"><span data-stu-id="29c69-127">Retrieve key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="29c69-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="29c69-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="29c69-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="29c69-129">Reference</span></span>

[<span data-ttu-id="29c69-130">Clase de API</span><span class="sxs-lookup"><span data-stu-id="29c69-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="29c69-131">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="29c69-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="29c69-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="29c69-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
