---
description: 'Más información sobre: API. JetDeleteColumn (método)'
title: Método API. JetDeleteColumn
TOCTitle: 'JetDeleteColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn(v=EXCHG.10)
ms:contentKeyID: 55100684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0801ffae0429b0c1d16d452d4170bdc6ce74937f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154046"
---
# <a name="apijetdeletecolumn-method"></a><span data-ttu-id="e9874-103">Método API. JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="e9874-103">Api.JetDeleteColumn method</span></span>

<span data-ttu-id="e9874-104">Elimina una columna de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e9874-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="e9874-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e9874-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e9874-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e9874-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e9874-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9874-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As StringApi.JetDeleteColumn(sesid, tableid, _
    column)
```

``` csharp
public static void JetDeleteColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column
)
```

#### <a name="parameters"></a><span data-ttu-id="e9874-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9874-108">Parameters</span></span>

  - <span data-ttu-id="e9874-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e9874-109">sesid</span></span>  
    <span data-ttu-id="e9874-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9874-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e9874-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e9874-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9874-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="e9874-112">tableid</span></span>  
    <span data-ttu-id="e9874-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9874-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e9874-114">Cursor en la tabla de la que se va a eliminar la columna.</span><span class="sxs-lookup"><span data-stu-id="e9874-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9874-115">columna</span><span class="sxs-lookup"><span data-stu-id="e9874-115">column</span></span>  
    <span data-ttu-id="e9874-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e9874-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e9874-117">Nombre de la columna que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="e9874-117">The name of the column to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9874-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9874-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e9874-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="e9874-119">Reference</span></span>

[<span data-ttu-id="e9874-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="e9874-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e9874-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="e9874-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e9874-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e9874-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
