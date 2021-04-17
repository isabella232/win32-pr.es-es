---
description: 'Más información sobre: Constructor de tablas'
title: Constructor de tablas
TOCTitle: 'Table constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.table(v=EXCHG.10)
ms:contentKeyID: 55104142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8987e643253791e5315dd07b7b20a40dee66cf9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696588"
---
# <a name="table-constructor"></a><span data-ttu-id="0c1c1-103">Constructor de tablas</span><span class="sxs-lookup"><span data-stu-id="0c1c1-103">Table constructor</span></span>

<span data-ttu-id="0c1c1-104">Inicializa una nueva instancia de la clase Table.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-104">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="0c1c1-105">La tabla se abre desde la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-105">The table is opened from the given database.</span></span>

<span data-ttu-id="0c1c1-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c1c1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c1c1-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c1c1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1c1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c1c1-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    name As String, _
    grbit As OpenTableGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim name As String
Dim grbit As OpenTableGrbit

Dim instance As New Table(sesid, dbid, _
    name, grbit)
```

``` csharp
public Table(
    JET_SESID sesid,
    JET_DBID dbid,
    string name,
    OpenTableGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0c1c1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c1c1-109">Parameters</span></span>

  - <span data-ttu-id="0c1c1-110">sesid</span><span class="sxs-lookup"><span data-stu-id="0c1c1-110">sesid</span></span>  
    <span data-ttu-id="0c1c1-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c1c1-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0c1c1-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c1c1-113">dbid</span><span class="sxs-lookup"><span data-stu-id="0c1c1-113">dbid</span></span>  
    <span data-ttu-id="0c1c1-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c1c1-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="0c1c1-115">Base de datos en la que se va a abrir la tabla.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-115">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c1c1-116">name</span><span class="sxs-lookup"><span data-stu-id="0c1c1-116">name</span></span>  
    <span data-ttu-id="0c1c1-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0c1c1-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0c1c1-118">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-118">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c1c1-119">grbit</span><span class="sxs-lookup"><span data-stu-id="0c1c1-119">grbit</span></span>  
    <span data-ttu-id="0c1c1-120">Tipo: [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0c1c1-120">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0c1c1-121">Opciones de JetOpenTable.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-121">JetOpenTable options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c1c1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c1c1-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c1c1-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="0c1c1-123">Reference</span></span>

[<span data-ttu-id="0c1c1-124">Table (clase)</span><span class="sxs-lookup"><span data-stu-id="0c1c1-124">Table class</span></span>](./table-class.md)

[<span data-ttu-id="0c1c1-125">Miembros de tabla</span><span class="sxs-lookup"><span data-stu-id="0c1c1-125">Table members</span></span>](./table-members.md)

[<span data-ttu-id="0c1c1-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0c1c1-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
