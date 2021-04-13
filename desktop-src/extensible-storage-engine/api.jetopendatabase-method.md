---
description: 'Más información sobre: API. JetOpenDatabase (método)'
title: Método API. JetOpenDatabase
TOCTitle: 'JetOpenDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopendatabase(v=EXCHG.10)
ms:contentKeyID: 55100768
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faaff0eec2b5bc8a2c2f2a72a61f9f6a23f7d972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279091"
---
# <a name="apijetopendatabase-method"></a><span data-ttu-id="2f739-103">Método API. JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="2f739-103">Api.JetOpenDatabase method</span></span>

<span data-ttu-id="2f739-104">Abre una base de datos adjuntada previamente con [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md)para su uso con una sesión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2f739-104">Opens a database previously attached with [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), for use with a database session.</span></span> <span data-ttu-id="2f739-105">Se puede llamar a esta función varias veces para la misma base de datos.</span><span class="sxs-lookup"><span data-stu-id="2f739-105">This function can be called multiple times for the same database.</span></span>

<span data-ttu-id="2f739-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2f739-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2f739-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2f739-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2f739-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f739-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As OpenDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As OpenDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetOpenDatabase(sesid, _
    database, connect, dbid, grbit)
```

``` csharp
public static JET_wrn JetOpenDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    OpenDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2f739-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f739-109">Parameters</span></span>

  - <span data-ttu-id="2f739-110">sesid</span><span class="sxs-lookup"><span data-stu-id="2f739-110">sesid</span></span>  
    <span data-ttu-id="2f739-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2f739-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2f739-112">La sesión que abre la base de datos.</span><span class="sxs-lookup"><span data-stu-id="2f739-112">The session that is opening the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="2f739-113">database</span><span class="sxs-lookup"><span data-stu-id="2f739-113">database</span></span>  
    <span data-ttu-id="2f739-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2f739-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2f739-115">Base de datos que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="2f739-115">The database to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="2f739-116">conectar</span><span class="sxs-lookup"><span data-stu-id="2f739-116">connect</span></span>  
    <span data-ttu-id="2f739-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2f739-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2f739-118">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2f739-118">Reserved for future use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2f739-119">dbid</span><span class="sxs-lookup"><span data-stu-id="2f739-119">dbid</span></span>  
    <span data-ttu-id="2f739-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2f739-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="2f739-121">Devuelve el DBID de la base de datos adjunta.</span><span class="sxs-lookup"><span data-stu-id="2f739-121">Returns the dbid of the attached database.</span></span>

<!-- end list -->

  - <span data-ttu-id="2f739-122">grbit</span><span class="sxs-lookup"><span data-stu-id="2f739-122">grbit</span></span>  
    <span data-ttu-id="2f739-123">Tipo: [Microsoft. ISAM. esent. Interop. OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2f739-123">Type: [Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2f739-124">Abra opciones de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2f739-124">Open database options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2f739-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f739-125">Return value</span></span>

<span data-ttu-id="2f739-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2f739-126">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="2f739-127">Código de advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="2f739-127">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2f739-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f739-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2f739-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="2f739-129">Reference</span></span>

[<span data-ttu-id="2f739-130">Clase de API</span><span class="sxs-lookup"><span data-stu-id="2f739-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2f739-131">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="2f739-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2f739-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2f739-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
