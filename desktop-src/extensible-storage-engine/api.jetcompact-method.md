---
description: 'Más información sobre: API. JetCompact (método)'
title: Método API. JetCompact
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001024"
---
# <a name="apijetcompact-method"></a><span data-ttu-id="82e3a-103">Método API. JetCompact</span><span class="sxs-lookup"><span data-stu-id="82e3a-103">Api.JetCompact method</span></span>

<span data-ttu-id="82e3a-104">Realiza una copia de una base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="82e3a-104">Makes a copy of an existing database.</span></span> <span data-ttu-id="82e3a-105">La copia se compacta con un estado óptimo para su uso.</span><span class="sxs-lookup"><span data-stu-id="82e3a-105">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="82e3a-106">Los datos de los datos copiados se empaquetarán de acuerdo con las medidas elegidas para los índices en la creación de índices.</span><span class="sxs-lookup"><span data-stu-id="82e3a-106">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="82e3a-107">De esta manera, los datos comprimidos se pueden almacenar de la forma más densa posible.</span><span class="sxs-lookup"><span data-stu-id="82e3a-107">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="82e3a-108">Como alternativa, los datos compactos pueden reservar espacio para las inserciones de índice o el crecimiento de registros posteriores.</span><span class="sxs-lookup"><span data-stu-id="82e3a-108">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

<span data-ttu-id="82e3a-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82e3a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82e3a-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82e3a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82e3a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82e3a-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="82e3a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82e3a-112">Parameters</span></span>

  - <span data-ttu-id="82e3a-113">sesid</span><span class="sxs-lookup"><span data-stu-id="82e3a-113">sesid</span></span>  
    <span data-ttu-id="82e3a-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82e3a-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="82e3a-115">La sesión que se va a usar para la llamada.</span><span class="sxs-lookup"><span data-stu-id="82e3a-115">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="82e3a-116">sourceDatabase</span><span class="sxs-lookup"><span data-stu-id="82e3a-116">sourceDatabase</span></span>  
    <span data-ttu-id="82e3a-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="82e3a-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="82e3a-118">La base de datos de origen que se compactará.</span><span class="sxs-lookup"><span data-stu-id="82e3a-118">The source database that will be compacted.</span></span>

<!-- end list -->

  - <span data-ttu-id="82e3a-119">destinationDatabase</span><span class="sxs-lookup"><span data-stu-id="82e3a-119">destinationDatabase</span></span>  
    <span data-ttu-id="82e3a-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="82e3a-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="82e3a-121">Nombre que se va a utilizar para la base de datos compactada.</span><span class="sxs-lookup"><span data-stu-id="82e3a-121">The name to use for the compacted database.</span></span>

<!-- end list -->

  - <span data-ttu-id="82e3a-122">statusCallback</span><span class="sxs-lookup"><span data-stu-id="82e3a-122">statusCallback</span></span>  
    <span data-ttu-id="82e3a-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="82e3a-123">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="82e3a-124">Función de devolución de llamada a la que se puede llamar periódicamente a través de la operación de compactación de base de datos para informar del progreso.</span><span class="sxs-lookup"><span data-stu-id="82e3a-124">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="82e3a-125">no se tiene en cuenta</span><span class="sxs-lookup"><span data-stu-id="82e3a-125">ignored</span></span>  
    <span data-ttu-id="82e3a-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_CONVERT](./jet-convert-class.md)</span><span class="sxs-lookup"><span data-stu-id="82e3a-126">Type: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span></span>  
    
    <span data-ttu-id="82e3a-127">Este parámetro se omite y debe ser null.</span><span class="sxs-lookup"><span data-stu-id="82e3a-127">This parameter is ignored and should be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="82e3a-128">grbit</span><span class="sxs-lookup"><span data-stu-id="82e3a-128">grbit</span></span>  
    <span data-ttu-id="82e3a-129">Tipo: [Microsoft. ISAM. esent. Interop. CompactGrbit](./compactgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="82e3a-129">Type: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="82e3a-130">Opciones de Compact.</span><span class="sxs-lookup"><span data-stu-id="82e3a-130">Compact options.</span></span>

## <a name="see-also"></a><span data-ttu-id="82e3a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="82e3a-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82e3a-132">Referencia</span><span class="sxs-lookup"><span data-stu-id="82e3a-132">Reference</span></span>

[<span data-ttu-id="82e3a-133">Clase de API</span><span class="sxs-lookup"><span data-stu-id="82e3a-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="82e3a-134">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="82e3a-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="82e3a-135">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="82e3a-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
