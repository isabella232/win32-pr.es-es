---
description: 'Más información sobre: API. JetGrowDatabase (método)'
title: Método API. JetGrowDatabase
TOCTitle: 'JetGrowDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgrowdatabase(v=EXCHG.10)
ms:contentKeyID: 55100754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a51f0d55187b6f6eac66c0cba2ec7b9daa7d1dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908278"
---
# <a name="apijetgrowdatabase-method"></a><span data-ttu-id="6acf7-103">Método API. JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="6acf7-103">Api.JetGrowDatabase method</span></span>

<span data-ttu-id="6acf7-104">Extiende el tamaño de una base de datos que está abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="6acf7-104">Extends the size of a database that is currently open.</span></span>

<span data-ttu-id="6acf7-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6acf7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6acf7-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6acf7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6acf7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6acf7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGrowDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetGrowDatabase(sesid, dbid, _
    desiredPages, actualPages)
```

``` csharp
public static void JetGrowDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="6acf7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6acf7-108">Parameters</span></span>

  - <span data-ttu-id="6acf7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6acf7-109">sesid</span></span>  
    <span data-ttu-id="6acf7-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6acf7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6acf7-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6acf7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6acf7-112">dbid</span><span class="sxs-lookup"><span data-stu-id="6acf7-112">dbid</span></span>  
    <span data-ttu-id="6acf7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6acf7-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="6acf7-114">Base de datos que se va a aumentar.</span><span class="sxs-lookup"><span data-stu-id="6acf7-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="6acf7-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="6acf7-115">desiredPages</span></span>  
    <span data-ttu-id="6acf7-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6acf7-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6acf7-117">Tamaño deseado de la base de datos, en páginas.</span><span class="sxs-lookup"><span data-stu-id="6acf7-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="6acf7-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="6acf7-118">actualPages</span></span>  
    <span data-ttu-id="6acf7-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6acf7-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6acf7-120">Tamaño de la base de datos, en páginas, después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6acf7-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="6acf7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="6acf7-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6acf7-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="6acf7-122">Reference</span></span>

[<span data-ttu-id="6acf7-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="6acf7-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6acf7-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="6acf7-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6acf7-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6acf7-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
