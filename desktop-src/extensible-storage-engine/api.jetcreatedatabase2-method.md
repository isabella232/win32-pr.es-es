---
description: 'Más información sobre: API. JetCreateDatabase2 (método)'
title: Método API. JetCreateDatabase2
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808275"
---
# <a name="apijetcreatedatabase2-method"></a><span data-ttu-id="ee829-103">Método API. JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="ee829-103">Api.JetCreateDatabase2 method</span></span>

<span data-ttu-id="ee829-104">Crea y adjunta un archivo de base de datos con un tamaño máximo de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="ee829-104">Creates and attaches a database file with a maximum database size specified.</span></span>

<span data-ttu-id="ee829-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee829-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ee829-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ee829-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee829-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee829-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ee829-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee829-108">Parameters</span></span>

  - <span data-ttu-id="ee829-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ee829-109">sesid</span></span>  
    <span data-ttu-id="ee829-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee829-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ee829-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ee829-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee829-112">database</span><span class="sxs-lookup"><span data-stu-id="ee829-112">database</span></span>  
    <span data-ttu-id="ee829-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ee829-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ee829-114">Ruta de acceso al archivo de base de datos que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="ee829-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee829-115">maxPages</span><span class="sxs-lookup"><span data-stu-id="ee829-115">maxPages</span></span>  
    <span data-ttu-id="ee829-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ee829-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ee829-117">Tamaño máximo, en páginas de base de datos, de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ee829-117">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="ee829-118">Pasar 0 significa que no hay ningún máximo aplicado.</span><span class="sxs-lookup"><span data-stu-id="ee829-118">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee829-119">dbid</span><span class="sxs-lookup"><span data-stu-id="ee829-119">dbid</span></span>  
    <span data-ttu-id="ee829-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee829-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="ee829-121">Devuelve el DBID de la nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="ee829-121">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee829-122">grbit</span><span class="sxs-lookup"><span data-stu-id="ee829-122">grbit</span></span>  
    <span data-ttu-id="ee829-123">Tipo: [Microsoft. ISAM. esent. Interop. CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ee829-123">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ee829-124">Opciones de creación de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="ee829-124">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee829-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee829-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee829-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="ee829-126">Reference</span></span>

[<span data-ttu-id="ee829-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="ee829-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ee829-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="ee829-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ee829-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ee829-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
