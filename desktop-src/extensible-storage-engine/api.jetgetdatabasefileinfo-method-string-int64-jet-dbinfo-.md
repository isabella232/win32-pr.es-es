---
description: 'Más información sobre: método API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)'
title: Método API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc036a1c1eceedd39fd265bcf85a2dbaf779a432
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154037"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a><span data-ttu-id="465c2-103">Método API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="465c2-103">Api.JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)</span></span>

<span data-ttu-id="465c2-104">Recupera cierta información sobre la base de datos dada.</span><span class="sxs-lookup"><span data-stu-id="465c2-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="465c2-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="465c2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="465c2-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="465c2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="465c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="465c2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="465c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="465c2-108">Parameters</span></span>

  - <span data-ttu-id="465c2-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="465c2-109">databaseName</span></span>  
    <span data-ttu-id="465c2-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="465c2-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="465c2-111">Nombre de archivo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="465c2-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="465c2-112">value</span><span class="sxs-lookup"><span data-stu-id="465c2-112">value</span></span>  
    <span data-ttu-id="465c2-113">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="465c2-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="465c2-114">Valor que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="465c2-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="465c2-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="465c2-115">infoLevel</span></span>  
    <span data-ttu-id="465c2-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="465c2-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="465c2-117">Datos específicos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="465c2-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="465c2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="465c2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="465c2-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="465c2-119">Reference</span></span>

[<span data-ttu-id="465c2-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="465c2-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="465c2-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="465c2-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="465c2-122">Sobrecarga JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="465c2-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="465c2-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="465c2-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
