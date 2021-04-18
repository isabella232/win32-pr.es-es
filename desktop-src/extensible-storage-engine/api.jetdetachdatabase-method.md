---
description: 'Más información sobre: API. JetDetachDatabase (método)'
title: Método API. JetDetachDatabase
TOCTitle: 'JetDetachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100687
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8881021d619bac1dae83a4a001e6b88e94e57256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666345"
---
# <a name="apijetdetachdatabase-method"></a><span data-ttu-id="1a004-103">Método API. JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="1a004-103">Api.JetDetachDatabase method</span></span>

<span data-ttu-id="1a004-104">Libera un archivo de base de datos que se adjuntó previamente a una sesión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1a004-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="1a004-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a004-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a004-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a004-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a004-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a004-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase ( _
    sesid As JET_SESID, _
    database As String _
)
'Usage
Dim sesid As JET_SESID
Dim database As StringApi.JetDetachDatabase(sesid, database)
```

``` csharp
public static void JetDetachDatabase(
    JET_SESID sesid,
    string database
)
```

#### <a name="parameters"></a><span data-ttu-id="1a004-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a004-108">Parameters</span></span>

  - <span data-ttu-id="1a004-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1a004-109">sesid</span></span>  
    <span data-ttu-id="1a004-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a004-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1a004-111">La sesión de base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="1a004-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a004-112">database</span><span class="sxs-lookup"><span data-stu-id="1a004-112">database</span></span>  
    <span data-ttu-id="1a004-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1a004-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1a004-114">Base de datos que se va a desasociar.</span><span class="sxs-lookup"><span data-stu-id="1a004-114">The database to detach.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a004-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a004-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a004-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="1a004-116">Reference</span></span>

[<span data-ttu-id="1a004-117">Clase de API</span><span class="sxs-lookup"><span data-stu-id="1a004-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1a004-118">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="1a004-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1a004-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1a004-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
