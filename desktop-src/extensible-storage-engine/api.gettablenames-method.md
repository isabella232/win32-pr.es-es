---
description: 'Más información sobre: API. GetTableNames (método)'
title: Método API. GetTableNames
TOCTitle: 'GetTableNames method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableNames(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablenames(v=EXCHG.10)
ms:contentKeyID: 55100650
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39a52d62ae5271353350df15c4c00833266094cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154050"
---
# <a name="apigettablenames-method"></a><span data-ttu-id="25acb-103">Método API. GetTableNames</span><span class="sxs-lookup"><span data-stu-id="25acb-103">Api.GetTableNames method</span></span>

<span data-ttu-id="25acb-104">Devuelve los nombres de las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="25acb-104">Returns the names of the tables in the database.</span></span>

<span data-ttu-id="25acb-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25acb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25acb-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25acb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25acb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25acb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableNames ( _
    sesid As JET_SESID, _
    dbid As JET_DBID _
) As IEnumerable(Of String)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim returnValue As IEnumerable(Of String)

returnValue = Api.GetTableNames(sesid, _
    dbid)
```

``` csharp
public static IEnumerable<string> GetTableNames(
    JET_SESID sesid,
    JET_DBID dbid
)
```

#### <a name="parameters"></a><span data-ttu-id="25acb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25acb-108">Parameters</span></span>

  - <span data-ttu-id="25acb-109">sesid</span><span class="sxs-lookup"><span data-stu-id="25acb-109">sesid</span></span>  
    <span data-ttu-id="25acb-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25acb-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="25acb-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="25acb-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="25acb-112">dbid</span><span class="sxs-lookup"><span data-stu-id="25acb-112">dbid</span></span>  
    <span data-ttu-id="25acb-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25acb-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="25acb-114">Base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="25acb-114">The database containing the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="25acb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25acb-115">Return value</span></span>

<span data-ttu-id="25acb-116">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="25acb-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\></span></span>  
<span data-ttu-id="25acb-117">Un iterador sobre los nombres de las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="25acb-117">An iterator over the names of the tables in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="25acb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="25acb-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25acb-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="25acb-119">Reference</span></span>

[<span data-ttu-id="25acb-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="25acb-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="25acb-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="25acb-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="25acb-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="25acb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
