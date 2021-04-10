---
description: 'Más información sobre: API. JetRenameTable (método)'
title: Método API. JetRenameTable
TOCTitle: 'JetRenameTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenametable(v=EXCHG.10)
ms:contentKeyID: 55100788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bb108498501df50a43964f5b069860d10c39258
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082044"
---
# <a name="apijetrenametable-method"></a><span data-ttu-id="d940e-103">Método API. JetRenameTable</span><span class="sxs-lookup"><span data-stu-id="d940e-103">Api.JetRenameTable method</span></span>

<span data-ttu-id="d940e-104">Cambia el nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="d940e-104">Changes the name of an existing table.</span></span>

<span data-ttu-id="d940e-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d940e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d940e-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d940e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d940e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d940e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    newTableName As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim newTableName As StringApi.JetRenameTable(sesid, dbid, _
    tableName, newTableName)
```

``` csharp
public static void JetRenameTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string newTableName
)
```

#### <a name="parameters"></a><span data-ttu-id="d940e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d940e-108">Parameters</span></span>

  - <span data-ttu-id="d940e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d940e-109">sesid</span></span>  
    <span data-ttu-id="d940e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d940e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d940e-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d940e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d940e-112">dbid</span><span class="sxs-lookup"><span data-stu-id="d940e-112">dbid</span></span>  
    <span data-ttu-id="d940e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d940e-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d940e-114">Base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="d940e-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="d940e-115">tableName</span><span class="sxs-lookup"><span data-stu-id="d940e-115">tableName</span></span>  
    <span data-ttu-id="d940e-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d940e-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d940e-117">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d940e-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="d940e-118">newTableName</span><span class="sxs-lookup"><span data-stu-id="d940e-118">newTableName</span></span>  
    <span data-ttu-id="d940e-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d940e-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d940e-120">El nuevo nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d940e-120">The new name of the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="d940e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d940e-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d940e-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="d940e-122">Reference</span></span>

[<span data-ttu-id="d940e-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d940e-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d940e-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d940e-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d940e-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d940e-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
